# Music Plus — Windows downloads

[Download Music Plus 1.0.9](packages/MusicPlus-1.0.9-compact-windows-x64.zip) · [Thay đổi](CHANGELOG-1.0.9.md) · [SHA-256](packages/MusicPlus-1.0.9-compact-windows-x64.zip.sha256)

Cần .NET Framework 4.8 và WebView2 Runtime. Source nằm trong GitHub private.

Thoát Music Plus cũ cả khay hệ thống. Giải nén **toàn bộ ZIP một lần** vào thư mục có quyền ghi
(ví dụ D:\MusicPlus), luôn mở MusicPlus.exe ở **ngoài cùng**. Giữ thư mục versions và current.json.
Không xoá %LOCALAPPDATA%\MusicPlus8: sign-in, settings, metadata/cache vẫn được giữ ở đó.

Từ 1.0.2: **Settings > Check for updates** kiểm tra GitHub, tải/kiểm gói và mở lại để cập nhật.
Không cần GitHub token, không có updater thường trực. Mỗi bản ở thư mục riêng; nếu khởi tạo
bản mới thất bại, launcher mở lại bản trước. **Clear unused cache** dọn cache thừa và bản cũ,
giữ dữ liệu cá nhân và một bản để rollback. Các bản <=1.0.1 cần cài ZIP này một lần vì đổi layout.

186 portable checks, 186 net48 checks, 17 Windows smoke checks và 4 native decoder vectors đạt.
Premium itag 141 tải toàn bài và phát WPF trên Windows thành công; người dùng đã xác nhận app chạy được.
Chưa kiểm chứng trọn vòng restart/update WPF; xem changelog về giới hạn còn lại.

## Nếu bản cũ báo Access denied khi update

[Tải công cụ sửa một lần — 1.0.7](packages/MusicPlus-UpdateRepair-1.0.7.exe). Chạy file, chọn MusicPlus.exe ngoài cùng trong thư mục app cũ nếu công cụ hỏi. Công cụ yêu cầu app thoát bình thường, chép/kiểm gói nhúng và mở lại bằng launcher cũ. Không yêu cầu admin, không sửa ACL hoặc LocalAppData. Có thể xoá công cụ sau khi dùng. Từ 1.0.7 tiếp tục cập nhật trong Settings.
