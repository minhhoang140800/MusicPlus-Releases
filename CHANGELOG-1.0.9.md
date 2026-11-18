# Music Plus 1.0.9 — 2026-11-18

- Cập nhật đồng bộ decoder và signature timestamp theo player hiện tại để sửa playback 403.
- Sửa đọc session đã lưu sau khi mở lại app; giữ nguyên đăng nhập, thư viện và settings.
- Đưa 1.0.9 lên kênh stable sau khi người dùng xác nhận app chạy thành công.

**Cập nhật:** Settings > Check for updates. Các bản mới được cung cấp qua kênh này;
không cần xóa app và giải nén đè mỗi lần. Người đang dùng 1.0.9 không cần cài lại.
Thông báo GitHub đang trả 1.0.8 được giải quyết khi manifest stable đồng bộ lên 1.0.9.0.

Kiểm chứng Windows: 186 portable + 186 .NET Framework checks, 17 Windows smoke checks,
4 native decoder vectors. Với cùng session Premium, bộ player cũ trả 403 cả hai lượt;
bộ mới tải toàn bộ hai bài itag 141, remux và phát WPF thành công, không cần retry.
Người dùng xác nhận chạy app thành công. Next/auto-next trên UI và vòng updater/restart
đầy đủ chưa được kiểm thử trực tiếp trong phiên phát triển.

Chế độ không đăng nhập vẫn có bài bị 403 ở phần sau. Native engine giữ nguyên;
decoder đóng gói có thể cần cập nhật tiếp khi YouTube thay đổi. Không đổi data path,
không thay payload repair 1.0.7 và không thêm updater thường trực.

Gói phát hành giữ nguyên từng byte so với bản thử 1.0.9 được xác nhận; README bên trong
vẫn ghi trạng thái candidate ban đầu. SHA256 của ZIP:
`17b78d245bb160de4003b575b9718e3197d2a4e076f419fca25e7d4b0dbbcd9c`.
