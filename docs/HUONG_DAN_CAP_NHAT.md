# Hướng dẫn cập nhật dữ liệu hằng tuần (khoảng 15–20 phút)

## Quy tắc chung

- Chỉ sửa 4 sheet có **tab màu vàng**: `1_ThongTin`, `2_NhiemVu`, `3_KeHoach`, `4_BanTin`.
- Trong mỗi sheet, chỉ sửa **ô hoặc cột tô vàng**. Không xóa dòng 1–2 (tên cột, mã trường), không đổi tên sheet.
- Ngày ghi dạng `dd/mm/yyyy`; tiến độ là số 0–100; thiếu thông tin ghi `<CẦN_BỔ_SUNG>`.
- Tệp Excel chứa dữ liệu chưa mã hóa: lưu tại máy hoặc SharePoint của Ban, **không tải lên GitHub**.

## Các bước

| Bước | Việc làm | Nơi thực hiện |
|---|---|---|
| 1 | Mở tệp Excel của tuần trước (hoặc vào Dashboard → **Cập nhật dữ liệu** → **Lưu Excel dữ liệu hiện hành**) | Máy tính |
| 2 | Sheet `1_ThongTin`: sửa **Ngày cập nhật dữ liệu** thành ngày thứ Hai của tuần. Ngày này là mốc tính "quá hạn", "sắp đến hạn" | Excel |
| 3 | Sheet `2_NhiemVu`: cập nhật Đầu mối, Hạn, Dự kiến, Tiến độ (%), Đã hoàn thành?, Ngày hoàn thành, Kết quả. Nhiệm vụ mới ghi vào dòng vàng trống, mã tiếp theo (NV-03, NV-04…) | Excel |
| 4 | Sheet `3_KeHoach`: cập nhật Đầu mối, Tiến độ (%), Đầu ra/mốc tiếp theo, Hạn, Ghi chú | Excel |
| 5 | Sheet `4_BanTin`: dán bảng bản tin tuần vào các dòng trống, cột C–G (Nhóm tin, Nội dung, Ngày tin, Nguồn, Đường link). Cột Tuần, Kỳ để trống | Excel |
| 6 | Lưu tệp (Ctrl + S) | Excel |
| 7 | Đăng nhập Dashboard → menu **Cập nhật dữ liệu** → **Chọn tệp Excel** → xem bảng kiểm tra và các lưu ý → **Xem thử trên Dashboard** (nếu cần) → **Tải tệp index.html mới** (trang tự ghép dữ liệu mã hóa vào giao diện hiện hành; nếu mở Dashboard từ tệp trên máy, chọn thêm tệp index.html đang dùng làm khuôn) | Dashboard |
| 8 | GitHub → trang chính của kho → **Add file** → **Upload files** → kéo tệp `index.html` vừa tải vào (ghi đè tệp cũ; nếu tên có thêm số như "index (1).html" thì đổi lại thành `index.html`) → **Commit changes** | GitHub |
| 9 | Sau 1–3 phút, mở lại trang, kiểm tra ngày cập nhật ở trang Tổng quan | Điện thoại |

Tệp tải về ở bước 7 được mã hóa bằng chính tài khoản đang đăng nhập, nên tài khoản, mật khẩu của người dùng không thay đổi.

## Soạn bản tin thị trường tuần bằng AI

Dùng câu lệnh bản tin hiện có, bổ sung đoạn sau ở cuối để kết quả dán thẳng được vào sheet `4_BanTin`:

> Ngoài bản tin dạng văn bản, xuất thêm một bảng 5 cột, mỗi tin một dòng: Nhóm tin | Nội dung | Ngày tin (dd/mm/yyyy) | Nguồn | Đường link.
> Cột "Nhóm tin" chỉ dùng đúng một trong các giá trị: Tóm tắt; Chính sách và pháp lý; Dự án và nhà đầu tư; Thị trường và chuỗi cung ứng; Bối cảnh khu vực; Nhận định tác động đối với PVEP.
> Phần Tóm tắt có 3–5 dòng. Nhóm không có tin thì không tạo dòng. Tin chưa kiểm chứng ghi <CẦN_XÁC_MINH> trong cột Nội dung. Không dùng tin cũ hơn 7 ngày so với ngày phát hành.

Sau khi AI trả kết quả:

1. Mở từng đường link để kiểm tra ngày đăng và nội dung (bắt buộc với tin đưa lên trang Lãnh đạo).
2. Chọn bảng kết quả → sao chép → bấm vào ô C của dòng vàng trống đầu tiên trong sheet `4_BanTin` → dán.
3. Nhóm không có tin sẽ tự hiển thị "Không ghi nhận thông tin mới." trên Dashboard.
4. Các kỳ bản tin cũ giữ nguyên trong sheet; Dashboard có ô chọn kỳ để xem lại.

## Khi có văn bản pháp lý mới

Thêm dòng ở sheet `PhapLy` (tab xám). Nếu có tệp PDF, đặt tệp vào thư mục `tai-lieu/<lĩnh vực>/` trên GitHub và ghi đường dẫn vào cột "Tệp PDF đánh dấu vàng". Phần nội dung cần đọc (sheet `TrongTam`, `NguyenVan`) có thể gửi cho trợ lý AI để đánh dấu và bổ sung.
