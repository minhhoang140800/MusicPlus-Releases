# Music Plus — Windows downloads

[Download Music Plus 1.0.6](packages/MusicPlus-1.0.6-compact-windows-x64.zip) · [Thay đổi](CHANGELOG-1.0.6.md) · [SHA-256](packages/MusicPlus-1.0.6-compact-windows-x64.zip.sha256)

Cần .NET Framework 4.8 và WebView2 Runtime. Source nằm trong GitHub private.

Thoát Music Plus cũ cả khay hệ thống. Giải nén **toàn bộ ZIP một lần** vào thư mục có quyền ghi
(ví dụ D:\MusicPlus), luôn mở MusicPlus.exe ở **ngoài cùng**. Giữ thư mục versions và current.json.
Không xoá %LOCALAPPDATA%\MusicPlus8: sign-in, settings, metadata/cache vẫn được giữ ở đó.

Từ 1.0.2: **Settings > Check for updates** kiểm tra GitHub, tải/kiểm gói và mở lại để cập nhật.
Không cần GitHub token, không có updater thường trực. Mỗi bản ở thư mục riêng; nếu khởi tạo
bản mới thất bại, launcher mở lại bản trước. **Clear unused cache** dọn cache thừa và bản cũ,
giữ dữ liệu cá nhân và một bản để rollback. Các bản <=1.0.1 cần cài ZIP này một lần vì đổi layout.

118 logic checks + 14 launcher process checks trên Linux đạt. Chưa kiểm chứng vòng cập nhật
WPF net48 trên Windows thực tế; xem changelog về giới hạn recovery, code signing và native engine.
