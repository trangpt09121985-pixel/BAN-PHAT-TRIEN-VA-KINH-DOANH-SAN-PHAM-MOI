# Dashboard Ban Phát triển và Kinh doanh Sản phẩm mới – PVEP

Trang điều hành tĩnh (HTML) phục vụ Lãnh đạo Tổng Công ty và Ban PT&KDSPM. Phiên bản 3.5.

- `index.html` – Dashboard trong một tệp duy nhất: giao diện, ảnh và dữ liệu đã mã hóa AES-256-GCM (khối `du-lieu-ma-hoa`); dữ liệu chỉ giải mã trên trình duyệt khi đăng nhập đúng.
- `cong-cu/cap-nhat-du-lieu.html` – công cụ cho quản trị viên: ghép dữ liệu từ tệp Excel vào index.html, đổi tài khoản và mật khẩu.
- `tai-lieu/` – văn bản pháp luật công khai: bản PDF đã đánh dấu vàng nội dung cần đọc và tệp Word gốc.
- `docs/` – hướng dẫn đưa lên GitHub và cập nhật hằng tuần.

Kỹ thuật: không dùng thư viện JavaScript bên ngoài, không tải tài nguyên từ máy chủ ngoài, không dùng localStorage, sessionStorage, cookie. Font nhúng Be Vietnam Pro, Barlow Condensed (SIL Open Font License 1.1).

Bảo mật: không đưa tệp Excel dữ liệu, văn bản nội bộ, tài khoản hoặc mật khẩu vào kho này.
