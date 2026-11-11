# Music Plus 1.0.4

- Update discovery ưu tiên GitHub API với no-cache, timeout 10 giây; fallback raw nếu API bị chặn/rate limit. Không cần token, chỉ kiểm tra khi bấm nút.
- Hiển thị phiên bản vừa kiểm tra; metadata thấp hơn bản cài không được báo latest. Nếu chỉ kiểm tra được raw, hiển thị phiên bản raw báo và đề nghị thử lại, không khẳng định mới nhất.
- Ghi log installed/offered/source/HTTP/age để chẩn đoán cache và version sai.
- Giữ sửa nút X và thông báo Clear cache từ 1.0.3.

Cập nhật từ 1.0.2/1.0.3 qua Settings; không đổi layout/launcher. 130 portable checks và package verifier đạt; app/framework tests cross-build không lỗi. Windows network/UI/update thực tế chưa được chạy trong môi trường build.
