# Music Plus 1.0.0

Bản compact Windows x64 để kiểm chứng sau audit, giữ dữ liệu tại `%LOCALAPPDATA%\MusicPlus8`.

- Sửa queue bị nhân đôi khi refresh; phân biệt từng bản sao bài trong playlist.
- Dừng tác vụ/view/queue cũ khi đổi tài khoản; tách cache audio theo tài khoản.
- Lưu cookies và account identity trong cùng file mã hoá atomic, có backup.
- Add single/batch ghép xác nhận theo video ID, không dựa vào thứ tự trả về.
  Không báo thành công khi thiếu ID; lỗi mạng sau ghi báo kết quả chưa xác định,
  cần refresh và kiểm tra trước khi retry. Remove chỉ ẩn hàng sau xác nhận server.
- Thông báo lỗi thao tác rõ hơn. Bỏ probe/test khỏi exe, cache thời lượng không cần thiết,
  icon trùng và việc quét process đo RAM liên tục; giảm polling Library nền.
- Khôi phục settings/metadata từ backup; dữ liệu hỏng được giữ lại, không ghi defaults đè lên.
- Chặn phím tắt phía sau Settings. Catalog artist/album không chọn đại shelf không rõ nghĩa.
- Giữ tính năng 0.9.4: copy/select text, Ctrl/Shift multi-select, Add picker một click có ảnh,
  cảnh báo trùng, link search, Back, Lyrics, Library order và các cột Views/Artist/Album.

**Cập nhật:** thoát cả khay hệ thống, giải nén toàn bộ ZIP rồi chép đè thư mục app.
Không xoá `%LOCALAPPDATA%\MusicPlus8`. Nên sao lưu thư mục dữ liệu trên chính máy trước khi thử.
Settings kiểm tra/tải ZIP có checksum và đủ dependencies; cơ chế PowerShell tự chép đè cũ đã
bị xoá. Tạm thời phải chép đè thủ công sau tải, chưa tự cài/rollback.

**Kiểm chứng:** 102 portable regression checks đạt; app và hai bộ test net48 build thành công,
0 warnings/errors. ZIP kiểm tra CRC, SHA256 từng file, đủ 13 file, đúng PE x64/version.
Môi trường build Linux chưa chạy WPF/login/audio/update thực tế trên Windows.
Không có benchmark chứng minh giảm RAM hoặc tăng tốc phát bài chưa cache.

Chưa có Authenticode; engine native vẫn là runtime đã khôi phục từ 0.8.11, thiếu source/build
recipe đầy đủ. Cold audio vẫn tải/remux toàn bài; eager paging và đồng bộ playlist còn giới hạn.
Chưa tích hợp hướng Free từ các bypass test; chưa cam kết Free/chặn quảng cáo.
Đây chưa phải chứng nhận sẵn sàng phát hành cho hàng nghìn người dùng.

`preview-1.0.0.json` ghi phiên bản/checksum gói này; stable `update.json` vẫn ở 0.9.4
trong lúc chờ kiểm chứng Windows. Source chỉ lưu trong repository private.
