# Kế hoạch chi tiết thực hiện bài kiểm tra thực hành nhóm trí tuệ nhân tạo (AI Team Lab)

Dự án thực tế: ClauseNest, nền tảng rà soát và trợ lý hợp đồng pháp lý trí tuệ nhân tạo.
Đội ngũ thực hiện:
* Kiều Hồng Phong (Quản lý sản phẩm)
* Đỗ Duy Đức (Kỹ sư trí tuệ nhân tạo)
* Nguyễn Đức Đạt (Kỹ sư phần mềm toàn năng)

## PHẦN 1: PHÂN CÔNG NHIỆM VỤ

### 1. Kiều Hồng Phong (Quản lý sản phẩm)
Nhiệm vụ chính: Quản trị chung, chủ trì xác định phạm vi dự án và lập bản đồ các bên liên quan (stakeholder map). Chịu trách nhiệm soạn thảo bài thuyết trình (pitch), điều phối họp định kỳ và nộp bài đại diện cho nhóm.
Trách nhiệm đầu ra: Chốt phạm vi dự án, chủ trì nội dung bản đồ các bên liên quan (Trang 1) và phối hợp viết bài thuyết trình (Trang 2).

### 2. Đỗ Duy Đức (Kỹ sư trí tuệ nhân tạo)
Nhiệm vụ chính: Phụ trách toàn bộ cấu trúc dữ liệu kỹ thuật, thuật toán ghép cặp (Hungarian Matching), tìm kiếm thời gian thực (live legal grounding), chỉ số đo lường độ chính xác và hệ thống đánh giá (evaluation framework).
Trách nhiệm đầu ra: Cung cấp số liệu bằng chứng thực tế (evidence) cho bài thuyết trình (Trang 2), phụ trách định hình vai trò cốt lõi kỹ thuật (Trang 3) và chủ trì thiết lập khung năng lực (competency framework) tại Trang 4.

### 3. Nguyễn Đức Đạt (Kỹ sư phần mềm toàn năng)
Nhiệm vụ chính: Phụ trách kiến trúc hệ thống giao diện lập trình ứng dụng (API), giao diện người dùng (frontend), cơ chế phân quyền truy cập (RBAC) và chiến lược bù đắp năng lực (resourcing strategy).
Trách nhiệm đầu ra: Phản biện bài thuyết trình và rà soát ma trận phân quyền (RACI matrix) tại Trang 2, chủ trì hoạch định chiến lược bù đắp năng lực (Trang 3) và chuẩn hóa cấu trúc dữ liệu giao tiếp (data contract) tại Trang 4.

## PHẦN 2: LỊCH TRÌNH THỰC HIỆN TỪNG BƯỚC

Khung thời gian 120 phút được chia thành các giai đoạn (phase) sau đây:

Giai đoạn 0: Chốt phạm vi dự án (Scope and Ground Rules)
Thời gian: 5 phút. Toàn nhóm cùng thực hiện. Phong chủ trì chốt mục tiêu và hoàn thiện tệp giới thiệu.

Giai đoạn 1: Bản đồ các bên liên quan và chiến lược (Stakeholder Map and Strategy)
Thời gian: 20 phút. Cá nhân làm trước rồi tổng hợp. Phong chủ trì lập danh sách 6 bên liên quan cụ thể, lập ma trận đánh giá và đưa ra 4 chiến lược.

Giai đoạn 2: Bài thuyết trình và ma trận phân quyền (Pitch and RACI Matrix)
Thời gian: 30 phút. Nhóm lên ý tưởng, cá nhân viết lại và nhóm chốt. Đức và Phong chủ trì xây dựng bài thuyết trình cấu trúc kết luận trước, xử lý phản biện và lập ma trận phân quyền.

Giai đoạn 3: Thiết kế đội ngũ (AI Team Design)
Thời gian: 25 phút. Toàn nhóm cùng thảo luận. Đạt và Đức chủ trì chọn mô hình kiến trúc, xác định vai trò cốt lõi và phương án bù đắp năng lực.

Giai đoạn 4: Kế hoạch phát triển (Team Health and Growth Plan)
Thời gian: 25 phút. Cá nhân tự chấm điểm rồi tổng hợp. Cả nhóm đánh giá 4 khía cạnh vận hành, nâng cấp khung năng lực và đề ra 3 hành động cụ thể trong 30 ngày.

Giai đoạn 5: Rà soát và nộp bài
Thời gian: 15 phút. Phong và Đạt chủ trì kiểm tra tính nhất quán giữa các trang, xuất tài liệu định dạng PDF và nộp lên kho lưu trữ (repository).

## PHẦN 3: NỘI DUNG GỢI Ý DÀNH CHO CÁC THÀNH VIÊN (PROMPTS)

Để tối ưu hóa thời gian, dưới đây là các đoạn lệnh gợi ý (prompt) để các thành viên sử dụng khi làm việc với hệ thống AI. Đoạn lệnh đã được bổ sung danh sách kiểm tra (checklist) và quy định văn phong rõ ràng. Yêu cầu sao chép toàn bộ khối nội dung bên dưới và gửi cho AI.

### 1. Gợi ý dành cho Đỗ Duy Đức (Kỹ sư trí tuệ nhân tạo)

Đóng vai là một kỹ sư trí tuệ nhân tạo cấp cao (Senior AI Engineer) trong dự án ClauseNest, nền tảng rà soát hợp đồng pháp lý. Mục tiêu là nâng cấp hệ thống đa tác nhân (multi-agent) đạt độ chính xác phát hiện sai lệch trên 95 phần trăm.

Quy tắc hành văn bắt buộc (Style Guidelines):
* Sử dụng văn phong học thuật chuyên nghiệp nhưng không quá vĩ mô.
* Tuyệt đối không sử dụng dấu ngoặc kép.
* Tuyệt đối không sử dụng dấu gạch nối giữa dòng hoặc gạch đầu dòng dạng dấu trừ.
* Tuyệt đối không in đậm đột ngột giữa câu.
* Tuyệt đối không sử dụng biểu tượng cảm xúc (icons hoặc emojis).
* Dịch các thuật ngữ chuyên ngành sang tiếng Việt và chú thích tiếng Anh trong ngoặc đơn, ví dụ như khung năng lực (competency framework).

Danh sách công việc cần hoàn thành (Task Checklist):
* Hạng mục 1: Viết một đoạn dữ liệu thực chứng (evidence) chứng minh độ chính xác của hệ thống. Bắt buộc nhắc đến thuật toán ghép cặp (Hungarian Matching) và cơ chế tra cứu thời gian thực (live legal grounding).
* Hạng mục 2: Thiết kế khung năng lực (competency framework) từ cấp độ 1 đến cấp độ 3 cho vị trí kỹ sư trí tuệ nhân tạo. Tập trung mạnh vào kỹ năng thiết lập hệ thống kiểm thử tự động (automated evaluation).
* Hạng mục 3: Viết một câu đánh giá sức khỏe đội ngũ về mặt chất lượng AI. Chỉ ra điểm mạnh của hệ thống đa tác nhân và phân tích rủi ro ở khâu nhận dạng ký tự quang học (OCR) đối với tài liệu quét (scan).

### 2. Gợi ý dành cho Nguyễn Đức Đạt (Kỹ sư phần mềm toàn năng)

Đóng vai là một kỹ sư phần mềm toàn năng cấp cao (Senior Fullstack Engineer) trong dự án ClauseNest.

Quy tắc hành văn bắt buộc (Style Guidelines):
* Sử dụng văn phong học thuật chuyên nghiệp nhưng không quá vĩ mô.
* Tuyệt đối không sử dụng dấu ngoặc kép.
* Tuyệt đối không sử dụng dấu gạch nối giữa dòng hoặc gạch đầu dòng dạng dấu trừ.
* Tuyệt đối không in đậm đột ngột giữa câu.
* Tuyệt đối không sử dụng biểu tượng cảm xúc (icons hoặc emojis).
* Dịch các thuật ngữ chuyên ngành sang tiếng Việt và chú thích tiếng Anh trong ngoặc đơn, ví dụ như chiến lược bù đắp năng lực (priority resourcing).

Danh sách công việc cần hoàn thành (Task Checklist):
* Hạng mục 1: Viết một đoạn ngắn biện luận lý do dự án quy mô 3 người lựa chọn kiến trúc nhúng (embedded architecture). Nhấn mạnh vào lợi ích của việc phối hợp trực tiếp trên cùng một hệ thống mã nguồn (codebase).
* Hạng mục 2: Lập chiến lược bù đắp năng lực (priority resourcing) cho 3 lỗ hổng bao gồm thẩm định pháp lý chuyên sâu, thiết kế hệ thống giao diện, và tự động hóa vận hành học máy (MLOps). Yêu cầu chọn một trong ba phương án là tuyển dụng (hire), thuê ngoài (outsource) hoặc hợp tác (partner) cho mỗi lỗ hổng và giải thích thật ngắn gọn.
* Hạng mục 3: Viết một hành động cụ thể trong kế hoạch 30 ngày (growth plan) để giải quyết vấn đề lệch cấu trúc dữ liệu giao tiếp (data contract) giữa máy chủ lõi và dịch vụ trí tuệ nhân tạo. Bắt buộc sử dụng chuẩn OpenAPI và đưa ra dấu hiệu hoàn thành (deliverable) rõ ràng.

## PHẦN 4: HƯỚNG DẪN KIỂM TRA CHÉO (GATE 5 CHECK)

Trang 1 và Trang 2: Trưởng ban pháp chế (người cần thuyết phục ở Trang 1) phải là đối tượng nhận bài thuyết trình ở Trang 2.
Trang 3 và Trang 4: Lỗ hổng về kiểm thử tự động (capability gap) ở Trang 3 phải khớp với vấn đề tốc độ và năng lực cần nâng cấp của kỹ sư trí tuệ nhân tạo ở Trang 4.
Trang 2 và Trang 4: Người phụ trách trong kế hoạch phát triển ở Trang 4 phải khớp chính xác với người chịu trách nhiệm cuối cùng (Accountable) trong ma trận phân quyền ở Trang 2.
