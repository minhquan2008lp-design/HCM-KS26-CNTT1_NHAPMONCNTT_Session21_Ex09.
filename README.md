# Phần 1: Thiết kế Prompt 3 thành phần
Câu 1. Vì sao câu hỏi ban đầu khiến AI trả lời sai?

Vì câu hỏi quá chung chung, thiếu thông tin về thiết bị, hệ điều hành và thông báo lỗi cụ thể. AI không đủ dữ liệu nên dễ phỏng đoán sai (AI Hallucination).

Câu 2. Prompt 3 thành phần hoàn chỉnh
[CONTEXT – NGỮ CẢNH]

Tôi là kỹ thuật viên vận hành trạm sạc VoltCharge, sử dụng Windows 11. Trụ sạc số 04 đột ngột ngừng hoạt động.

[RAW ERROR – LỖI NGUYÊN VĂN]
ControllerDaemon failed to start.
System.UnauthorizedAccessException:
Access to the path 'C:\Program Files\VoltCharge\data\session.log' is denied.
Process terminated with exit code 5 (0x00000005).
[INSTRUCTION – YÊU CẦU]

Hãy giải thích lỗi bằng tiếng Việt đơn giản, tìm nguyên nhân và đưa ra 3 bước khắc phục an toàn trên Windows 11. Không hướng dẫn tháo thiết bị hoặc thực hiện lệnh nguy hiểm.




Phần 2: Giải mã lỗi và khắc phục
Câu 3. Dịch và giải thích lỗi
- Access is denied: Truy cập bị từ chối.
- UnauthorizedAccessException: Lỗi không đủ quyền truy cập.
Nguyên nhân: Phần mềm không có quyền ghi file session.log trong thư mục Program Files được Windows bảo vệ, khiến dịch vụ không thể khởi động.

Câu 4. Ba bước khắc phục
1. Run as Administrator: Nhấn chuột phải vào phần mềm VoltCharge → chọn Run as administrator.
2. Kiểm tra phân quyền: Vào Properties → Security của thư mục data, kiểm tra quyền ghi file.
3. Cấp quyền và kiểm tra: Nhờ quản trị viên cấp quyền Write/Modify cho đúng tài khoản dịch vụ, sau đó kiểm tra lại phần mềm.

Câu 5. Xử lý API_KEY

Phải xóa hoặc che giấu API Key trước khi gửi cho AI.

API_KEY: [REDACTED]

Tránh lộ thông tin bí mật, ngăn người khác lợi dụng khóa để truy cập trái phép vào hệ thống.

Khi sử dụng AI cần nhớ 3 nguyên tắc:
1. Cung cấp đầy đủ ngữ cảnh để tránh AI đoán sai.
2. Không chạy mã lệnh khi chưa kiểm tra.
3. Tuyệt đối không gửi mật khẩu, API Key và OTP lên AI.