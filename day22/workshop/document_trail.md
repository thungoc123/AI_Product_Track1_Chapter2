

# Tổng hợp Hồ sơ & Trạng thái

| STT | Loại hồ sơ                                                                 | Trạng thái | Link / Deadline           |
|-----|---------------------------------------------------------------------------|:----------:|--------------------------|
|  1  | Hồ sơ Đánh giá tác động chuyển dữ liệu ra nước ngoài                      |    ✘       | Deadline: 20/05/2026      |
|  2  | Hồ sơ Đánh giá tác động xử lý dữ liệu cá nhân (DPIA)                      |    ✘       | Deadline: 25/05/2026      |
|  3  | Hồ sơ Phân tầng rủi ro AI (Dán nhãn & Thông báo Bộ KH&CN)                 |    ✘       | Deadline: 01/06/2026      |
|  4  | Hợp đồng & Điều khoản sử dụng (T&C) có mục Consent riêng                  |    ✘       | Deadline: 01/06/2026      |
|  5  | Thỏa thuận mức độ dịch vụ (SLA) với đối tác API (Alibaba/Azure)           |    ✘       | Deadline: 01/06/2026      |

---

## Lựa chọn hồ sơ ưu tiên

**Hồ sơ cần hoàn thiện:**
> **Hồ sơ Đánh giá tác động chuyển dữ liệu ra nước ngoài**  
> (Mẫu số 06 - Nghị định 13)

**Lý do rủi ro cao nhất:**
- Hệ thống bắt buộc gửi dữ liệu giọng nói/văn bản sang máy chủ nước ngoài (Qwen-2, ElevenLabs) để xử lý dưới 2 giây.
- Nếu không có hồ sơ này, vi phạm trực tiếp quy định về an ninh mạng và bảo vệ dữ liệu xuyên biên giới.
- Nguy cơ bị đình chỉ dịch vụ ngay lập tức khi thanh tra.

---

## Template tài liệu cần xây dựng (cho Hồ sơ chuyển dữ liệu)

- **Thông tin bên chuyển:** Công ty ChinTalk AI Việt Nam (Địa chỉ, Mã số thuế, DPO)
- **Mô tả dữ liệu:** Giọng nói người dùng, nội dung hội thoại (đã ẩn danh hóa ID)
- **Bên nhận dữ liệu:** Alibaba Cloud (Trung Quốc) / Microsoft Azure (Singapore)
- **Biện pháp bảo vệ:**
	- Mã hóa đường truyền SSL/TLS
	- Cam kết xóa dữ liệu sau khi xử lý (Stateless API)

---

## Phân công & Tần suất cập nhật

- **Người chịu trách nhiệm:** Product Lead (Nguyễn Thị Ngọc Thư) phối hợp với Kỹ thuật
- **Tần suất cập nhật:**
	- Mỗi khi thay đổi nhà cung cấp API (VD: Chuyển từ Qwen sang GPT-5)
	- Hoặc cập nhật hạ tầng server