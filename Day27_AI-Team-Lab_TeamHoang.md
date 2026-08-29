# Day 27: AI Team Lab từ Stakeholder đến Team Health và Growth Plan

Dự án: ClauseNest
Mô tả: Nền tảng rà soát và trợ lý hợp đồng pháp lý trí tuệ nhân tạo (AI Legal Assistant)
Thành viên thực hiện:
* Kiều Hồng Phong (Product Lead)
* Đỗ Duy Đức (AI Engineer)
* Nguyễn Đức Đạt (Fullstack Software Engineer)
Mục tiêu hiện tại: Đạt chứng nhận sản phẩm khả dụng tối thiểu (MVP) trong vòng 1 đến 3 tháng tới. Triển khai thử nghiệm (pilot) cho 3 phòng pháp chế đối tác. Yêu cầu kỹ thuật đạt độ chính xác rà soát rủi ro pháp lý lớn hơn 92 phần trăm, độ trễ xử lý dưới 3 giây và hỗ trợ tối thiểu 5 loại hợp đồng kinh tế phổ biến.

## TRANG 1: BẢN ĐỒ CÁC BÊN LIÊN QUAN VÀ CHIẾN LƯỢC (STAKEHOLDER MAP AND STRATEGY)

### 1. Danh sách các bên liên quan (Stakeholders)
1. Giảng viên hướng dẫn (Mentor): Chuyên gia đánh giá kiến trúc kỹ thuật đa tác nhân (multi-agent) và tính khả thi của giải pháp.
2. Trưởng ban pháp chế doanh nghiệp đối tác (Legal Lead): Người có thẩm quyền phê duyệt việc đưa công cụ trí tuệ nhân tạo vào quy trình rà soát hợp đồng chính thức.
3. Chuyên viên kinh doanh và mua hàng (Sales and Procurement Specialist): Người dùng cuối thường xuyên tạo, đàm phán hợp đồng và cần phát hiện nhanh sai lệch so với mẫu chuẩn.
4. Luật sư cố vấn chuyên môn (Domain Legal Expert): Cố vấn thẩm định tính chính xác của các điều khoản đối chiếu theo hệ thống luật hiện hành.
5. Giám đốc công nghệ và quản trị bảo mật (CTO and IT Security Officer): Người kiểm soát rủi ro an toàn thông tin, bảo mật tài liệu hợp đồng và phân quyền dữ liệu.
6. Đội ngũ nòng cốt (Core Team): Nhóm trực tiếp phát triển, tích hợp và vận hành hệ thống trí tuệ nhân tạo bao gồm Phong, Đức và Đạt.

### 2. Ma trận các bên liên quan (Stakeholder Matrix)

Vùng đánh giá (Quadrant): Mức độ quan tâm thấp (Low Interest) và Mức độ ảnh hưởng cao (High Influence)
* Nhóm cản trở (Blocker): Cần giữ hài lòng và giải tỏa triệt để mối lo.
* Giám đốc công nghệ và quản trị bảo mật: Thái độ hiện tại (stance) là chưa ủng hộ. Khách hàng lo ngại rò rỉ dữ liệu hợp đồng mật khi gọi giao diện lập trình ứng dụng (API).
* Trưởng ban pháp chế: Thái độ hiện tại (stance) là trung lập. Khách hàng hoài nghi khả năng hiểu luật chuyên sâu của trí tuệ nhân tạo.

Vùng đánh giá (Quadrant): Mức độ quan tâm cao (High Interest) và Mức độ ảnh hưởng cao (High Influence)
* Nhóm ủng hộ chủ chốt (Champion): Cần hợp tác chặt chẽ.
* Giảng viên hướng dẫn: Thái độ hiện tại (stance) là ủng hộ. Giảng viên tích cực kết nối và tư vấn giải pháp.
* Đội ngũ nòng cốt: Thái độ hiện tại (stance) là ủng hộ. Nhóm cam kết hoàn thành mục tiêu.

Vùng đánh giá (Quadrant): Mức độ quan tâm thấp (Low Interest) và Mức độ ảnh hưởng thấp (Low Influence)
* Nhóm theo dõi (Bystander): Theo dõi định kỳ.
* Nhà đầu tư (Investor): Thái độ hiện tại (stance) là trung lập. Nhà đầu tư đang quan sát chỉ số phát triển và bản dùng thử (demo).

Vùng đánh giá (Quadrant): Mức độ quan tâm cao (High Interest) và Mức độ ảnh hưởng thấp (Low Influence)
* Nhóm hỗ trợ (Supporter): Giữ thông tin và liên tục lấy phản hồi (feedback).
* Chuyên viên kinh doanh: Thái độ hiện tại (stance) là ủng hộ. Nhóm này rất hào hứng vì hệ thống giúp giảm thời gian đọc dò hợp đồng.
* Luật sư cố vấn chuyên môn: Thái độ hiện tại (stance) là ủng hộ. Chuyên gia sẵn sàng hỗ trợ kiểm tra tập dữ liệu.

### 3. Chiến lược cho bốn bên liên quan ưu tiên (Priority Stakeholders)

Chiến lược tận dụng sự ủng hộ:
* Giảng viên hướng dẫn: Họ quan tâm tính đột phá của hệ thống đa tác nhân và độ tin cậy khi kiểm chứng thực tế. Họ có thể giúp giới thiệu dự án với các doanh nghiệp trong mạng lưới. Hành động cụ thể là gửi báo cáo đo lường chuẩn (benchmark) so sánh độ chính xác của 3 tác nhân trước thứ sáu.
* Chuyên viên kinh doanh: Họ quan tâm giao diện so sánh sai lệch trực quan (visual diff) và xuất báo cáo nhanh. Họ có thể cung cấp 20 mẫu hợp đồng thực tế đã qua chỉnh sửa. Hành động cụ thể là cung cấp tài khoản trải nghiệm tính năng trên môi trường thử nghiệm (staging) trước thứ ba kèm biểu mẫu khảo sát.

Chiến lược ưu tiên thuyết phục:
* Giám đốc công nghệ: Họ lo ngại hợp đồng kinh tế chứa bí mật kinh doanh bị gửi ra ngoài. Họ có thể chặn cổng mạng hoặc từ chối cấp phép. Hành động cụ thể là soạn tài liệu kỹ thuật chuyên sâu (whitepaper) trình bày rõ cơ chế mã hóa phân tầng và phân quyền truy cập (RBAC) để thuyết phục vào thứ năm.
* Trưởng ban pháp chế: Họ lo ngại trí tuệ nhân tạo bị ảo giác (hallucination) và trích dẫn sai luật. Họ có thể không cho phép nhân viên sử dụng hệ thống. Hành động cụ thể là trình diễn tính năng tra cứu thời gian thực (live legal grounding) và cơ chế vòng lặp con người (human-in-the-loop) vào thứ tư tuần sau.

## TRANG 2: BÀI THUYẾT TRÌNH VÀ MA TRẬN PHÂN QUYỀN (PITCH AND RACI MATRIX)

### 1. Bài thuyết trình cấu trúc kết luận trước (Conclusion First Pitch)
Kết luận: Đội ngũ đề xuất triển khai chương trình thử nghiệm (pilot) 14 ngày sử dụng nền tảng ClauseNest cho phòng pháp chế, giúp giảm 60 phần trăm thời gian rà soát hợp đồng và loại bỏ rủi ro điều khoản trái luật.
Lý do chính: Quy trình đối chiếu thủ công hiện mất rất nhiều thời gian và dễ bỏ sót các thay đổi tinh vi. Hệ thống tự động phân tích cây cấu trúc điều khoản và phát hiện sai lệch chỉ trong 30 giây.
Dữ liệu thực chứng (Evidence): Trên tập kiểm thử 100 hợp đồng thực tế, hệ thống đạt độ chính xác phát hiện sai lệch 95.2 phần trăm nhờ thuật toán ghép cặp (Hungarian Matching) và độ chính xác phân tích rủi ro pháp lý 91.8 phần trăm nhờ hội đồng đánh giá chéo (cross-judge). Thời gian xử lý trung bình dưới 2.5 giây cho mỗi hợp đồng.
Đề nghị hành động nhỏ (Small ask): Đề xuất trưởng ban pháp chế cho phép 2 chuyên viên tham gia buổi hướng dẫn sử dụng (onboarding) 30 phút vào thứ ba tuần tới để trải nghiệm trực tiếp.

### 2. Phản biện chính và phương án xử lý
Phản biện: Khách hàng thường đặt câu hỏi làm sao đảm bảo trí tuệ nhân tạo không trích dẫn các văn bản pháp luật đã hết hiệu lực.
Phương án xử lý: Hệ thống tích hợp công nghệ tra cứu thời gian thực (live legal grounding) qua giao diện lập trình ứng dụng (API) kết nối trực tiếp đến các cơ sở dữ liệu pháp luật chính thống. Hệ thống tự động kiểm tra trạng thái hiệu lực văn bản trước khi đưa ra kết luận và hiển thị đường dẫn trích dẫn luật gốc.

### 3. Ma trận phân quyền (RACI Matrix)

* Chuẩn hóa luồng người dùng (user flow): Phong chịu trách nhiệm cuối cùng (Accountable). Đạt và Đức cần được hỏi ý kiến (Consulted). Giảng viên cần được thông báo (Informed).
* Thu thập và gán nhãn bộ dữ liệu (dataset): Đức chịu trách nhiệm cuối cùng (Accountable). Đạt là người trực tiếp làm (Responsible). Phong và giảng viên cần được hỏi ý kiến (Consulted).
* Phát triển hệ thống đa tác nhân (multi-agent): Đức chịu trách nhiệm cuối cùng (Accountable). Đạt là người trực tiếp làm (Responsible). Giảng viên cần được hỏi ý kiến (Consulted). Phong cần được thông báo (Informed).
* Xây dựng giao diện (frontend) và hệ thống lõi (backend core): Đạt chịu trách nhiệm cuối cùng (Accountable). Đức là người trực tiếp làm (Responsible). Phong cần được hỏi ý kiến (Consulted). Giảng viên cần được thông báo (Informed).
* Thiết lập hệ thống kiểm thử tự động (automated evals): Đức chịu trách nhiệm cuối cùng (Accountable). Đạt là người trực tiếp làm (Responsible). Phong cần được thông báo (Informed). Giảng viên cần được hỏi ý kiến (Consulted).
* Vận hành chương trình thử nghiệm (pilot): Phong chịu trách nhiệm cuối cùng (Accountable). Đạt và Đức là người trực tiếp làm (Responsible). Giảng viên cần được hỏi ý kiến (Consulted).

## TRANG 3: THIẾT KẾ ĐỘI NGŨ (AI TEAM DESIGN)

### 1. Kiến trúc đội ngũ (Team Architecture)
Mô hình lựa chọn: Kiến trúc nhúng (embedded architecture). Năng lực trí tuệ nhân tạo được nhúng trực tiếp vào nhóm phát triển sản phẩm.
Lý do lựa chọn: Với quy mô 3 người, mô hình này loại bỏ rào cản phòng ban, giúp kỹ sư phần mềm và kỹ sư trí tuệ nhân tạo phối hợp trực tiếp trên cùng một hệ thống mã nguồn (codebase).

### 2. Phân định vai trò (Roles)
Vai trò cốt lõi (Core roles):
* Quản lý sản phẩm (Product Lead): Định hình bài toán, xây dựng bộ tiêu chí đánh giá (evaluation rubrics) và quản lý tiến độ.
* Kỹ sư trí tuệ nhân tạo (AI Engineer): Phát triển thuật toán, kỹ thuật tinh chỉnh câu lệnh (prompt engineering) và hệ thống kiểm thử tự động.
* Kỹ sư phần mềm toàn năng (Fullstack Software Engineer): Xây dựng kiến trúc hệ thống lõi (backend core) và giao diện người dùng (frontend).
Vai trò mở rộng (Extended roles): Cố vấn pháp lý chuyên sâu và kỹ sư bảo mật hệ thống (security engineer) cho giai đoạn mở rộng quy mô (scale).

### 3. Chiến lược bù đắp năng lực (Priority Resourcing)
Thẩm định án lệ chuyên sâu: Sử dụng phương án hợp tác (partner) với văn phòng luật sư đối tác để cố vấn định kỳ. Không cần tuyển nhân sự cố định ở giai đoạn sản phẩm khả dụng tối thiểu (MVP).
Thiết kế hệ thống giao diện (design system): Sử dụng phương án thuê ngoài (outsource). Dự án sẽ thuê chuyên gia thiết kế bộ giao diện chuẩn một lần duy nhất để tối ưu chi phí.
Tự động hóa hệ thống vận hành học máy (MLOps): Sử dụng phương án tự đào tạo nâng cấp (up-skill). Đội ngũ sẽ tận dụng các công cụ mã nguồn mở và tự trau dồi thay vì tuyển nhân sự mới.

### 4. Mục tiêu của đội ngũ (Squad Goal)
Đội ngũ của chúng tôi sở hữu nền tảng ClauseNest và chịu trách nhiệm đưa bản nguyên mẫu (prototype) từ hiện trạng lên bản sản phẩm khả dụng tối thiểu (MVP) đạt độ chính xác trên 95 phần trăm trong vòng 45 ngày.

## TRANG 4: SỨC KHỎE ĐỘI NGŨ VÀ KẾ HOẠCH PHÁT TRIỂN (TEAM HEALTH AND GROWTH PLAN)

### 1. Đánh giá sức khỏe đội ngũ (Team Health Score)
Chất lượng hệ thống: Đạt 3.8 trên 5 điểm. Thuật toán hoạt động tốt nhưng đôi khi gặp lỗi tiền xử lý với các tài liệu quét (scan) chất lượng kém.
Tiến độ dự án: Đạt 3.0 trên 5 điểm. Đội ngũ đang bị trễ tiến độ ở khâu đồng bộ dữ liệu giao tiếp (DTO) do chưa chuẩn hóa cấu trúc từ đầu.
Tinh thần đội ngũ: Đạt 4.8 trên 5 điểm. Tinh thần trách nhiệm cao, các thành viên giao tiếp cởi mở và chủ động khắc phục sự cố.
Tốc độ ra sản phẩm: Đạt 3.2 trên 5 điểm. Đội ngũ đang tốn nhiều thời gian kiểm thử chất lượng thủ công thay vì sử dụng hệ thống kiểm thử tự động.

### 2. Nâng cấp khung năng lực (Competency Framework)
Vai trò được chọn: Kỹ sư trí tuệ nhân tạo (AI Engineer).
Cấp độ hiện tại: Cấp độ thực hành (L2 AI Practitioner). Kỹ sư đã làm chủ kỹ thuật tinh chỉnh câu lệnh và tìm kiếm vector.
Năng lực trọng tâm cần nâng cấp: Cấp độ xây dựng kiến trúc (L3 AI Builder). Kỹ sư cần thiết lập hệ thống kiểm thử tự động (automated evaluation) cho cấu trúc đa tác nhân.
Hành động 30 ngày: Xây dựng bộ kiểm thử chuẩn gồm 30 trường hợp pháp lý (golden cases) và viết kịch bản đo lường tự động qua hệ thống tích hợp liên tục (CI/CD).

### 3. Kế hoạch phát triển 30 ngày (Growth Plan)
Khắc phục khâu kiểm thử thủ công: Đức phụ trách xây dựng bộ kiểm thử 30 trường hợp tiêu chuẩn và kịch bản đo lường tự động (automated evals). Hạn hoàn thành là ngày 15 tháng 9 năm 2026. Dấu hiệu hoàn thành là tập dữ liệu chuẩn được tạo và hệ thống tự động báo cáo độ chính xác.
Khắc phục độ trễ tiến độ tích hợp: Đạt phụ trách chuẩn hóa toàn bộ cấu trúc dữ liệu giao tiếp (data contract) bằng chuẩn OpenAPI. Hạn hoàn thành là ngày 5 tháng 9 năm 2026. Dấu hiệu hoàn thành là tài liệu giao diện lập trình ứng dụng (API) được đồng bộ hoàn toàn.
Cải thiện quản trị rủi ro tiến độ: Phong phụ trách thiết lập các buổi họp ngắn hằng ngày (daily standup) và tổng kết định kỳ. Hạn hoàn thành là hằng tuần. Dấu hiệu hoàn thành là bảng công việc (kanban board) được cập nhật liên tục.
