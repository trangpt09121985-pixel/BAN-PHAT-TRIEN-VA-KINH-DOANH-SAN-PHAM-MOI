# Hướng dẫn đưa Dashboard lên GitHub Pages (từ phiên bản 3.4)

Từ phiên bản 3.4, dữ liệu mã hóa nằm ngay trong tệp `index.html`; không còn tệp `data/du-lieu.enc.js`.

Toàn bộ thao tác làm trên trình duyệt (Chrome hoặc Edge), không cần cài phần mềm.

## A. Trường hợp chưa có kho (lần đầu)

1. Đăng nhập https://github.com → bấm **+** (góc trên phải) → **New repository**.
2. **Repository name**: ví dụ `dashboard-ptkdspm`. Chọn **Public** (gói GitHub miễn phí chỉ bật Pages cho kho Public; dữ liệu vẫn được mã hóa). Bấm **Create repository**.
3. Trong kho vừa tạo, bấm liên kết **uploading an existing file**.
4. Giải nén tệp zip đã nhận. Mở thư mục `github`, chọn **toàn bộ nội dung bên trong** (index.html, README.md, các thư mục cong-cu, docs, tai-lieu…) và kéo thả vào trang tải lên. Chrome/Edge giữ nguyên cấu trúc thư mục.
   - Tệp `.gitignore` là tệp ẩn; nếu không thấy, có thể bỏ qua.
5. Đợi thanh tải lên chạy xong (khoảng 53 MB; nên tải làm 2 lần: phần trang web, sau đó thư mục tai-lieu) → ô **Commit changes** ghi `Phiên bản 3.0` → bấm **Commit changes**.
6. Vào **Settings** → **Pages** → mục **Branch** chọn `main` và `/ (root)` → **Save**.
7. Sau 1–3 phút, trang hiển thị địa chỉ dạng `https://<tên-tài-khoản>.github.io/dashboard-ptkdspm/`. Mở địa chỉ này trên điện thoại để kiểm tra.

## B. Trường hợp đã có kho, nhận phiên bản giao diện mới

Tệp `index.html` trong gói mới đã mã hóa bằng tài khoản đang dùng (đã thông báo qua kênh nội bộ). Nếu chỉ cần cập nhật giao diện, tải thẳng tệp này lên. Khi muốn ghép dữ liệu Excel mới vào giao diện mới:

1. Mở `cong-cu/cap-nhat-du-lieu.html` (trong gói mới) → tab **1. Mã hóa từ tệp Excel**.
2. Chọn tệp Excel dữ liệu mới nhất của Ban, chọn tệp `index.html` của gói mới làm khuôn, nhập tài khoản và mật khẩu đang dùng → bấm **Kiểm tra và tạo index.html**.
3. Mở kho → **Add file** → **Upload files** → kéo tệp `index.html` vừa tạo và các tệp, thư mục thay đổi khác (cong-cu, NHAT_KY_PHIEN_BAN.md…) vào → **Commit changes**.
   - Phiên bản 3.6: tải thêm thư mục `tai-lieu/video` (các tệp `.mp4.enc.N`, mỗi tệp dưới 25 MB). Nếu vượt 100 tệp một lần, tải riêng thư mục này. Tệp Excel 3.6 chứa khóa giải mã video; luôn dùng Excel 3.6 trở lên khi ghép dữ liệu, nếu không video sẽ không phát được.
4. Sau 1–3 phút, tải lại trang (trên máy tính: Ctrl + F5). Có thể xóa thư mục `data` cũ trên GitHub (không còn dùng).

## C. Đổi tài khoản và mật khẩu (bắt buộc trước khi gửi đường dẫn cho Lãnh đạo)

Khi cần đổi tài khoản hoặc mật khẩu đang dùng:

1. Mở `https://<địa-chỉ-trang>/cong-cu/cap-nhat-du-lieu.html` → tab **2. Đổi tài khoản, mật khẩu**.
2. Chọn tệp `index.html` đang dùng → nhập tài khoản hiện tại → nhập tài khoản và mật khẩu mới (tối thiểu 8 ký tự, có chữ hoa, chữ thường, số; khuyến nghị từ 12 ký tự) → bấm **Đổi và tạo index.html mới**.
3. Tải tệp `index.html` mới lên trang chính của kho (Add file → Upload files → Commit changes), ghi đè tệp cũ. Nếu tên tệp tải về có thêm số, ví dụ "index (1).html", đổi lại đúng thành `index.html`.
4. Thông báo tài khoản mới cho người dùng qua kênh nội bộ. Không ghi tài khoản, mật khẩu vào GitHub, README hay nội dung commit.

## Lưu ý

- Giới hạn tải lên qua trình duyệt: mỗi tệp tối đa 25 MB, mỗi lần tối đa 100 tệp. Tệp lớn nhất của gói khoảng 7,7 MB; `index.html` khoảng 2,7 MB. Nếu trình duyệt báo quá 100 tệp, tải lần lượt từng thư mục con của `tai-lieu`.
- Không tải lên GitHub: tệp Excel dữ liệu (chứa khóa giải mã video), video MP4 chưa mã hóa, văn bản nội bộ (QĐ 138/QĐ-BNNMT, báo cáo nội bộ, quyết định nội bộ).
- Thư mục `tai-lieu` chỉ chứa văn bản quy phạm pháp luật công khai; bất kỳ ai có đường dẫn trực tiếp đến tệp PDF đều mở được.
- Đề nghị Ban CNTT&CĐS thẩm định trước khi dùng chính thức; nếu Tổng Công ty có máy chủ nội bộ, có thể chép nguyên thư mục `github` lên máy chủ đó mà không cần sửa mã.
