1. User EU 
- Không có user EU sử dụng ứng dụng 
Trong phần Problem Statement và Target User, bạn xác định rất rõ đối tượng khách hàng là:

Vị trí địa lý: Người học tiếng Trung tại Việt Nam.

Quốc tịch/Đặc điểm: Người đi làm Việt Nam (Vietnamese professional).

Bối cảnh sử dụng: Giao thương, công việc tại Việt Nam hoặc với đối tác Trung Quốc.

=> Kết luận: Người dùng tại EU (Liên minh Châu Âu) không nằm trong tệp khách hàng ưu tiên (Primary Target) của giai đoạn MVP và gọi vốn Seed này.

2. Dữ liệu Việt Nam 
- Dữ liệu cá nhân của người dùng Việt Nam (họ tên, số điện thoại, giọng nói, lịch sử hội thoại) phải được lưu trữ bản gốc tại Việt Nam.
- Có chuyển dữ liệu ra nước ngoài bằng AI trung quốc. Qwen 2 của alibaba và STT/TTS của Azure/ElevenLabs
Dựa trên quy định pháp luật Việt Nam hiện hành (đặc biệt là Nghị định 13/2023/NĐ-CP và các văn bản hướng dẫn tính đến năm 2026), dự án ChinTalk AI của bạn BẮT BUỘC phải thực hiện đánh giá tác động và các thủ tục pháp lý sau:
Các thủ tục PDPL cụ thể ChinTalk AI phải áp dụng:
- Lập hồ sơ Đánh giá tác động xử lý dữ liệu cá nhân (DPIA) nội địa
- Cơ chế "Consent" (Đồng ý) đặc biệt cho dữ liệu nhạy cảm
- Chỉ định nhân sự bảo vệ dữ liệu

3. Tầng rủi ro Luật AI VN 
Đây là AI giáo dục nên mức độ rủi ro Cao. 
# Phân tích Tuân thủ Pháp lý ChinTalk AI (Thị trường Việt Nam 2026)

Dựa trên hồ sơ dự án **ChinTalk AI** và các quy định pháp luật mới nhất (Luật Bảo vệ dữ liệu cá nhân - PDPL và Luật Trí tuệ nhân tạo - Luật số 134/2025/QH15), dưới đây là bản tóm tắt các nghĩa vụ pháp lý trọng yếu cần thực hiện.

## 1. Phân tầng Rủi ro theo Luật AI Việt Nam (Hiệu lực 1/3/2026)
Dự án được xác định nằm ở **Tầng TRUNG BÌNH**.

* **Lý do:** Là hệ thống AI tạo nội dung (Chatbot), có khả năng gây nhầm lẫn nếu người dùng không được thông báo. 
* **Nghĩa vụ chính:**
    * **Dán nhãn AI:** Mọi phản hồi (văn bản và giọng nói) phải đi kèm thông báo rõ ràng: *"Nội dung được tạo bởi AI"*.
    * **Thông báo Bộ KH&CN:** Thực hiện thủ tục thông báo vận hành hệ thống AI theo quy định.
    * **Lưu ý:** Tránh định vị sản phẩm là "Hệ thống giáo dục chính quy" để không bị kéo lên **Tầng CAO** (đòi hỏi đăng ký CSDL AI quốc gia và giám sát con người khắt khe).

## 2. Tuân thủ Bảo vệ Dữ liệu Cá nhân (PDPL 2025)
Do ChinTalk AI xử lý dữ liệu giọng nói (Dữ liệu sinh trắc học - Nhóm dữ liệu nhạy cảm).

* **Đánh giá tác động xử lý dữ liệu (DPIA):** Lập hồ sơ đánh giá rủi ro khi thu thập và xử lý giọng nói, nộp bản gốc cho Cục An ninh mạng (A05 - Bộ Công an).
* **Cơ chế Đồng ý (Consent):** Thiết lập pop-up đồng ý riêng biệt cho việc thu thập dữ liệu nhạy cảm, không gộp chung vào Điều khoản sử dụng.
* **Nhân sự bảo vệ dữ liệu:** Chỉ định cá nhân hoặc bộ phận phụ trách bảo vệ dữ liệu cá nhân (DPO).

## 3. Đánh giá tác động chuyển dữ liệu ra nước ngoài
Đây là nghĩa vụ **BẮT BUỘC** do đặc thù kỹ thuật của dự án.

* **Bối cảnh:** Việc sử dụng các API quốc tế (Qwen-2 của Alibaba, ElevenLabs, Azure STT/TTS) đồng nghĩa với việc gửi dữ liệu người dùng Việt Nam ra máy chủ nước ngoài.
* **Hành động:**
    * Lập hồ sơ **Đánh giá tác động chuyển dữ liệu cá nhân ra nước ngoài** (Mẫu số 06 - Nghị định 13).
    * Gửi hồ sơ về Bộ Công an trong vòng 60 ngày kể từ khi bắt đầu xử lý dữ liệu.
* **Chiến lược giảm thiểu rủi ro:** Ẩn danh hóa (Anonymization) dữ liệu giọng nói trước khi gửi qua API để chỉ truyền dữ liệu kỹ thuật, không truyền thông tin định danh người dùng.

## 4. Danh mục hành động (Checklist cho Investor Package)

| STT | Hành động cụ thể | Thời hạn | Cơ quan chủ quản |
|:---:|:---|:---|:---|
| 1 | Dán nhãn "Nội dung do AI tạo" trên UI/UX | Trước khi Launch | Tự thực hiện |
| 2 | Thông báo vận hành AI tầng Trung bình | Quý 1 - Quý 2/2026 | Bộ KH&CN |
| 3 | Lập báo cáo DPIA (Xử lý dữ liệu nhạy cảm) | 60 ngày sau Launch | Bộ Công an (A05) |
| 4 | Lập báo cáo Chuyển dữ liệu ra nước ngoài | 60 ngày sau Launch | Bộ Công an (A05) |
| 5 | Lưu trữ dữ liệu định danh (Metadata) tại VN | Ngay từ đầu | Viettel IDC/VNPT Cloud |

---
*Tài liệu này được soạn thảo để bổ sung vào phần "Dependencies & Constraints" và "Critical Path" trong bộ hồ sơ gọi vốn Seed của ChinTalk AI.*