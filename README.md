# VinGlucare Agent — Day 22 Monetization Lab

**Học viên:** Lê Thanh Tình  
**Dự án:** P-147 — VinGlucare Agent  
**Sản phẩm:** AI Agent hỗ trợ người bệnh đái tháo đường tuýp 2 quản lý thuốc, đường huyết và lối sống tại nhà; đồng thời cung cấp dữ liệu theo dõi có cấu trúc cho bác sĩ.

## Hồ sơ nộp bài

- [LeThanhTinh_Day22_model.xlsx](./LeThanhTinh_Day22_model.xlsx): mô hình Cost/Job, pricing, Value Metric, channel fit, kế hoạch 90 ngày và Evidence Pack.
- [LeThanhTinh_Day22_onepager.pdf](./LeThanhTinh_Day22_onepager.pdf): Monetization One-Pager, một trang.

## 1. Khách hàng, ngân sách và Job

Khách hàng mục tiêu là phòng khám nội tiết quy mô SMB. Khoản chi trả đến từ ngân sách vận hành/chăm sóc bệnh mạn tính; người phê duyệt dự kiến là Trưởng phòng khám hoặc Giám đốc vận hành, phối hợp với IT và đơn vị phụ trách bảo vệ dữ liệu.

**Định nghĩa một Job:** một bệnh nhân hoạt động hoàn tất một tháng theo dõi — ghi dữ liệu ít nhất 14 ngày, nhận nhắc thuốc và có bản tóm tắt tháng cho bác sĩ.

VinGlucare không chẩn đoán, thay đổi thuốc/liều, dự đoán biến chứng hoặc xử lý tình huống cấp cứu.

## 2. Value Metric và Pricing

Mô hình được chọn là **Hybrid**:

- Phí nền: **$100/phòng khám/tháng** cho dashboard, onboarding và support.
- Phí usage: **$2,50/bệnh nhân hoạt động/tháng**.

Scorecard hiện tại:

- Attribution: **5/10**.
- Autonomy: **7/10**.

VinGlucare chưa sử dụng outcome pricing vì hiện mới có log và mục tiêu eval kỹ thuật, chưa đủ bằng chứng để quy kết kết quả lâm sàng cho AI.

Benchmark tham khảo:

- DarioHealth B2B sử dụng mô hình PMPM/PEMPM.
- Dario Diabetes Success Plan công bố các gói $20, $25 và $70 mỗi thành viên/tháng.

## 3. Unit Economics

| Chỉ số | Giá trị |
|---|---:|
| Cost/Job | **$0,830** |
| Giá sàn 3× Cost/Job | **$2,489** |
| Giá usage đề xuất | **$2,50** |
| Gross Margin | **66,8%** |
| Containment hiện tại | **80% — ước tính trước pilot** |
| Containment tối thiểu để GM ≥ 60% | **66,4%** |
| Ngưỡng khiến GM dưới 50% | **Containment < 53,1%** |

Cost/Job bao gồm LLM, hạ tầng, retry và QA nội bộ; mẫu số là số Job hoàn thành, không phải số Job đã thử. Các giả định chính gồm 1.000 Job thử/tháng, 800 Job hoàn thành, retry 8% và QA 20% số ca.

Giá GPT-4o mini được kiểm tra ngày **08/10/2026**:

- Input: $0,15/1M token.
- Cached input: $0,075/1M token.
- Output: $0,60/1M token.

## 4. Go-to-Market

Kênh duy nhất trong 90 ngày đầu là **Partner-Led**, với đối tác mục tiêu:

> Phòng khám Nội tiết — Bệnh viện Đa khoa Quốc tế Vinmec Central Park.

Trạng thái hiện tại: **chưa liên hệ**. Kế hoạch được xem là không đạt nếu trong 14 ngày không tìm được một sponsor và ít nhất 10 bệnh nhân đồng ý thử nghiệm.

Pain Moment: từ **20:00–22:00 sau bữa tối**, người bệnh đo đường huyết, kiểm tra thuốc và thường sử dụng Zalo; bác sĩ cần dữ liệu có cấu trúc trước buổi tái khám.

Điểm nhúng đề xuất:

- Zalo Official Account dẫn vào PWA.
- QR onboarding tại quầy khám.
- Dashboard VinGlucare trong quy trình chuẩn bị tái khám của bác sĩ.

### Kiểm tra khả năng chi trả cho kênh

| Chỉ số | Giá trị |
|---|---:|
| ARPU | **$600/tháng** |
| ACV | **$7.200/năm** |
| Ngân sách CAC | **$4.811/khách hàng** |
| CAC sales-led ước tính | **$25.200/khách hàng** |
| Chênh lệch | **5,24× ngân sách CAC** |
| Deal/AE/ngày | **0,278** |

Sales-led khả thi về số deal nhưng chưa khả thi về CAC, vì vậy chưa tuyển đội sales trong giai đoạn đầu.

## 5. Kế hoạch 90 ngày

### Tháng 1 — Học

- Phỏng vấn 5 bệnh nhân và 2 bác sĩ.
- Tuyển 10 người dùng thử.
- Đo token, containment, thời gian QA và baseline an toàn.
- KPI: ít nhất 7/10 người kích hoạt; không có lỗi an toàn nghiêm trọng.
- Owner: Lê Thanh Tình.

### Tháng 2–3 — Pilot

- Pilot 8 tuần tại một phòng khám với 20–50 bệnh nhân.
- KPI: WAU ≥ 60%, containment ≥ 80%, citation ≥ 85%, NPS ≥ 30.
- Owner: Lê Thanh Tình và Trần Xuân Đức.

### Tháng 4+ — Mở rộng

- Mở rộng lên 3 phòng khám và 200 bệnh nhân hoạt động.
- Hoàn thiện playbook triển khai, DPA và case study.
- KPI: ít nhất 2 LOI; partner CAC không vượt $4.811.
- Owner: Lê Thanh Tình và Phạm Long Nhật.

## 6. Evidence Pack

| Tài sản | Trạng thái | Người phụ trách | Deadline |
|---|---|---|---|
| Eval Results: 50 câu và 30 prompt nguy hiểm; citation, faithfulness, containment, severity | Chưa có | Phạm Long Nhật | 15/10/2026 |
| Risk Checklist: hallucination, data training, encryption, retention/deletion, incident response, giới hạn không chẩn đoán | Bản nháp | Trần Xuân Đức | 17/10/2026 |
| Pilot Report 8 tuần: enrollment, WAU, adherence, containment, safety và thời gian bác sĩ tiết kiệm | Chưa có | Lê Thanh Tình | 15/12/2026 |

## Lưu ý về số liệu

Các con số về volume, containment, token, QA, ARPU, CAC và giá trị tiết kiệm là giả định phục vụ mô hình ban đầu. Chúng phải được thay bằng log sử dụng, hóa đơn hạ tầng, time-study và kết quả pilot trước khi dùng trong hợp đồng hoặc tuyên bố hiệu quả lâm sàng.

