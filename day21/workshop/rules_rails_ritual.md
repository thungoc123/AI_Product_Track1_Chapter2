Risk lớn nhất: Sự đứt gãy giữa Kỳ vọng Trải nghiệm và Rào cản Kỹ thuật" (Experience vs. Technical Friction). (đội ngũ nội bộ không thống nhất được việc ưu tiên "Nói được" hay "Nói đúng" trong giai đoạn đầu)

R1 — RULES (Quy tắc)
Cấm cụ thể: Nghiêm cấm việc ưu tiên độ chính xác ngữ pháp (Grammar Correctness) nếu việc đó làm độ trễ hệ thống (Latency) vượt quá 2.5 giây. Tuyệt đối không tự ý tích hợp thêm các module kiểm tra lỗi nặng vào luồng xử lý chính (Main Pipeline) mà chưa qua kiểm duyệt của Lead Tech.

Allowed alternative: Nếu muốn cải thiện độ chính xác, hãy sử dụng cơ chế xử lý song song (Asynchronous) hoặc hậu kiểm (Post-processing) sau khi AI đã phản hồi cho người dùng, với chi phí server bổ sung không quá $150/tháng.

Hậu quả vi phạm: Vi phạm lần đầu sẽ phải trình bày lại logic tối ưu hóa tại buổi họp kỹ thuật. Vi phạm lần hai dẫn đến đình chỉ quyền can thiệp vào Core Engine (Production branch).

Update mechanism: Mọi thay đổi về thứ tự ưu tiên (Speed vs. Quality) phải được cập nhật vào trang "Product North Star" trên Notion và thông báo qua Slack #eng-announcement.

R2 — RAILS (Công cụ chặn tự động)
Tool 1: Datadog / New Relic ($70 - $150/tháng): Thiết lập hệ thống cảnh báo tự động (Alerting). Nếu thời gian phản hồi trung bình (P95 Latency) chạm ngưỡng 2 giây, hệ thống sẽ gửi thông báo khẩn cấp cho toàn team Engineering để rollback các tính năng gây chậm.

Tool 2: LangSmith / Promptfoo ($0 - $100/tháng tùy volume): Sử dụng để chạy các bộ test tự động (Automated Benchmarking) cho mỗi lần cập nhật Prompt. Nếu Prompt mới giúp nói đúng hơn nhưng làm tăng số lượng Tokens khiến phản hồi chậm, tool sẽ tự động đánh dấu "Fail" và chặn merge vào code chính.

R3 — RITUAL (Nghi thức hàng tuần)
Nghi thức: "The 2-Second Ping-Pong" diễn ra vào 10:00 sáng Thứ Sáu. Mỗi thành viên (kể cả Founder) sẽ dùng bản build mới nhất để hội thoại liên tục với AI trong 5 phút.

Question Founder sẽ hỏi team: "Trong 5 phút vừa qua, có khoảnh khắc nào bạn phải chờ đợi AI đến mức muốn ngắt lời nó để nói bằng tiếng Việt không?" (Câu hỏi này ép team phải nhìn vào sự thật về độ trễ thay vì chỉ nhìn vào các con số kỹ thuật vô hồn).

Self-check:
Tổng cost Rails: Khoảng $170 - $250/tháng (Dưới mức $500).

Ritual implement được trong 1 tuần? Có. Chỉ cần một buổi họp 15-30 phút sáng Thứ Sáu và cài đặt nhanh các công cụ tracking latency.