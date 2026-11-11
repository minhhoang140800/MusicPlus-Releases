# Music Plus 1.0.2

Cài ZIP này một lần để chuyển sang cập nhật qua Settings.

- Mở `MusicPlus.exe` ngoài cùng, giữ `versions` và `current.json` bên cạnh.
- Settings > Check for updates tải và kiểm gói từ GitHub rồi khởi động lại để cài.
  Dữ liệu tại `%LOCALAPPDATA%\MusicPlus8` được giữ nguyên.
- Mỗi bản ở thư mục riêng. Launcher chỉ xác nhận bản mới sau khi giao diện mở được;
  nếu khởi tạo lỗi sẽ mở lại bản trước. Không copy đè app đang chạy, không có updater thường trú.
- Clear unused cache xoá ảnh/audio không dùng, bản cũ không còn cần để rollback,
  staging/tải dở từ updater cũ. Giữ sign-in, settings, metadata, file audio được bảo vệ,
  active transfers và current/previous/pending version.
- Giữ Lyrics có thể copy, flyout giữ tên bài/artist khi pause và các sửa trước.

**Cài lần này:** thoát cả khay hệ thống, giải nén toàn bộ ZIP vào thư mục có quyền ghi,
ví dụ `D:\MusicPlus`. Mở exe ngoài cùng và tạo shortcut tới nó. Không mở exe bên trong versions.
Các bản <=1.0.1 dùng layout cũ nên cần bước này; từ 1.0.2 cập nhật trong Settings.
Source được giữ trong repo private; stable manifest đã chuyển sang 1.0.2.

**Kiểm chứng:** 118 portable checks và 14 launcher process checks với fake apps trên Linux
đạt. Bộ xác thực package của app kiểm đủ inventory/hash. App, launcher, framework tests và
Windows storage/WPF tests cross-build thành công. Chưa chạy update/restart WPF net48 trên
Windows thật, file lock/Defender hoặc live playback/login. Không coi mô phỏng là chứng nhận Windows.
Startup recovery không tự phát hiện mọi lỗi sau khi giao diện đã mở. Launcher protocol v1
cố định; các bản app/dependencies tương thích v1 dùng được nó. Đổi protocol/runtime có thể cần
cài gói mới. Chưa có Authenticode; checksum/manifest dùng cùng GitHub trust domain.
