# Music Plus 1.0.6 — sửa chờ khi chọn bài

- Sửa Play/Space trong lúc tải lại huỷ bài: giờ hiển thị dấu đang tải và không huỷ request.
  Bạn vẫn có thể chọn bài khác hoặc Next.
- Bỏ khoá chung toàn pipeline giữa bài bạn chọn và tải trước. Mỗi resolver có lane riêng;
  recovery không reset/kill worker của resolver còn lại. Shared config loading vẫn đồng bộ.
- Không ép tải lại config vừa refresh liên tục trong một phút, trừ khi config thiếu/hết hạn.
- Request range phụ kẹt quá hai giây không có tiến triển sẽ bỏ để tiếp tục response gốc.
  Có dữ liệu tiến triển thì gia hạn, không cắt một lượt tải khỏe mạnh chỉ vì dài hơn hai giây.
- Thêm log wait lane, header và range fallback; giữ phục hồi 403 và dữ liệu tài khoản.

Log được cung cấp cho thấy nhiều lần chuẩn bị bị huỷ khi nút Play vẫn trông như Play;
trong cùng log, một lượt hoàn thành mất 3.271s và cache mở khoảng 0.28s. Đây là số đo 1.0.5,
không phải benchmark 1.0.6. Khoá chung 1.0.5 là hồi quy đã sửa; range stall là rủi ro tìm thấy
trong code, chưa được chứng minh là nguyên nhân toàn bộ độ trễ của máy người dùng.

Cập nhật qua Settings > Check for updates, kiểm tra Version 1.0.6 sau khi mở lại.
162 portable checks đạt, gồm prefetch kẹt không chặn lane khác, cancelled wait, config refresh,
range header/body kẹt, dữ liệu fallback chính xác và range có tiến triển hơn hai giây.
App/framework/Windows test projects build được. Windows smoke checks có ca Play không huỷ
CTS nhưng chưa chạy ở Linux. Cold audio vẫn tải toàn bài; chưa đo latency live Windows bản này.
