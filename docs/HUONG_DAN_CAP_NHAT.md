# Hướng dẫn cập nhật dữ liệu hằng tuần (khoảng 15–20 phút)

Từ phiên bản 3.4, Dashboard là một tệp `index.html` duy nhất, dữ liệu mã hóa nhúng ngay trong tệp; không còn tệp `data/du-lieu.enc.js`. Từ phiên bản 3.6, video mô phỏng được mã hóa và đặt trong thư mục `tai-lieu/video`.

## Quy tắc chung

- Chỉ sửa 4 sheet có **tab màu vàng**: `1_ThongTin`, `2_NhiemVu`, `3_KeHoach`, `4_BanTin`.
- Trong mỗi sheet, chỉ sửa **ô hoặc cột tô vàng**. Không xóa dòng 1–2 (tên cột, mã trường), không đổi tên sheet.
- Ngày ghi dạng `dd/mm/yyyy`; tiến độ là số 0–100; thiếu thông tin ghi `<CẦN_BỔ_SUNG>`.
- Tệp Excel chứa dữ liệu chưa mã hóa và khóa giải mã video: lưu tại máy hoặc SharePoint của Ban, **không tải lên GitHub**.

## Các bước

| Bước | Việc làm | Nơi thực hiện |
|---|---|---|
| 1 | Mở tệp Excel của tuần trước (hoặc vào Dashboard → **Cập nhật dữ liệu** → **Lưu Excel dữ liệu hiện hành**) | Máy tính |
| 2 | Sheet `1_ThongTin`: sửa **Ngày cập nhật dữ liệu** thành ngày thứ Hai của tuần. Ngày này là mốc tính "quá hạn", "sắp đến hạn" | Excel |
| 3 | Sheet `2_NhiemVu`: cập nhật Đầu mối, Hạn, Dự kiến, Tiến độ (%), Đã hoàn thành?, Ngày hoàn thành, Kết quả. Nhiệm vụ mới ghi vào dòng vàng trống, mã tiếp theo (NV-03, NV-04…) | Excel |
| 4 | Sheet `3_KeHoach`: cập nhật Đầu mối, Tiến độ (%), Đầu ra/mốc tiếp theo, Hạn, Ghi chú | Excel |
| 5 | Sheet `4_BanTin`: dán bảng bản tin tuần vào các dòng trống, cột C–G (Nhóm tin, Nội dung, Ngày tin, Nguồn, Đường link). Cột Tuần, Kỳ để trống | Excel |
| 6 | Lưu tệp (Ctrl + S) | Excel |
| 7 | Đăng nhập Dashboard → menu **Cập nhật dữ liệu** → **Chọn tệp Excel** → xem bảng kiểm tra và các lưu ý → **Xem thử trên Dashboard** (nếu cần) → **Tải tệp index.html mới** (nếu mở Dashboard từ tệp trên máy, chọn thêm tệp index.html đang dùng làm khuôn) | Dashboard |
| 8 | GitHub → trang chính của kho → **Add file** → **Upload files** → kéo tệp `index.html` vừa tải vào (ghi đè tệp cũ; nếu tên có thêm số như "index (1).html" thì đổi lại thành `index.html`) → **Commit changes** | GitHub |
| 9 | Sau 1–3 phút, mở lại trang, kiểm tra ngày cập nhật ở trang Tổng quan | Điện thoại |

Dữ liệu trong tệp tải về ở bước 7 được mã hóa bằng chính tài khoản đang đăng nhập, nên tài khoản, mật khẩu của người dùng không thay đổi.

Khi nhận phiên bản giao diện mới: mở `cong-cu/cap-nhat-du-lieu.html` → tab 1, chọn tệp Excel mới nhất của Ban và tệp `index.html` của gói mới làm khuôn, nhập tài khoản đang dùng → tải `index.html` vừa tạo lên GitHub. Cách này giữ nguyên dữ liệu và tài khoản hiện hành. Từ phiên bản 3.6, dùng tệp Excel 3.6 trở lên để video phát được.

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

## Khi văn bản mới có biểu mẫu hồ sơ (từ phiên bản 3.2)

1. Tách trang biểu mẫu thành tệp PDF riêng (nếu có bản Word gốc thì lưu thêm tệp .docx), đặt vào thư mục `tai-lieu/bieu-mau/` trên GitHub.
2. Thêm dòng ở sheet `BieuMau`: mã biểu mẫu (BM-xx), mã văn bản (VBxx), số hiệu, số mẫu, tên biểu mẫu, đường dẫn tệp PDF và Word, trang trong văn bản gốc, lĩnh vực, căn cứ (điều, khoản yêu cầu nộp mẫu).
3. Cập nhật dữ liệu như bước 7–8. Biểu mẫu sẽ hiện ở tab "Biểu mẫu", trong cửa sổ văn bản và trong tìm kiếm.

## Nội dung đào tạo (từ phiên bản 3.2)

- Thuật ngữ có giải thích chi tiết: sheet `TuDien_ChiTiet` (thuật ngữ tiếng Anh, giải thích tiếng Việt, mã hình minh họa, mã bài học liên quan).
- Bài học khóa điện gió: sheet `KhoaHoc_Bai` (từ phiên bản 3.3 có cột "Ảnh bìa"), câu hỏi: `KhoaHoc_CauHoi`, nguồn: `KhoaHoc_Nguon`.
- Chuyên đề đào tạo: sheet `DaoTao_ChuyenDe`, cột Thời lượng (phút) và Nội dung. Quy ước định dạng trong ô nội dung: dòng bắt đầu bằng `## ` là tiêu đề mục; `- ` là gạch đầu dòng; `| a | b |` là bảng; `! ` là lưu ý; `> ` là ví dụ; `? ` là liên hệ dự án; `* ` là điểm chính; `@ mã hình|chú thích` là hình minh họa; `@ anh:mã ảnh|chú thích` là ảnh thực tế.

## Video mô phỏng quy trình đầu tư ĐGNK (từ phiên bản 3.6)

- Sheet `Video_QuyTrinh`: mỗi dòng một video (V01–V06). Cột cần cập nhật: **Trạng thái** (Kịch bản / Phân cảnh / Đang dựng / Rà soát / Hoàn thành), **Đường dẫn video** (đường dẫn SharePoint/Stream của bản 1080p, nếu có) và **Ghi chú**.
- Không sửa các cột **Tệp video mã hóa**, **Dung lượng**, **Mốc cảnh**, **Phụ đề** nếu không thay tệp video; các cột này khớp với tệp trong thư mục `tai-lieu/video` trên GitHub.
- Khóa giải mã video nằm ở sheet cấu hình, dòng `videoQT.khoaVideo`. Không xóa, không sửa dòng này.
- Video trên GitHub chỉ là bản 720p đã mã hóa (`.mp4.enc.N`, mỗi tệp dưới 25 MB). Bản 1080p chưa mã hóa lưu trên SharePoint hoặc Microsoft Stream của PVEP, không tải lên GitHub.
- Video chỉ phát khi mở Dashboard qua đường dẫn web (https://); mở tệp index.html trực tiếp trên máy thì phần video không tải được.
- Cột "Lớp quản trị" và "Lớp kỹ thuật – cảnh và lời thuyết minh" dùng cùng quy ước định dạng như bài học; có thể sửa trực tiếp trong Excel.
- Lớp quản trị dựa trên Khung 10 giai đoạn đề xuất và Quy trình Giai đoạn 1 (dự thảo); khi quy trình được ban hành, cập nhật lại nội dung và cân nhắc dựng lại video.
