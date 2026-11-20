# Music Plus 1.0.11 — 2026-11-20

- Lyrics chạy theo từng dòng: highlight và tự cuộn theo vị trí phát khi có timestamp khớp bài.
- Bấm vào một dòng để tua đến đó và phát, kể cả khi đang pause.
- Giữ bôi đen/copy qua nhiều dòng; double-click chọn từ và kéo chọn không gây tua nhầm.
  Tự cuộn tạm dừng khi bạn cuộn hoặc chọn lời.
- Bài thiếu timing phù hợp tiếp tục hiện lời tĩnh. Ưu tiên nguồn YouTube; LRCLIB dự phòng
  khi tên bài, ca sĩ, album và thời lượng khớp. Độ phủ/độ chính xác phụ thuộc dữ liệu nguồn.

Chỉ giữ lyrics đang xem trong RAM. Timer 150 ms dừng khi pause, đóng lyrics hoặc ẩn/minimize
cửa sổ. Cache đĩa giới hạn 128 mục/4 MiB; Clear unused cache cũng dọn lyrics. LRCLIB nhận
metadata bài/thời lượng khi cần tra cứu, không nhận cookie hoặc thông tin đăng nhập YouTube.

Kiểm chứng: 218 portable checks, 218 net48 checks, 37 Windows checks, 4 native decoder vectors.
Lấy được 58 dòng có timestamp từ LRCLIB; thử trên MP4 thật với phiên đăng nhập sao chép mã hóa
tạm, bấm dòng 31,32 giây đã tua đúng, phát tiếp và cập nhật highlight. Tài khoản gốc, thư viện
và settings không bị thay đổi. Nhánh timed YouTube có kiểm thử parser, chưa xác nhận độ phủ live.

Mẫu 300 dòng sau khi làm nóng WPF tăng khoảng 3,52 MB bộ nhớ riêng trong một lần đo;
đây không phải mức RAM cố định cho mọi bài. Native seek có thể khựng ngắn do mở lại file.

**Cập nhật:** Settings > Check for updates. Không cần xóa hay giải nén đè app.
Bộ decoder sửa 403, điều khiển phím media, layout updater và repair 1.0.7 được giữ nguyên.
