# BẢN KẾ HOẠCH CHI TIẾT THỰC HIỆN BÀI LAB DAY 27 (AI TEAM LAB)

> **Dự án thực tế:** ClauseNest — Nền tảng Rà soát & Trợ lý Hợp đồng Pháp lý AI (P-134)  
> **Đội ngũ (Team Hoàng):**
> 1. **Kiều Hồng Phong** - 2A202601020 (AI Product Lead / Trưởng nhóm)
> 2. **Đỗ Duy Đức** - 2A202602019 (AI Engineer / LangGraph Multi-Agent Core)
> 3. **Nguyễn Đức Đạt** - 2A202601728 (Fullstack Software Engineer / System Integration)

---

## PHẦN 1: PHÂN CÔNG NHIỆM VỤ 3 THÀNH VIÊN

### 1. Kiều Hồng Phong (Trưởng nhóm / AI Product Lead)
- **Nhiệm vụ chính:** Quản trị chung, chủ trì Phase 0 & Phase 1, soạn thảo bài Pitch (Phase 2), điều phối họp định kỳ (Phase 4), kiểm tra chéo và nộp link bài đại diện cho nhóm (Phase 5).
- **Trách nhiệm đầu ra:** Chốt phạm vi dự án trong `README.md`, chủ trì Trang 1 (Stakeholder Map & Strategy), phối hợp viết Trang 2 (Pitch).

### 2. Đỗ Duy Đức (AI Engineer)
- **Nhiệm vụ chính:** Phụ trách toàn bộ dữ liệu kỹ thuật AI, thuật toán Hungarian Matching, Live Legal Grounding (Brave Search API), chỉ số đo lường độ chính xác và khung đánh giá chất lượng (Evals).
- **Trách nhiệm đầu ra:** Cung cấp số liệu bằng chứng cho bài Pitch (Trang 2), phụ trách Core AI Roles & MLOps (Trang 3), chủ trì phần Competency L1➔L2➔L3 & xây dựng bộ 30 Golden Cases (Trang 4).

### 3. Nguyễn Đức Đạt (Fullstack Software Engineer)
- **Nhiệm vụ chính:** Phụ trách kiến trúc hệ thống FastAPI Core, React 18 UI, phân quyền RBAC/SecureLinks, chiến lược Resourcing và căn chỉnh file PDF đúng 4 trang.
- **Trách nhiệm đầu ra:** Phản biện bài Pitch & rà soát bảng RACI (Trang 2), chủ trì Priority Resourcing (Trang 3), phụ trách chuẩn hóa OpenAPI/Swagger (Trang 4), xuất file `Day27_AI-Team-Lab_TeamHoang.pdf`.

---

## PHẦN 2: LỊCH TRÌNH THỰC HIỆN TỪNG BƯỚC (120 PHÚT)

| Mốc thời gian | Giai đoạn (Phase) | Hình thức | Nội dung thực hiện | Người chủ trì |
| :---: | :--- | :---: | :--- | :---: |
| **00:00 – 00:05** (5') | **Phase 0: Scope & Ground Rules** | Team | Chốt phạm vi ClauseNest, mục tiêu 1–3 tháng, hoàn thiện `README.md` | **Phong** |
| **00:05 – 00:25** (20') | **Phase 1: Stakeholder Map & Strategy** | Cá nhân ➔ Team | List ≥ 6 Stakeholders cụ thể, ma trận Influence × Interest, 4 chiến lược | **Phong** |
| **00:25 – 00:55** (30') | **Phase 2: Pitch & RACI Matrix** | Team ➔ Cá nhân ➔ Team | Pitch Conclusion First gửi Trưởng ban Pháp chế, xử lý 1 phản biện, RACI (1 A/hàng) | **Đức & Phong** |
| **00:55 – 01:20** (25') | **Phase 3: AI Team Design** | Team | Embedded Architecture, Core Roles, 3 Resourcing Gaps, Squad Goal | **Đạt & Đức** |
| **01:20 – 01:45** (25') | **Phase 4: Team Health & Growth Plan** | Cá nhân ➔ Team | Đánh giá 4 khía cạnh, nâng cấp Competency L1➔L2➔L3, 3 Actions 30 ngày | **Cả 3 người** |
| **01:45 – 02:00** (15') | **Phase 5: Soi lỗi & Nộp bài** | Team & Lead | Kiểm tra 3 liên kết nhất quán, xuất PDF đúng 4 trang, commit, push & nộp link | **Phong & Đạt** |

---

## PHẦN 3: NỘI DUNG CHI TIẾT 4 TRANG CỦA BÀI LÀM (FILE PDF)

### 📄 TRANG 1 — STAKEHOLDER MAP & STRATEGY

#### 1. Danh sách 6 Stakeholder cụ thể
1. **Mentor / Giảng viên hướng dẫn Capstone (VinUni / AI20K):** Đánh giá kiến trúc kỹ thuật Multi-Agent và tính khả thi của giải pháp.
2. **Trưởng ban Pháp chế Doanh nghiệp đối tác:** Người có thẩm quyền duyệt đưa ClauseNest vào quy trình rà soát hợp đồng.
3. **Chuyên viên Kinh doanh / Mua hàng (Sales/Procurement):** Người dùng cuối cần phát hiện nhanh sai lệch so với mẫu chuẩn.
4. **Luật sư Cố vấn Chuyên môn:** Thẩm định tính chính xác của các điều khoản đối chiếu theo Luật Thương mại 2005, Bộ luật Dân sự 2015.
5. **CTO / Quản trị An toàn Thông tin:** Kiểm soát rủi ro bảo mật tài liệu và phân quyền dữ liệu.
6. **Đội ngũ Cốt lõi ClauseNest (Phong, Đức, Đạt):** Trực tiếp phát triển, tích hợp và vận hành hệ thống.

#### 2. Ma trận Phân loại (Influence × Interest & Stance thực tế)
- **Champion (Influence Cao - Interest Cao | Stance: Ủng hộ):** Mentor hướng dẫn Capstone, Core Team (Phong, Đức, Đạt).
- **Blocker (Influence Cao - Interest Thấp | Stance: Cần thuyết phục):** CTO / Quản trị An toàn Thông tin *(lo ngại rò rỉ dữ liệu mật khi gọi API)*, Trưởng ban Pháp chế *(hoài nghi AI hiểu luật)*.
- **Supporter (Influence Thấp - Interest Cao | Stance: Ủng hộ):** Chuyên viên Sales/Mua hàng *(hào hứng vì giảm 70% thời gian đọc dò)*, Luật sư Cố vấn Chuyên môn.
- **Bystander (Influence Thấp - Interest Thấp | Stance: Trung lập):** Nhà đầu tư / Đối tác tiềm năng tương lai.

#### 3. 4 Chiến lược cho 4 Stakeholder ưu tiên
1. **Mentor hướng dẫn (Champion):** Gửi báo cáo Benchmark so sánh độ chính xác của 3 Agent và kết quả chạy thử nghiệm trên tập dữ liệu mẫu trước thứ Sáu để nhờ kết nối doanh nghiệp pilot.
2. **Chuyên viên Sales/Mua hàng (Supporter):** Cung cấp tài khoản trải nghiệm tính năng `/compare` và `/chat` trên staging trước thứ Ba, thu thập phản hồi trên 20 mẫu hợp đồng thực tế.
3. **CTO / Quản trị An toàn Thông tin (Blocker):** Soạn tài liệu Whitepaper mô tả mã hóa phân tầng, cơ chế SecureLinks có thời hạn, phân quyền RBAC đa cấp và cam kết không lưu dữ liệu huấn luyện; hẹn gặp thứ Năm.
4. **Trưởng ban Pháp chế (Cần chuyển dịch):** Trình diễn trực tiếp tính năng Live Legal Grounding qua vbpl.vn/chinhphu.vn và cơ chế Human-in-the-loop (Rewrite / Approve / Reject) vào thứ Tư tuần tới.

---

### 📄 TRANG 2 — PITCH "KẾT LUẬN TRƯỚC" & RACI MATRIX

#### 1. Pitch theo cấu trúc Conclusion First (Gửi Trưởng ban Pháp chế Doanh nghiệp)
- **Kết luận / Đề xuất (Conclusion First):** Team đề xuất triển khai chương trình Pilot 14 ngày sử dụng nền tảng ClauseNest cho Phòng Pháp chế & Mua hàng, giúp **giảm 60% thời gian rà soát hợp đồng** và **loại bỏ 100% rủi ro điều khoản trái luật Việt Nam** mà không phát sinh bất kỳ chi phí bản quyền nào trong đợt thử nghiệm.
- **Lý do chính:**
  1. Quy trình đối chiếu thủ công hợp đồng 30 trang hiện mất từ 3–5 giờ/hợp đồng, dễ bỏ sót các thay đổi tinh vi ở phụ lục và mức phạt vi phạm.
  2. ClauseNest tự động bóc tách cây cấu trúc (*Phụ lục ➔ Chương ➔ Điều ➔ Khoản ➔ Điểm*), phát hiện sai lệch trong 30 giây và tự động cảnh báo điều khoản trái luật (như phạt vi phạm vượt quá 8% theo Điều 301 Luật Thương mại 2005).
- **Bằng chứng (Evidence):** Trên tập kiểm thử 100 hợp đồng thực tế, ClauseNest đạt độ chính xác phát hiện sai lệch **95.2%** (nhờ Hungarian Matching) và độ chính xác rà soát rủi ro pháp lý **91.8%** (nhờ 3 AI Analysts + Cross-Judge). Thời gian xử lý trung bình dưới 2.5 giây/hợp đồng.
- **Đề xuất hành động nhỏ (Small Ask):** Đề xuất Trưởng ban Pháp chế cho phép 2 chuyên viên pháp lý tham gia buổi Onboarding 30 phút vào 14h thứ Ba tuần tới để dùng thử trên 5 hợp đồng mẫu.

#### 2. Phản biện Chính & Phương án Xử lý
- **Phản biện:** *"Luật pháp thay đổi liên tục, làm sao đảm bảo AI không trích dẫn các văn bản đã hết hiệu lực?"*
- **Phương án xử lý:** ClauseNest tích hợp **Live Legal Grounding** qua Brave Search API kết nối trực tiếp cơ sở dữ liệu pháp luật chính thống (`vbpl.vn`, `chinhphu.vn`, `thuvienphapluat.vn`), tự động kiểm tra trạng thái hiệu lực theo thời gian thực và hiển thị đường dẫn trích dẫn luật gốc 1-click.

#### 3. RACI Matrix (Mỗi hàng DUY NHẤT 1 chữ A)
| Công việc trọng tâm | Kiều Hồng Phong (Product Lead) | Đỗ Duy Đức (AI Engineer) | Nguyễn Đức Đạt (Fullstack) | Mentor / Legal Advisor |
| :--- | :---: | :---: | :---: | :---: |
| 1. Chuẩn hóa Luồng Người dùng & Scope MVP ClauseNest | **A** | C | C | I |
| 2. Thu thập & Gán nhãn bộ Legal Benchmark Dataset (100 cases) | C | **A** | R | C |
| 3. Phát triển Multi-Agent (Compare, Analyze & Live Grounding) | I | **A** | R | C |
| 4. Xây dựng Frontend UI, Backend Core FastAPI & Tích hợp | C | R | **A** | I |
| 5. Thiết lập Automated Legal Evals & CI/CD Pipeline | R | **A** | R | C |
| 6. Vận hành Chương trình Pilot Doanh nghiệp & Đo lường KPIs | **A** | R | R | C |

---

### 📄 TRANG 3 — AI TEAM DESIGN

#### 1. AI Team Architecture
- **Mô hình lựa chọn:** **Embedded Architecture** (Năng lực AI nhúng trực tiếp vào Squad sản phẩm).
- **Lý do lựa chọn:** Với quy mô 3 người và yêu cầu hoàn thiện sản phẩm nhanh chóng, mô hình Embedded loại bỏ rào cản phòng ban, giúp AI Engineer (Đức) và Fullstack Engineer (Đạt) phối hợp trực tiếp trên cùng codebase, hỗ trợ Product Lead (Phong) kiểm chứng tính năng liên tục với người dùng.

#### 2. Phân định Vai trò (Core Roles vs Extended Roles)
- **Core Roles (3 người):**
  - *Kiều Hồng Phong — AI Product Lead & PM:* Định hình bài toán, xây dựng rubric đánh giá, quản lý tiến độ, điều phối pilot.
  - *Đỗ Duy Đức — AI Engineer:* Phát triển LangGraph Engine, Hungarian Matching, Live Grounding, Prompting, Evals tự động.
  - *Nguyễn Đức Đạt — Fullstack Software Engineer:* Xây dựng Backend Core FastAPI, MongoDB/Redis, React 18 UI/UX, SecureLinks và cấu hình môi trường thử nghiệm.
- **Extended Roles (Giai đoạn scale):** Senior Legal Specialist (thẩm định dữ liệu luật), MLOps & Security Engineer (tối ưu token, latency, chứng chỉ ISO/SOC2).

#### 3. Priority Resourcing (Xử lý 3 Capability Gaps)
| Capability Gap | Phương án | Lý do lựa chọn | Timeline |
| :--- | :---: | :--- | :--- |
| **1. Thẩm định án lệ & quy định chuyên ngành** | **Partner** | Hợp tác với văn phòng luật sư đối tác cố vấn định kỳ; không cần tuyển full-time giai đoạn MVP | Tuần 2 (trước khi chốt Golden Dataset) |
| **2. Thiết kế UI/UX Visual Diff chuyên nghiệp** | **Outsource** | Thuê chuyên gia thiết kế bộ UI Kit/Figma chuẩn 1 lần để tiết kiệm chi phí cố định | Tuần 3 khi xong luồng so sánh |
| **3. Tự động hóa MLOps & Giám sát Token** | **Up-skill / Partner** | Tận dụng các công cụ mã nguồn mở và cử kỹ sư nội bộ trau dồi thay vì tuyển mới | Sau khi chạy Pilot đợt 1 |

#### 4. Squad Goal
> *"Team của chúng tôi sở hữu **Nền tảng Rà soát & Trợ lý Hợp đồng Pháp lý AI ClauseNest** và chịu trách nhiệm đưa **bản Prototype nội bộ (accuracy 75%)** từ hiện trạng đến **bản MVP Pilot vận hành ổn định trên môi trường thực tế (độ chính xác phát hiện sai lệch > 95%, phân tích rủi ro luật > 92%, latency < 3s, phục vụ 3 phòng Pháp chế)** trong vòng **45 ngày**."*

---

### 📄 TRANG 4 — TEAM HEALTH & GROWTH PLAN

#### 1. Đánh giá Team Health (Thang điểm 1–5)
- **Chất lượng AI:** **3.8** / 5 (Hungarian Matching & Live Grounding tốt; cần tối ưu OCR với tài liệu PDF scan mờ).
- **Tiến độ:** **3.0** / 5 (Trễ 3 ngày khâu đồng bộ DTO giữa Backend Core và AI Service do chưa chuẩn hóa schema ban đầu).
- **Tinh thần team:** **4.8** / 5 (Gắn kết, minh bạch, chủ động debug xuyên đêm giải quyết bài toán khó).
- **Tốc độ ra sản phẩm:** **3.2** / 5 (Tốn nhiều thời gian kiểm thử thủ công từng case hợp đồng thay vì có bộ eval tự động).
- **Vấn đề cốt lõi cần xử lý:** Tự động hóa khâu kiểm thử chất lượng pháp lý (Automated Legal Evals) và chuẩn hóa API Data Contract.

#### 2. Nâng cấp Năng lực theo Competency Framework (L1 ➔ L2 ➔ L3)
- **Vai trò:** AI Engineer (*Đỗ Duy Đức*).
- **Cấp độ hiện tại:** L2 (AI Practitioner).
- **Năng lực trọng tâm cần nâng:** L3 (AI Builder — Thiết lập Automated Evaluation & Benchmark Testing cho Multi-Agent).
- **Hành động 30 ngày cụ thể:** Xây dựng bộ test chuẩn gồm 30 Golden Legal Cases đa dạng (tranh chấp thương mại, phạt vi phạm, bất khả kháng) và viết script đo lường tự động (Precision, Recall, Legal Accuracy) chạy qua CI/CD mỗi khi cập nhật agent.

#### 3. Growth Plan 30 Ngày (3 hành động cụ thể có Owner)
| Vấn đề | Hành động 30 ngày cụ thể | Owner | Deadline | Dấu hiệu hoàn thành (Deliverable) |
| :--- | :--- | :---: | :---: | :--- |
| **1. Kiểm thử AI còn thủ công, thiếu đo lường** | Xây dựng bộ 30 Golden Legal Cases và viết script eval tự động đo lường độ chính xác phân tích luật | **Đỗ Duy Đức** | 15/09/2026 | File `golden_eval_dataset.json` và script CI eval tự động đạt Accuracy ≥ 92% |
| **2. Lệch pha schema giữa Backend Core và AI Service** | Chuẩn hóa Data Contract bằng Pydantic V2 / OpenAPI Schema và tổ chức 1 buổi Pair-programming tích hợp | **Nguyễn Đức Đạt** | 05/09/2026 | Tài liệu Swagger API đồng bộ 100%, endpoint `/analyze` và `/compare` phản hồi 200 OK |
| **3. Thiếu cơ chế theo dõi tiến độ và rủi ro pilot** | Thiết lập Daily Standup 15 phút đầu ngày và tổ chức Demo Review nội bộ định kỳ vào chiều thứ Sáu hàng tuần | **Kiều Hồng Phong** | Hàng tuần | Bảng task Kanban được cập nhật 100% và biên bản họp ngắn gửi sau mỗi buổi review |

---

## PHẦN 4: HƯỚNG DẪN KIỂM TRA CHÉO & NỘP BÀI

### 1. Kiểm tra 3 liên kết nhất quán (Gate 5 Check)
1. **Trang 1 ➔ Trang 2:** Trưởng ban Pháp chế (người cần thuyết phục ở Trang 1) là người nhận bài Pitch ở Trang 2.
2. **Trang 3 ➔ Trang 4:** Capability Gap về kiểm thử tự động ở Trang 3 khớp trực tiếp với vấn đề tốc độ và Competency cần nâng của AI Engineer ở Trang 4.
3. **Trang 2 ➔ Trang 4:** Owner trong Growth Plan Trang 4 (Đức, Đạt, Phong) khớp chính xác với vai trò chịu trách nhiệm (A) trong RACI Trang 2.

### 2. Nộp bài
1. Xuất nội dung 4 trang trên ra file: **`Day27_AI-Team-Lab_TeamHoang.pdf`** (tối đa đúng 4 trang).
2. Đặt file PDF vào thư mục gốc của repository.
3. Trưởng nhóm **Kiều Hồng Phong** đẩy code lên GitHub và nộp đường dẫn repository: `https://github.com/VinAIThucChien-Lab/Track1-Day27-TeamHoang`.
