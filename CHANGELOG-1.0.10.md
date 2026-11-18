# Music Plus 1.0.10 — 2026-11-18

Sửa phím Play/Pause, Next và Previous trên bàn phím khi sự kiện đi qua WPF,
kể cả khi Settings đang mở. Bổ sung hỗ trợ lệnh Play/Pause riêng của Windows,
trả đúng xác nhận cho lệnh đã nhận và tránh xử lý trùng giữa WPF/native/SMTC.
Không chặn các phím media toàn hệ thống hoặc chiếm điều khiển của app khác.

Kiểm chứng: tái hiện lỗi WPF trên 1.0.9 trước sửa; 26 Windows checks đạt sau sửa,
gồm Play/Pause, Next, Settings, native command và chống nhận trùng. Bốn lệnh thật
qua dịch vụ SMTC của Windows (Pause, Play, Next, Previous) cũng đạt trên phiên test
riêng, không gửi phím toàn hệ thống. Chưa bấm trực tiếp phím Fn/media trên thiết bị vật lý.
186 portable, 186 net48 checks và bốn native decoder vectors đạt.

**Cập nhật:** Settings > Check for updates. App tải, kiểm gói, cài vào thư mục phiên bản
riêng và mở lại. Không cần xóa hay giải nén app; đăng nhập, thư viện và settings được giữ nguyên.
Bộ decoder sửa 403, native engine và payload repair 1.0.7 không thay đổi.
