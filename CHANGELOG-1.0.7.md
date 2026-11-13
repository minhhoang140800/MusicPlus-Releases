# Music Plus 1.0.7 — sửa bước cài cập nhật

- Bỏ Directory.Move cả thư mục exe/dll vừa giải nén. Chép vào phiên bản không hoạt động,
  kiểm hash rồi mới ghi pending; bản đang chạy và bản rollback được giữ nguyên.
- Dùng FileVersionInfo thay cho CLR AssemblyName để đọc version; retry ngắn khi file bị giữ
  tạm thời, tiếp tục candidate dở mà không đổi quyền hệ thống.
- Không xác nhận được bên nào giữ file từ ảnh Access denied. Cách cài mới tránh phụ thuộc
  đổi tên thư mục; không cam kết sửa mọi ACL/antivirus denial hoặc yêu cầu chạy admin.

Nếu 1.0.2–1.0.6 không tự cài được fix, dùng **MusicPlus-UpdateRepair-1.0.7.exe** một lần.
Chọn MusicPlus.exe ngoài cùng trong thư mục app cũ nếu được hỏi. Công cụ đóng app qua lệnh
thoát bình thường, không kill; gói 1.0.7/SHA được nhúng sẵn và dùng cùng extractor/publisher
như updater mới. Dữ liệu LocalAppData không bị sửa. Sau đó cập nhật tiếp trong Settings.

170 portable checks đạt: locked-source copy, current/user-state preservation, pending reuse,
orphan resume, recovery-version protection, cancellation và version reader không giữ file.
App/framework/Windows test projects và repair exe build được; kiểm tra resource/SHA nhúng
khớp ZIP đã xác minh. Chưa chạy Windows GUI/Defender/ACL end-to-end trong môi trường Linux.
Bao gồm các sửa loading/playback của 1.0.6; launcher v1 và đường dẫn userdata giữ nguyên.
