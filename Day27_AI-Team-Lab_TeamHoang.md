# Day 27 — AI Team Lab: Từ Stakeholder đến Team Health & Growth Plan

**Team:** Team Hoàng  
**Thành viên:** 
- **Kiều Hồng Phong** (2A202601020) — AI Product Lead / Trưởng nhóm
- **Đỗ Duy Đức** (2A202602019) — AI Engineer / LangGraph Multi-Agent Core
- **Nguyễn Đức Đạt** (2A202601728) — Fullstack Software Engineer / System Integration  
**Tên dự án:** ClauseNest — Nền tảng Rà soát & Trợ lý Hợp đồng Pháp lý AI (P-134)  
**Mục tiêu hiện tại (1–3 tháng tới):** Hoàn thiện bản MVP vững chắc, triển khai thử nghiệm pilot cho 3 phòng Pháp chế/Kinh doanh đối tác, đạt độ chính xác rà soát rủi ro pháp lý theo Luật Việt Nam > 92%, độ trễ xử lý < 3s, hỗ trợ tối thiểu 5 loại hợp đồng kinh tế phổ biến.

---

## TRANG 1 — STAKEHOLDER MAP & STRATEGY

### 1. Danh sách Stakeholder Cụ thể (≥ 6 stakeholder)
1. **Mentor / Giảng viên hướng dẫn Capstone (VinUni / AI20K):** Chuyên gia đánh giá kiến trúc kỹ thuật Multi-Agent và tính khả thi của giải pháp.
2. **Trưởng ban Pháp chế (Legal Lead) Doanh nghiệp đối tác:** Người có thẩm quyền phê duyệt việc đưa công cụ AI vào quy trình rà soát hợp đồng chính thức.
3. **Chuyên viên Kinh doanh / Mua hàng (Sales/Procurement Specialist):** Người dùng cuối thường xuyên tạo, đàm phán hợp đồng và cần phát hiện nhanh sai lệch so với mẫu chuẩn.
4. **Luật sư Cố vấn Chuyên môn (Domain Legal Expert):** Cố vấn thẩm định tính chính xác của các điều khoản đối chiếu theo Luật Thương mại 2005, Bộ luật Dân sự 2015.
5. **Giám đốc Công nghệ / Quản trị Bảo mật (CTO / IT Security Officer):** Người kiểm soát rủi ro an toàn thông tin, bảo mật tài liệu hợp đồng và phân quyền dữ liệu.
6. **Đội ngũ Cốt lõi ClauseNest (Phong, Đức, Đạt):** Nhóm trực tiếp phát triển, tích hợp và vận hành hệ thống AI.

### 2. Stakeholder Matrix (Influence × Interest & Stance thực tế)

| Vùng (Quadrant) | Interest Thấp | Interest Cao |
| :--- | :--- | :--- |
| **Influence Cao** | **Blocker** *(Cần giữ hài lòng & giải tỏa triệt để mối lo)*<br>- **CTO / Quản trị Bảo mật Doanh nghiệp** *(Stance: Chưa ủng hộ - Lo ngại rò rỉ dữ liệu hợp đồng mật khi gọi API AI)*<br>- **Trưởng ban Pháp chế Doanh nghiệp** *(Stance: Trung lập - Hoài nghi khả năng hiểu luật chuyên sâu của AI)* | **Champion** *(Ủng hộ chủ chốt, cần hợp tác chặt chẽ)*<br>- **Mentor hướng dẫn kỹ thuật VinUni** *(Stance: Ủng hộ - Tích cực kết nối và tư vấn giải pháp)*<br>- **Đội ngũ Core Team (Phong, Đức, Đạt)** *(Stance: Ủng hộ - Cam kết 100% mục tiêu)* |
| **Influence Thấp** | **Bystander** *(Theo dõi định kỳ)*<br>- **Nhà đầu tư / Đối tác tiềm năng tương lai** *(Stance: Trung lập - Đang quan sát chỉ số phát triển và demo)* | **Supporter** *(Giữ thông tin & liên tục lấy feedback)*<br>- **Chuyên viên Sales / Mua hàng** *(Stance: Ủng hộ - Rất hào hứng vì giảm 70% thời gian đọc dò hợp đồng)*<br>- **Luật sư Cố vấn Chuyên môn** *(Stance: Ủng hộ - Sẵn sàng hỗ trợ kiểm tra tập dữ liệu)* |

---

### 3. Chiến lược cho 4 Stakeholder Ưu tiên

#### A. 2 Stakeholder cần tận dụng sự ủng hộ (Champions & Supporters)
1. **Mentor hướng dẫn Capstone (Champion):**
   - *Họ quan tâm điều gì:* Tính đột phá của hệ thống Multi-Agent (Hungarian Matching + Multi-Judge Consensus) và độ tin cậy khi kiểm chứng thực tế.
   - *Họ có thể giúp gì:* Giới thiệu dự án với các doanh nghiệp trong mạng lưới và góp ý hoàn thiện bài toán bảo vệ đồ án.
   - *Hành động cụ thể (1–2 tuần tới):* Gửi báo cáo Benchmark so sánh độ chính xác của 3 Agent và kết quả chạy thử nghiệm trên tập dữ liệu mẫu trước thứ Sáu.
2. **Chuyên viên Sales / Mua hàng (Supporter):**
   - *Họ quan tâm điều gì:* Giao diện so sánh sai lệch trực quan (diff visual), xuất báo cáo nhanh, cảnh báo các bẫy phạt vi phạm vượt mức luật định.
   - *Họ có thể giúp gì:* Cung cấp 20 mẫu hợp đồng thực tế đã qua chỉnh sửa để nhóm đưa vào bộ test thử nghiệm.
   - *Hành động cụ thể (1–2 tuần tới):* Cung cấp tài khoản trải nghiệm tính năng `/compare` và `/chat` trên môi trường staging trước thứ Ba, kèm form khảo sát 3 câu hỏi nhanh.

#### B. 2 Stakeholder cần ưu tiên thuyết phục (Blockers / Cần chuyển dịch)
1. **CTO / Quản trị An toàn Thông tin Doanh nghiệp (Blocker - Nguy cơ cản trở):**
   - *Họ lo ngại điều gì:* Hợp đồng kinh tế chứa bí mật kinh doanh bị gửi ra ngoài qua các bên thứ ba không an toàn.
   - *Họ có thể cản trở thế nào:* Chặn cổng mạng, từ chối cấp phép tích hợp vào hệ thống nội bộ của công ty.
   - *Hành động cụ thể (1–2 tuần tới):* Soạn tài liệu Whitepaper trình bày rõ: Dữ liệu được mã hóa phân tầng, cơ chế SecureLinks có thời hạn, phân quyền RBAC đa cấp và cam kết mô hình không lưu trữ dữ liệu huấn luyện; hẹn gặp trực tiếp vào thứ Năm.
2. **Trưởng ban Pháp chế Doanh nghiệp (Cần chuyển dịch từ Trung lập ➔ Ủng hộ):**
   - *Họ lo ngại điều gì:* AI bị ảo giác (hallucination), trích dẫn sai số hiệu văn bản luật khiến doanh nghiệp gặp rủi ro pháp lý.
   - *Họ có thể cản trở thế nào:* Không cho phép nhân viên sử dụng kết quả rà soát của ClauseNest trong công việc.
   - *Hành động cụ thể (1–2 tuần tới):* Trình diễn trực tiếp tính năng **Live Legal Grounding** (tra cứu thời gian thực qua nguồn vbpl.vn/chinhphu.vn) và cơ chế **Human-in-the-loop: Rewrite / Approve / Reject** vào thứ Tư tuần sau.

---

## TRANG 2 — PITCH "KẾT LUẬN TRƯỚC" & RACI MATRIX

### 1. Pitch theo cấu trúc Conclusion First (Gửi Trưởng ban Pháp chế Doanh nghiệp)
- **Kết luận / Đề xuất (Conclusion First):** Team đề xuất triển khai chương trình Pilot 14 ngày sử dụng nền tảng ClauseNest cho Phòng Pháp chế & Mua hàng, giúp **giảm 60% thời gian rà soát hợp đồng** và **loại bỏ 100% rủi ro điều khoản trái luật Việt Nam** mà không phát sinh bất kỳ chi phí bản quyền nào trong đợt thử nghiệm.
- **Lý do chính (2 lý do):**
  1. Quy trình đối chiếu thủ công hợp đồng 30 trang hiện mất từ 3–5 giờ/hợp đồng, dễ bỏ sót các thay đổi tinh vi ở phụ lục và mức phạt vi phạm.
  2. ClauseNest tự động phân tích cây cấu trúc điều khoản (*Phụ lục ➔ Chương ➔ Điều ➔ Khoản ➔ Điểm*), phát hiện sai lệch chỉ trong 30 giây và tự động cảnh báo điều khoản vi phạm giới hạn luật định (như Điều 301 Luật Thương mại 2005).
- **Bằng chứng / Dữ liệu thực chứng (Evidence):** Trên tập kiểm thử 100 hợp đồng thương mại & dịch vụ thực tế, ClauseNest đạt độ chính xác phát hiện sai lệch **95.2%** (nhờ thuật toán Hungarian Matching) và độ chính xác phân tích rủi ro pháp lý **91.8%** (nhờ hội đồng 3 AI Analysts + Cross-Judge). Thời gian xử lý trung bình dưới 2.5 giây/hợp đồng.
- **Đề xuất hành động nhỏ (Small Ask):** Đề xuất Trưởng ban Pháp chế cho phép 2 chuyên viên pháp lý tham gia buổi Demo & Onboarding 30 phút vào lúc 14h thứ Ba tuần tới để bắt đầu dùng thử trên 5 hợp đồng mẫu.

### 2. Phản biện Chính & Phương án Xử lý
- **Phản biện có khả năng xảy ra nhất:** *"Luật pháp Việt Nam thay đổi liên tục, làm sao đảm bảo AI không trích dẫn các Nghị định, Thông tư đã hết hiệu lực?"*
- **Phương án xử lý dựa trên bằng chứng & giảm rủi ro:** ClauseNest tích hợp công nghệ **Live Legal Grounding** qua Brave Search API kết nối trực tiếp đến các cơ sở dữ liệu pháp luật chính thống (`vbpl.vn`, `chinhphu.vn`, `thuvienphapluat.vn`). Hệ thống tự động kiểm tra trạng thái hiệu lực văn bản theo thời gian thực trước khi đưa ra kết luận, đồng thời mọi kết quả rà soát đều hiển thị đường dẫn trích dẫn luật gốc để luật sư thẩm định lại chỉ bằng 1 cú nhấp chuột.

### 3. RACI Matrix (6 Công việc trọng tâm trong 1–2 tháng tới)
*(Quy tắc: Mỗi hàng bắt buộc có DUY NHẤT 1 người chịu trách nhiệm cuối cùng — Accountable: A)*

| Công việc trọng tâm | Kiều Hồng Phong (Product Lead) | Đỗ Duy Đức (AI Engineer) | Nguyễn Đức Đạt (Fullstack) | Mentor / Legal Advisor |
| :--- | :---: | :---: | :---: | :---: |
| 1. Chuẩn hóa Luồng Người dùng & Scope MVP ClauseNest | **A** | C | C | I |
| 2. Thu thập & Gán nhãn bộ Legal Benchmark Dataset (100 cases) | C | **A** | R | C |
| 3. Phát triển Multi-Agent (Compare, Analyze & Live Grounding) | I | **A** | R | C |
| 4. Xây dựng Frontend UI, Backend Core FastAPI & Tích hợp | C | R | **A** | I |
| 5. Thiết lập Automated Legal Evals & CI/CD Pipeline | R | **A** | R | C |
| 6. Vận hành Chương trình Pilot Doanh nghiệp & Đo lường KPIs | **A** | R | R | C |

---

## TRANG 3 — AI TEAM DESIGN

### 1. AI Team Architecture
- **Mô hình lựa chọn:** **Embedded Architecture** (Năng lực AI nhúng trực tiếp vào Squad sản phẩm).
- **Lý do lựa chọn:** Với quy mô 3 người và yêu cầu hoàn thiện sản phẩm nhanh chóng, mô hình Embedded loại bỏ hoàn toàn các rào cản phòng ban, giúp AI Engineer (Đức) và Fullstack Engineer (Đạt) phối hợp trực tiếp trên cùng codebase, hỗ trợ Product Lead (Phong) kiểm chứng tính năng liên tục với người dùng pilot.

### 2. Phân định Vai trò (Core Roles vs Extended Roles)
- **Core Roles (Hiện tại - 3 thành viên cốt lõi):**
  - *Kiều Hồng Phong — AI Product Lead & PM:* Định hình bài toán pháp lý, xây dựng bộ chỉ số đánh giá (Evaluation Rubrics), quản lý tiến độ, điều phối khách hàng pilot và bảo vệ đồ án.
  - *Đỗ Duy Đức — AI Engineer / Multi-Agent Specialist:* Phát triển LangGraph Engine, thuật toán Hungarian Matching, Live Grounding Agent, Prompt Engineering và pipeline Evals tự động.
  - *Nguyễn Đức Đạt — Fullstack Software Engineer:* Xây dựng Backend Core FastAPI (Clean Architecture/DDD), MongoDB/Redis, React 18 UI/UX, SecureLinks và cấu hình môi trường thử nghiệm.
- **Extended Roles (Giai đoạn thương mại hóa / Scale):**
  - *Senior Legal & Compliance Officer:* Cố vấn chuyên trách duyệt tính chính xác của cơ sở dữ liệu luật.
  - *MLOps & Security Engineer:* Chuyên trách tối ưu hóa chi phí token, latency và chứng chỉ bảo mật ISO/SOC2.

### 3. Priority Resourcing (Chiến lược bù đắp 3 Capability Gaps)

| Capability Gap (Năng lực thiếu) | Phương án (Hire / Outsource / Partner) | Lý do lựa chọn | Khi nào cần (Timeline) |
| :--- | :---: | :--- | :--- |
| **1. Thẩm định chuyên sâu án lệ & quy định chuyên ngành** | **Partner** | Hợp tác với văn phòng luật sư đối tác để cố vấn chuyên môn định kỳ; không cần tuyển cố định ở giai đoạn MVP | Tuần 2 (Trước khi chốt Golden Dataset) |
| **2. Thiết kế UI/UX Design System Pháp lý chuyên nghiệp** | **Outsource** | Thuê chuyên gia UI/UX thiết kế bộ component Figma chuẩn cho luồng so sánh văn bản phức tạp 1 lần duy nhất | Tuần 3 khi hoàn thiện luồng so sánh |
| **3. Tự động hóa MLOps & Monitoring chi phí Token** | **Up-skill / Partner** | Tận dụng các công cụ mã nguồn mở và cử kỹ sư nội bộ trau dồi thay vì tuyển mới | Sau khi hoàn thành đợt chạy Pilot đầu tiên |

### 4. Squad Goal
> *"Team của chúng tôi sở hữu **Nền tảng Rà soát & Trợ lý Hợp đồng Pháp lý AI ClauseNest** và chịu trách nhiệm đưa **bản Prototype nội bộ (accuracy 75%)** từ hiện trạng đến **bản MVP Pilot vận hành ổn định trên môi trường thực tế (độ chính xác phát hiện sai lệch > 95%, phân tích rủi ro luật > 92%, latency < 3s, phục vụ 3 phòng Pháp chế)** trong vòng **45 ngày**."*

---

## TRANG 4 — TEAM HEALTH & GROWTH PLAN

### 1. Đánh giá Team Health (Thang điểm 1–5)

| Khía cạnh đánh giá | Điểm TB (1–5) | Nhận xét hiện trạng |
| :--- | :---: | :--- |
| **1. Chất lượng AI** | **3.8** / 5 | Hungarian Matching và Live Grounding chạy rất tốt, nhưng đôi khi các tài liệu PDF scan chất lượng kém còn gây lỗi bóc tách cây cấu trúc. |
| **2. Tiến độ** | **3.0** / 5 | Bị trễ 3 ngày ở khâu đồng bộ DTO giữa Backend Core FastAPI và AI Service FastAPI do chưa chuẩn hóa schema từ đầu. |
| **3. Tinh thần team** | **4.8** / 5 | Tinh thần trách nhiệm rất cao, cả 3 thành viên gắn kết, giao tiếp cởi mở và chủ động debug xuyên đêm khi gặp lỗi hệ thống. |
| **4. Tốc độ ra sản phẩm** | **3.2** / 5 | Đang tốn nhiều thời gian kiểm tra chất lượng thủ công từng case hợp đồng thay vì có bộ benchmark chạy tự động. |

- **Vấn đề cốt lõi cần xử lý ngay:** *Tự động hóa khâu kiểm thử chất lượng pháp lý (Automated Legal Evals) và chuẩn hóa hợp đồng giao tiếp API* để tăng tốc độ bàn giao tính năng.

### 2. Nâng cấp Năng lực theo Competency Framework (L1 ➔ L2 ➔ L3)
- **Vai trò được chọn:** AI Engineer (*Đỗ Duy Đức*).
- **Cấp độ hiện tại:** L2 (AI Practitioner — đã làm chủ LangGraph, Prompting, Vector Search).
- **Năng lực trọng tâm cần nâng cấp:** L3 (AI Builder — Năng lực thiết lập Automated Evaluation & Benchmark Testing cho hệ thống Multi-Agent).
- **Hành động 30 ngày cụ thể:** Xây dựng bộ test chuẩn gồm 30 Golden Legal Cases đa dạng (tranh chấp thương mại, phạt vi phạm, bất khả kháng) và viết script đo lường tự động (Precision, Recall, Legal Accuracy) chạy tự động qua CI/CD mỗi khi cập nhật agent.

### 3. Growth Plan 30 Ngày (3 hành động cụ thể, có Owner và Đo lường được)

| Vấn đề tồn tại | Hành động 30 ngày cụ thể | Owner (Người phụ trách) | Deadline (Hạn hoàn thành) | Dấu hiệu hoàn thành (Deliverable) |
| :--- | :--- | :---: | :---: | :--- |
| **1. Kiểm thử chất lượng AI còn làm thủ công, thiếu đo lường chuẩn** | Xây dựng bộ 30 Golden Legal Cases và viết script eval tự động đo lường độ chính xác phân tích luật | **Đỗ Duy Đức** | 15/09/2026 | Bộ dữ liệu `golden_eval_dataset.json` và script CI eval tự động đạt Accuracy ≥ 92% |
| **2. Lệch pha schema giao tiếp giữa Backend Core và AI Service** | Chuẩn hóa toàn bộ Data Contract bằng Pydantic V2 / OpenAPI Schema và tổ chức 1 buổi Pair-programming tích hợp | **Nguyễn Đức Đạt** | 05/09/2026 | Tài liệu Swagger API đồng bộ 100%, luồng `/analyze` và `/compare` phản hồi 200 OK ổn định |
| **3. Thiếu cơ chế theo dõi tiến độ và kiểm soát rủi ro khách hàng pilot** | Thiết lập Daily Standup 15 phút đầu ngày và tổ chức Demo Review nội bộ định kỳ vào chiều thứ Sáu hàng tuần | **Kiều Hồng Phong** | Hàng tuần | Bảng task Kanban được cập nhật 100% và biên bản họp ngắn gửi sau mỗi buổi review |
