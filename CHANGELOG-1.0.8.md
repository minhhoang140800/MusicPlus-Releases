# Music Plus 1.0.8

- Sửa đăng nhập khi cookie xác thực đầu tiên rỗng nhưng có cookie hợp lệ khác. Kiểm tra tài khoản, chữ ký và account scope dùng cùng cách chọn.
- Đồng bộ User-Agent/Origin/Referer của request player và tải audio. Bổ sung cver còn thiếu cho WEB_REMIX theo clientVersion thực tế, giữ nguyên các tham số đã ký.
- Thêm thông tin chẩn đoán audio không chứa cookie, token hay URL để phân biệt client version, định dạng và decoder.
- Giữ dữ liệu và cơ chế Settings > Check for updates của 1.0.7.

186 kiểm tra portable đạt. App, net48 tests và Windows smoke tests cross-build thành công; chưa chạy các kiểm tra Windows thực tế. Chưa xác nhận lỗi 403 đã hết bằng phát nhạc Premium: proxy Cloud vẫn từ chối kết nối YouTube dù danh sách mạng đã cho phép. Decoder/player bundle không thay đổi.
