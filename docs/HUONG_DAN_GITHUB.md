# Hướng dẫn đưa Dashboard v3.0 lên GitHub Pages

Toàn bộ thao tác làm trên trình duyệt (Chrome hoặc Edge), không cần cài phần mềm.

## A. Trường hợp chưa có kho (lần đầu)

1. Đăng nhập https://github.com → bấm **+** (góc trên phải) → **New repository**.
2. **Repository name**: ví dụ `dashboard-ptkdspm`. Chọn **Public** (gói GitHub miễn phí chỉ bật Pages cho kho Public; dữ liệu vẫn được mã hóa). Bấm **Create repository**.
3. Trong kho vừa tạo, bấm liên kết **uploading an existing file**.
4. Giải nén tệp zip đã nhận. Mở thư mục `github`, chọn **toàn bộ nội dung bên trong** (index.html, README.md, các thư mục data, cong-cu, docs, tai-lieu…) và kéo thả vào trang tải lên. Chrome/Edge giữ nguyên cấu trúc thư mục.
   - Tệp `.gitignore` là tệp ẩn; nếu không thấy, có thể bỏ qua.
5. Đợi thanh tải lên chạy xong (khoảng 53 MB; nên tải làm 2 lần: phần trang web, sau đó thư mục tai-lieu) → ô **Commit changes** ghi `Phiên bản 3.0` → bấm **Commit changes**.
6. Vào **Settings** → **Pages** → mục **Branch** chọn `main` và `/ (root)` → **Save**.
7. Sau 1–3 phút, trang hiển thị địa chỉ dạng `https://<tên-tài-khoản>.github.io/dashboard-ptkdspm/`. Mở địa chỉ này trên điện thoại để kiểm tra.

## B. Trường hợp đã có kho phiên bản 2.0

1. Mở kho → **Add file** → **Upload files**.
2. Kéo thả toàn bộ nội dung thư mục `github` vào. Tệp trùng tên (index.html, data/du-lieu.enc.js, cong-cu/…) sẽ được ghi đè.
3. **Commit changes**. Sau 1–3 phút, tải lại trang (trên máy tính: Ctrl + F5).

## C. Đổi tài khoản và mật khẩu (bắt buộc trước khi gửi đường dẫn cho Lãnh đạo)

Gói này dùng tài khoản thử nghiệm `ptkd.demo`. Thay bằng tài khoản chính thức:

1. Mở `https://<địa-chỉ-trang>/cong-cu/cap-nhat-du-lieu.html` → tab **2. Đổi tài khoản, mật khẩu**.
2. Chọn tệp `data/du-lieu.enc.js` (trong thư mục `github` đã giải nén) → nhập tài khoản hiện tại → nhập tài khoản và mật khẩu mới (tối thiểu 10 ký tự, có chữ hoa, chữ thường, số) → bấm nút tạo tệp.
3. Tải tệp `du-lieu.enc.js` mới lên thư mục `data` của kho (Add file → Upload files → Commit changes).
4. Thông báo tài khoản mới cho người dùng qua kênh nội bộ. Không ghi tài khoản, mật khẩu vào GitHub, README hay nội dung commit.

## Lưu ý

- Giới hạn tải lên qua trình duyệt: mỗi tệp tối đa 25 MB, mỗi lần tối đa 100 tệp. Tệp lớn nhất của gói khoảng 7,7 MB. Nếu trình duyệt báo quá 100 tệp, tải lần lượt từng thư mục con của `tai-lieu`.
- Không tải lên GitHub: tệp Excel dữ liệu, bản xem ngoại tuyến, văn bản nội bộ (QĐ 138/QĐ-BNNMT, báo cáo nội bộ, quyết định nội bộ).
- Thư mục `tai-lieu` chỉ chứa văn bản quy phạm pháp luật công khai; bất kỳ ai có đường dẫn trực tiếp đến tệp PDF đều mở được.
- Đề nghị Ban CNTT&CĐS thẩm định trước khi dùng chính thức; nếu Tổng Công ty có máy chủ nội bộ, có thể chép nguyên thư mục `github` lên máy chủ đó mà không cần sửa mã.
