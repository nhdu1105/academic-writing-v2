# Academic Writing Skills

Bộ 5 skill cho Academic Writing, 15,000 từ, tiếng Anh, Harvard referencing — thiết kế để **phối hợp với nhau như một pipeline**, không phải 5 công cụ rời rạc. File này là bản đồ điều phối: skill nào gọi trước, skill nào cần input gì, đầu ra đi đâu tiếp theo, và khi nào phải quay lại bước trước thay vì đi tiếp.

## Cài đặt

**Qua Claude Code / Claude Cowork (plugin marketplace):**

```
/plugin marketplace add nhdu1105/academic-writing
/plugin install academic-writing-skills@academic-writing
```

Cả 5 skill sẽ xuất hiện dưới dạng `academic-writing-skills:<tên-skill>` và tự kích hoạt theo đúng chủ đề, không cần gõ lệnh — nhưng vì chúng phụ thuộc lẫn nhau, Claude cần tự kiểm tra trạng thái dự án trước khi chọn skill, không chỉ khớp từ khóa trong câu hỏi. Xem phần "Quy tắc điều phối" bên dưới.

**Qua Claude.ai / Claude API (upload thủ công):** vào từng thư mục trong `skills/`, nén nội dung thư mục đó (chứa `SKILL.md` và `references/` nếu có) thành file `.zip`, rồi tải lên theo hướng dẫn "Using skills in Claude" của Anthropic.

## 5 skill và hợp đồng input/output

Mỗi skill nhận một đầu vào cụ thể từ skill trước và tạo ra một đầu ra cụ thể cho skill sau. Đây là phần quan trọng nhất để phối hợp đúng — nếu input còn thiếu, gọi ngược lại skill sản xuất ra nó thay vì cố chạy skill hiện tại với dữ liệu giả định.

|Skill|Input cần có|Output tạo ra|Đưa cho|
|-|-|-|-|
|`rq-finding`|Hồ sơ người nghiên cứu (background, vai trò, quyền truy cập dữ liệu, nỗi bực dọc nghề nghiệp)|RQ đã khóa + title + aim + SMART objectives, đã qua Four Tests|`dissertation-structure`|
|`dissertation-structure`|RQ đã khóa + objectives|Outline toàn bài với word budget, hoặc outline chi tiết một chapter với "Argument to be made" cho từng section|`deep-research` (để tìm nguồn theo outline) và `academic-chapter-writing-agent` (để viết theo outline)|
|`deep-research`|Outline chapter (đặc biệt cột "Argument to be made")|Literature matrix theo từng section, nguồn đã gắn nhãn VERIFIED/UNVERIFIABLE/NOT FOUND, `[SOURCE NEEDED]` ở chỗ còn thiếu|`academic-chapter-writing-agent`|
|`academic-chapter-writing-agent`|Outline đã duyệt + literature matrix + rubric weighting của chapter đó|Draft chapter đã qua Argument-Review nội bộ (claim–evidence–interpretation–implication, warrant, hedging đúng mức)|`quality-check`|
|`quality-check`|Draft chapter hoặc toàn bài|Điểm theo rubric từng tiêu chí, gap cụ thể, fix cụ thể, và audit "golden thread" xuyên suốt các chapter|Quay lại skill tương ứng với loại gap (xem bảng loop-back)|

## Trình tự pipeline

```
rq-finding ──► dissertation-structure ──► deep-research
                       │                        │
                       └───────────┬────────────┘
                                   ▼
                  academic-chapter-writing-agent
                                   │
                                   ▼
                            quality-check
                                   │
                     (loop-back theo loại gap, xem dưới)
                                   │
                                   ▼
                                nộp bài
```

Đây không phải trình tự cứng chạy một lần từ trên xuống. `deep-research` và `academic-chapter-writing-agent` lặp lại cho **mỗi chapter**; `quality-check` chạy sau mỗi chapter và lại một lần nữa cho toàn bài trước khi nộp.

## Quy tắc điều phối

Đây là phần Claude cần áp dụng chủ động, không chờ người dùng gọi đúng tên skill.

**1. Kiểm tra trạng thái trước khi chọn skill.** Trước khi chạy bất kỳ skill nào, xác định dự án đang ở đâu trong pipeline dựa trên những gì đã có trong cuộc hội thoại hoặc tài liệu người dùng cung cấp: đã có RQ khóa chưa? đã có outline duyệt chưa? đã có literature matrix cho chapter này chưa? Nếu người dùng nhảy thẳng tới một bước ("viết Chapter 2 cho tôi") nhưng bước trước đó chưa xong (chưa có outline duyệt, hoặc outline có nhưng chưa có literature matrix), không chạy `academic-chapter-writing-agent` với dữ liệu tự bịa. Nói rõ input nào còn thiếu, và đề xuất chạy skill sản xuất ra nó trước — hoặc chạy nối tiếp trong cùng một lượt nếu người dùng đã cung cấp đủ nguyên liệu thô (ví dụ ghi chú rời) để skill trước xử lý ngay.

**2. Không chạy `academic-chapter-writing-agent` mà không có outline đã duyệt.** Bản thân skill này yêu cầu outline ở bước khởi tạo. Nếu chưa có, gọi `dissertation-structure` trước, trình bày outline, và chỉ chuyển sang viết sau khi người dùng xác nhận — đúng như quy tắc "duyệt trước khi viết" đã ghi trong `dissertation-structure`.

**3. Không chạy `academic-chapter-writing-agent` khi outline có ô `[SOURCE NEEDED]` chưa xử lý** cho phần người dùng muốn viết. Ưu tiên chạy lại `deep-research` cho đúng mục đó trước, hoặc hỏi người dùng có tài liệu riêng để lấp không.

**4. Loop-back từ `quality-check` theo loại gap** — đừng chỉ liệt kê điểm yếu rồi dừng, hãy chỉ ra skill nào xử lý loại gap đó:

|Loại gap `quality-check` phát hiện|Quay lại skill|
|-|-|
|Golden thread đứt gãy (RQ Ch1 không khớp Ch4, objective không có mục tương ứng ở Ch5, thuật ngữ trôi giữa các chapter)|`dissertation-structure` — sửa kiến trúc trước, đừng sửa câu chữ|
|Trích dẫn không xác minh được, thiếu nguồn cho một luận điểm, tỷ lệ nguồn quá cũ|`deep-research`|
|Lập luận yếu — mô tả thay vì luận, thiếu warrant, overclaiming, thiếu counter-position|`academic-chapter-writing-agent` — yêu cầu chạy lại Argument-Review nội bộ trên đúng đoạn đó|
|RQ tự nó là pseudo-topic, hoặc không qua nổi Four Tests|`rq-finding` — đây là dấu hiệu vấn đề nằm từ gốc, không phải lỗi viết|

**5. Không để hai skill giẫm chân nhau.** `dissertation-structure` quyết định kiến trúc và word budget; `academic-chapter-writing-agent` chỉ viết trong khung đó, không tự đổi cấu trúc. `deep-research` chỉ tổng hợp bằng chứng, không viết văn xuôi dissertation; nếu người dùng yêu cầu "viết luôn đoạn văn" từ kết quả research, đó là tín hiệu chuyển sang `academic-chapter-writing-agent` với literature matrix vừa có làm input, không phải để `deep-research` tự viết.

**6. Theo dõi trạng thái xuyên suốt hội thoại.** Ghi nhớ: RQ đã khóa (nội dung), outline đã duyệt (theo chapter), chapter nào đã có literature matrix, chapter nào đã có draft, điểm `quality-check` gần nhất của từng chapter. Khi người dùng quay lại sau một khoảng, dùng trạng thái này để biết nên tiếp nối ở đâu thay vì hỏi lại từ đầu.

## Bốn thứ được mã hóa trong bộ skill này

**Four Tests và bẫy Pseudo-Topic.** Lấy từ Dissertation Guide của trường. Đề tài phải qua cả bốn: Feasibility, Originality, Significance, Boundedness. Và phải vượt được bẫy pseudo-topic — câu hỏi mà examiner biết trước câu trả lời.

**Thang địa lý có lập luận transferability.** Vietnam → Đông Nam Á → Châu Á → Âu/Mỹ → Toàn cầu. Khi dùng bằng chứng ngoài Việt Nam, bắt buộc phải lập luận trên ít nhất hai chiều tương đồng (cấu trúc kinh tế, thể chế, độ trưởng thành thị trường, văn hóa, nhân khẩu) **và** nêu giới hạn của phép chuyển. Lập luận transferability không tìm ra giới hạn nào thì không phải lập luận.

**Word budget theo trọng số rubric.** 15,000 từ phân bổ theo % chấm điểm, với Chapter 4 được cấp nhiều từ hơn trọng số 20% vì nó chứa cả findings lẫn discussion. Reflection MBA path cap cứng 1,000 từ.

**Ba trạng thái nguồn.** VERIFIED / UNVERIFIABLE / NOT FOUND. Nguồn không xác minh được không vào reference list. Chỗ nào lập luận thiếu nguồn thì đánh dấu `[SOURCE NEEDED]` chứ không lấp bằng trích dẫn tự sinh.

## Hai file reference đi kèm

**`dissertation-structure/references/methodology-selection.md`** — sáu thiết kế nghiên cứu khả thi ở quy mô 15,000 từ kèm điểm chết của từng loại, thứ tự câu hỏi để chọn, sàn cỡ mẫu, cây quyết định human subjects ethics, và bài toán dùng dữ liệu nội bộ nơi mình làm việc trong ngành có quản lý chặt.

**`quality-check/references/reasoning-audit.md`** — các họ ngụy biện hay gặp trong luận văn kinh doanh, kiểm toán Toulmin, phép thử causal claim, đánh giá giải thích thay thế, thang epistemic 5 mức, kiểm tra tính toàn vẹn dữ liệu của chính mình, chuẩn báo cáo thống kê kèm benchmark effect size, và self-plagiarism.

## Những gì lấy từ Academic Research Skills

Bộ này kế thừa một số công cụ từ ARS (Cheng-I Wu 吳政宜, CC BY-NC 4.0), đã lược bỏ phần không hợp quy mô:

|Lấy|Vào đâu|
|-|-|
|Mô hình CARS (Swales) 3 moves + bẫy universal negative + niche-purpose mismatch|`dissertation-structure`, Chapter 1|
|Mô hình Toulmin 6 thành phần, trọng tâm là **Warrant**|`academic-chapter-writing-agent`|
|Thang epistemic status 5 mức|`academic-chapter-writing-agent`|
|6 loại câu hỏi Socratic|`rq-finding`|
|Danh mục ngụy biện, thu gọn còn 3 họ liên quan|`reasoning-audit.md`|
|Bradford Hill adapted làm phép thử causal claim|`reasoning-audit.md`|
|Inference to Best Explanation|`reasoning-audit.md`|
|Chuẩn báo cáo thống kê + benchmark Cohen|`reasoning-audit.md`|
|Own-data integrity checks|`reasoning-audit.md`|
|Cây quyết định IRB, đã bỏ phần đặc thù Đài Loan|`methodology-selection.md`|
|Research design patterns, giữ 6 loại khả thi|`methodology-selection.md`|

**Không lấy:** PRISMA và systematic review protocol, meta-analysis, preregistration, EQUATOR — quá tầm cho một dissertation 15,000 từ một nghiên cứu. Template LaTeX, journal submission, venue disclosure, CRediT authorship, funding statement — không liên quan tới bài nộp Word một tác giả. Hướng dẫn APA7 và trích dẫn tiếng Trung — bạn dùng Harvard. Toàn bộ cơ chế điều phối multi-agent gốc của ARS — không chuyển sang skill được; phần điều phối trong file này được viết riêng cho 5 skill ở trên.

**Lưu ý về nguồn:** ARS trích một số bài rất mới cho phần taxonomy lỗi AI mà tôi không xác minh được. Các checklist vẫn dùng được vì tự nó đứng vững về mặt lập luận, nhưng đừng trích những bài đó vào dissertation nếu chưa tự kiểm tra chúng có thật.

## Phạm vi

Bộ skill này được thiết kế để co-pilot với người dùng từ khâu lên ý tưởng nghiên cứu, đánh giá ý tưởng nghiên cứu, thiết lập cấu trúc bài viết, tự động nghiên cứu và tìm nguồn tài liệu phù hợp, viết phân tích (hoặc tự viết và nhờ check) theo rule được mô tả chặt chẽ, kiểm tra lại chất lượng bài viết — với việc điều phối giữa các bước đó do Claude tự quản lý theo trạng thái dự án, không phải do người dùng phải nhớ đúng trình tự và gọi đúng tên skill mỗi lần.
