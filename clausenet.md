# Bối Cảnh Dự Án: ClauseNest (P-134)
**Nền tảng Rà soát & Trợ lý Hợp đồng Pháp lý AI**

Tài liệu này cung cấp toàn bộ bối cảnh (context) về dự án ClauseNest để các thành viên (Phong, Đức, Đạt) đưa vào Prompt khi làm việc với AI, giúp AI hiểu sâu sắc về bài toán, nghiệp vụ và kiến trúc kỹ thuật đang giải quyết.

---

## 1. Tổng Quan Dự Án (Project Overview)
- **Tên dự án:** ClauseNest
- **Mã dự án:** P-134
- **Lĩnh vực:** LegalTech (Công nghệ Pháp lý) dành cho thị trường Việt Nam.
- **Vấn đề giải quyết:** Quy trình đối chiếu, rà soát hợp đồng thủ công của phòng Pháp chế và Mua hàng/Kinh doanh (thường dài 30 trang) mất từ 3–5 giờ/hợp đồng. Dễ bỏ sót các thay đổi tinh vi ở phụ lục, các bẫy phạt vi phạm, hoặc các điều khoản trái với pháp luật Việt Nam (Luật Thương mại 2005, Bộ luật Dân sự 2015).
- **Giải pháp:** Nền tảng AI tự động phân tích cấu trúc hợp đồng, so sánh (diff) sai lệch so với mẫu chuẩn, rà soát rủi ro pháp lý và đề xuất sửa đổi theo thời gian thực (Live Legal Grounding).

## 2. Mục Tiêu Ngắn Hạn (1–3 Tháng tới)
- **Giai đoạn:** Chuyển từ bản Prototype nội bộ (độ chính xác 75%) lên bản MVP (Minimum Viable Product).
- **Target:** Triển khai chạy thử nghiệm (Pilot) 14 ngày cho 3 phòng Pháp chế/Kinh doanh của doanh nghiệp đối tác.
- **KPIs Kỹ thuật:**
  - Độ chính xác phát hiện sai lệch văn bản (Visual Diff): > 95%.
  - Độ chính xác phân tích rủi ro luật: > 92%.
  - Độ trễ xử lý (Latency): < 3 giây/hợp đồng.
  - Hỗ trợ xử lý: Tối thiểu 5 loại hợp đồng kinh tế phổ biến.

## 3. Kiến Trúc Kỹ Thuật (Technical Architecture)
### 3.1. AI / ML / LLM (Phụ trách: Đỗ Duy Đức)
- **Framework:** LangGraph (Multi-Agent Architecture).
- **Thuật toán cốt lõi:**
  - **Hungarian Matching:** Dùng để bóc tách cây cấu trúc hợp đồng (Phụ lục ➔ Chương ➔ Điều ➔ Khoản ➔ Điểm) và đối chiếu điểm khác biệt tinh vi.
  - **Multi-Agent Consensus (3 AI Analysts + 1 Cross-Judge):** Hội đồng AI chéo đánh giá độc lập các điều khoản, sau đó hội chẩn (Consensus) để đưa ra kết luận rủi ro cuối cùng, chống ảo giác (hallucination).
- **Live Legal Grounding:** Tích hợp Brave Search API để AI tra cứu thời gian thực cơ sở dữ liệu pháp luật (vbpl.vn, chinhphu.vn, thuvienphapluat.vn) đảm bảo không trích dẫn luật đã hết hiệu lực.
- **Evaluation:** Đang xây dựng bộ Benchmark 30 Golden Legal Cases (các case pháp lý kinh điển) để CI/CD chạy script test (Precision, Recall, Legal Accuracy) mỗi lần update model.

### 3.2. Hệ thống Phần Mềm (Phụ trách: Nguyễn Đức Đạt)
- **Mô hình tổ chức:** Embedded Architecture (AI Engineer và Fullstack làm việc chung trên một codebase Squad thay vì tách rời team AI riêng).
- **Backend Core:** FastAPI, kiến trúc Clean Architecture/DDD. Database: MongoDB (lưu trữ metadata hợp đồng) / Redis (caching). API Data Contract sử dụng Pydantic V2 / OpenAPI Schema.
- **Frontend:** React 18, giao diện trực quan làm nổi bật so sánh văn bản (Visual Diff).
- **Bảo mật (Security):** Phân quyền RBAC đa cấp, cơ chế SecureLinks (link chia sẻ hợp đồng có thời hạn, tự hủy), mã hóa phân tầng để cam kết bảo mật với các Giám đốc IT (CTO). Cam kết mô hình LLM không lưu dữ liệu công ty để huấn luyện lại.

## 4. Chân Dung Khách Hàng / Stakeholders (Phụ trách quản trị: Kiều Hồng Phong)
- **Chuyên viên Sales / Mua hàng (Người dùng cuối):** Muốn giảm thiểu thời gian đọc văn bản, tìm nhanh các bẫy điều khoản, dễ dùng. (Rất ủng hộ).
- **Trưởng ban Pháp chế Doanh nghiệp (Người phê duyệt):** Thận trọng, sợ AI "ảo giác" (hallucination) trích dẫn sai luật gây hậu quả. Cần thuyết phục bằng tính năng "Human-in-the-loop: Rewrite/Approve/Reject" và Live Grounding có trích dẫn nguồn 1-click.
- **CTO / Quản lý Bảo mật:** Sợ rò rỉ dữ liệu hợp đồng thương mại mật khi đẩy qua các API bên thứ 3. Cần thuyết phục bằng Whitepaper về luồng mã hóa phân quyền.
- **Mentor (AI20K / VinUni):** Quan tâm tính đột phá kỹ thuật thuật toán và độ mượt của Multi-Agent.

## 5. Tình Trạng "Sức Khỏe" Đội Ngũ Hiện Tại (Team Health)
- **Giao tiếp & Tinh thần:** Rất tốt (4.8/5), chủ động, sẵn sàng debug xuyên đêm.
- **Tốc độ:** Chậm ở khâu kiểm thử chất lượng pháp lý (đang phải đọc dò lại từng case thủ công do chưa có script Automated Evals).
- **Kỹ thuật tồn đọng:** Thiếu đồng bộ Schema (DTO) giữa Backend Core (FastAPI) và AI Service dẫn đến tốn thời gian tích hợp; lỗi bóc tách cây cấu trúc khi gặp tài liệu PDF scan chất lượng kém.
