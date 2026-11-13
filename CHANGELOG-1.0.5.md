# Music Plus 1.0.5 — phục hồi lỗi 403 khi chuyển bài

- 401/403 ở các bước đọc cấu hình/player/tải audio: làm mới link, client configuration và
  playback transport rồi thử lại một lần. Cùng luồng cho next thủ công, tự next và prefetch.
- Player config trong RAM/disk hết hiệu lực sau 30 phút; cache URL theo expire của link
  trừ 30 giây. Không giữ task prefetch đã dùng/lỗi để phát lại.
- Kết nối cũ chỉ dispose khi các request đang dùng đã hoàn tất. Cache MP4 đã chuẩn bị vẫn
  dùng đường nhanh. Không thêm browser hay tiến trình chạy nền.
- Giữ session/account; huỷ retry nếu đổi bài/tài khoản. Không tự retry thao tác ghi playlist.
- Nếu bị từ chối tiếp, dừng sau một refresh và báo rõ. Logs có stage/status/attempt, không
  chứa signed URL hoặc cookies. Ảnh chụp lỗi chưa đủ để xác nhận nguyên nhân server cụ thể.

Cập nhật: Settings > Check for updates, sau khi mở lại kiểm tra Version 1.0.5.
150 portable checks đạt, gồm HTTP 403 từ downloader qua fake handler, phục hồi, chặn retry
vô hạn, cancel/account guard, expiry và transport lifetime. App/framework/Windows test
projects cross-build thành công. Chưa tái hiện live YouTube/WPF trên Windows; không cam kết
mọi lỗi server 403 đều được giải quyết. Nếu còn lỗi, Export logs ngay sau lỗi để xác định stage.
