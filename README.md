# Music Plus — Windows downloads

Public binaries only. Source is maintained privately.

[Download Music Plus 1.0.0 — bản kiểm chứng](packages/MusicPlus-1.0.0-compact-windows-x64.zip)

[Thay đổi và giới hạn 1.0.0](CHANGELOG-1.0.0.md) · [SHA-256](packages/MusicPlus-1.0.0-compact-windows-x64.zip.sha256)

Thoát hẳn app kể cả khay hệ thống, giải nén **toàn bộ ZIP**, chép đè vào thư mục app cũ.
Không xoá `%LOCALAPPDATA%\MusicPlus8`: dữ liệu đăng nhập, settings, metadata/cache được giữ ở đó.
Nên sao lưu thư mục dữ liệu trên chính máy trước khi thử. Máy/tài khoản Windows khác phải đăng nhập riêng.
Cần .NET Framework 4.8 và WebView2 Runtime.

1.0.0 bỏ cơ chế tự thay file bằng PowerShell chưa được kiểm chứng. Settings chỉ kiểm tra,
tải và kiểm ZIP để bạn cập nhật thủ công. Không thêm dịch vụ/browser chạy nền.
Build/portable checks đạt; Windows live login/audio, UI, update/rollback và RAM/latency
còn phải kiểm chứng. Vì vậy stable manifest vẫn trỏ 0.9.4, chưa tự đẩy bản 1.0.0 tới mọi máy.

[Download 0.9.4](packages/MusicPlus-0.9.4-compact-windows-x64.zip) · [Changelog 0.9.4](CHANGELOG-0.9.4.md)
