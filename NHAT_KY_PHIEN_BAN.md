# Nhật ký phiên bản – Dashboard Ban Phát triển và Kinh doanh Sản phẩm mới

## Phiên bản 3.6 – 26/10/2026
- Khóa học điện gió: Bài 4 bổ sung khí động học cánh (lực nâng, lực cản, góc tấn và thất tốc, xoắn cánh, đường Cp–λ, điều khiển MPPT, mật độ không khí theo nhiệt độ và độ cao, hệ thống pitch); Bài 7 bổ sung bảng lựa chọn móng theo độ sâu nước, móng trên bờ và vùng bãi triều gần bờ; Bài 8 bổ sung trình tự lắp đặt, kiểm soát chất lượng và chứng nhận loại, đo đường cong công suất theo IEC 61400-12-1:2022, chạy thử và nghiệm thu, an toàn (GWO), số hóa. Khóa học có 13 bài, 40 câu hỏi; 9 hình minh họa mới.
- Video mô phỏng quy trình: thay khung 12 tập bằng 6 video 3D đã dựng (V01 Tổng quan vòng đời; V02 Khảo sát gió và điều kiện tự nhiên; V03 Thi công và lắp đặt; V04 Báo cáo tiền khả thi, khả thi và mô hình kinh tế; V05 Pháp lý, phê duyệt và quyết định đầu tư; V06 Vận hành, bảo dưỡng và quản lý tài sản), tổng khoảng 17 phút, thuyết minh giọng nữ, phụ đề tiếng Việt. V04–V06 được xây dựng từ đề cương của kịch bản. Trang video có trình phát, danh sách cảnh để tua nhanh, lời thuyết minh đầy đủ và lớp quy trình quản trị lấy từ khung 12 tập trước.
- Video trên web được mã hóa AES-256-GCM (thư mục tai-lieu/video, mỗi tệp dưới 25 MB); khóa giải mã nằm trong dữ liệu đã mã hóa của Dashboard. Excel: sheet Video_QuyTrinh thêm cột Mô tả ngắn, Tệp video mã hóa, Dung lượng, Mốc cảnh, Phụ đề; sheet cấu hình thêm khóa videoQT.khoaVideo.

## Phiên bản 3.5 – 26/10/2026
- Đổi tài khoản đăng nhập của Dashboard (thông báo tài khoản qua kênh nội bộ, không ghi vào kho).
- Khóa học điện gió: Bài 6 "Thiết kế tuabin gió" bổ sung tải cực hạn, tải mỏi và trường hợp tải thiết kế (quy tắc Miner); kết cấu cánh (spar cap, shear web, vỏ sandwich), moay-ơ, bedplate, tháp; hệ truyền động (mô-men định mức, bánh răng hành tinh, hộp số hay truyền động trực tiếp, độ tin cậy); điều khiển pitch độc lập; tối ưu đa mục tiêu; tiêu chuẩn và chứng nhận (IEC 61400-22 đã rút lại từ 31/8/2018); tuabin trục đứng.
- Bài mới 7 "Nền móng ngoài khơi và điện gió nổi". Bài 8 "Chế tạo, vận chuyển và lắp đặt" bổ sung sản xuất cánh (VARI, RTM, kiểm tra không phá hủy), tháp, hộp số, máy phát, lắp ráp nacelle, ràng buộc vận chuyển đường bộ và đường biển. Khóa học có 13 bài, 36 câu hỏi; 10 hình minh họa mới.
- Mục mới "Video mô phỏng quy trình" (Phát triển năng lực): khung 12 tập từ khởi tạo dự án tới vận hành thương mại; mỗi tập có lớp quy trình quản trị đầu tư PVEP và lớp phân cảnh mô phỏng 3D, cổng quyết định, văn bản, biểu mẫu, bài học liên quan; hướng dẫn xây dựng bộ video. Excel thêm sheet Video_QuyTrinh để cập nhật trạng thái và đường dẫn video.
- Công cụ cập nhật: mật khẩu tối thiểu 8 ký tự, có chữ hoa, chữ thường, chữ số (khuyến nghị từ 12 ký tự).

## Phiên bản 3.4 – 23/10/2026
- Dữ liệu mã hóa nhúng trực tiếp trong tệp index.html (khối `du-lieu-ma-hoa`); không còn tệp data/du-lieu.enc.js. Dashboard là một tệp HTML duy nhất, mở được cả khi tải về máy.
- Trang Cập nhật dữ liệu: nút "Tải tệp index.html mới" tự ghép dữ liệu mới vào giao diện hiện hành; khi mở Dashboard từ tệp trên máy, trang yêu cầu chọn tệp index.html đang dùng làm khuôn.
- Công cụ cong-cu/cap-nhat-du-lieu.html: tab 1 nhận tệp Excel và tệp index.html làm khuôn, xuất index.html; tab 2 đổi tài khoản trực tiếp trên index.html (vẫn nhận tệp du-lieu.enc.js của phiên bản cũ).
- Cập nhật hướng dẫn trong Excel (sheet 0_HuongDan), README và thư mục docs.

## Phiên bản 3.3 – 21/10/2026
- Khóa học điện gió, Bài 10 "Kinh tế dự án": ví dụ tính LCOE từng bước cho trang trại 495 MW (CAPEX theo IRENA 2025, phân bổ theo cơ cấu điển hình, CRF, LCOE ở P50 và P90); bảng độ nhạy và ba biến số quyết định tính khả thi; hợp đồng bán điện và phân bổ rủi ro giá; DSCR, LLCR và cách ngân hàng thẩm định; khung giá điện gió năm 2025 (QĐ 1508/QĐ-BCT, QĐ 1824/QĐ-BCT); mục "Bài này chưa đề cập".
- Bài 6 "Thiết kế tuabin và nền móng": quy trình thiết kế tích hợp, vì sao ba cánh và đón gió phía trước, công suất riêng, IEC 61400-1:2019/AMD1:2025, IEC 61400-15-1:2025 và tình trạng dự thảo IEC 61400-15-2.
- Bài 1: số liệu IRENA năm 2025 (suất đầu tư 976 và 2.931 USD/kW; hệ số công suất 36% và 41%).
- 8 hình minh họa mới (có chuyển động): quy trình thiết kế, bóng tháp, công suất riêng, phân bổ CAPEX, chi phí năm tới LCOE, LCOE theo suất chiết khấu, LCOE theo hệ số công suất, rủi ro giá theo hợp đồng.
- Ảnh thực tế: banner ảnh chuyển động trên trang Tổng quan và trang Khóa học; ảnh bìa cho Bài 1, 2, 6, 7; ảnh trong bài và trong cửa sổ Từ điển (móng, tàu lắp đặt, điện gió nổi, điện gió gần bờ).
- Công cụ Kinh tế: thêm phần vốn vay (tỷ lệ vay, lãi suất, thời hạn) để tính DSCR, LLCR ở P50 và P90; thêm LCOE ở P90, độ nhạy theo suất chiết khấu và OPEX, biểu đồ LCOE theo suất chiết khấu. Suất đầu tư mặc định cập nhật 2.931 USD/kW (IRENA 2025).
- Thử thách: 30 câu hỏi (thêm 5). Excel: sheet KhoaHoc_Bai thêm cột "Ảnh bìa".

## Phiên bản 3.2 – 20/10/2026
- Từ điển điện gió ngoài khơi: bấm vào thuật ngữ tiếng Anh mở cửa sổ giải thích bằng tiếng Việt; 111 thuật ngữ cốt lõi có giải thích chi tiết, hình minh họa (tĩnh hoặc động), liên kết tới bài học liên quan và các thuật ngữ gần nghĩa. Bộ lọc mới "Có giải thích chi tiết".
- Khóa học điện gió: thêm Bài 2 "Khung pháp lý và tiêu chuẩn" (khái niệm 06 hải lý theo Luật Điện lực 2024, thứ tự ưu tiên, hai luồng thủ tục, bộ TCVN 10687); hiệu chỉnh và bổ sung các bài theo tài liệu đào tạo EPU 2026 và IRENA 2025 (cấp độ nhám và hệ số α, cường độ rối, mô hình đĩa truyền động Cp/Ct, mô hình vết khí động Jensen, P75, cấp tuabin S/T, yêu cầu tần số theo TT 05/2025/TT-BCT, LCOE theo FCR, BCR, nội suy IRR).
- Trình bày bài học: ảnh bìa có tuabin quay, thanh tiến độ, mục lục, tiêu đề đánh số, bảng, ô "Điểm chính", 27 hình minh họa SVG (một số có chuyển động; tự tắt khi thiết bị bật chế độ giảm chuyển động).
- Công cụ tính toán: Weibull phân tích tại một tốc độ chọn trước; Tốc độ gió theo độ cao thêm bảng theo 7 cấp độ nhám; Công suất đầu ra thêm tính mật độ không khí theo độ cao, nhiệt độ và lực đẩy Ct; Kinh tế thêm P50/P75/P90, BCR, thời gian hoàn vốn, trượt giá PPA.
- Thử thách: 25 câu hỏi (thêm 5).
- Đào tạo: 12 chuyên đề có nội dung chi tiết (thời lượng, mục tiêu, nội dung theo mục, bảng, ví dụ, liên hệ dự án, liên kết tới văn bản).
- Văn bản pháp lý: tab mới "Biểu mẫu" gồm 26 mẫu hồ sơ tách thành tệp PDF riêng (TT 79/2025 Mẫu số 01 kèm bản Word; NĐ 243/2026 Phụ lục II; NĐ 272/2026; NĐ 06/2022 Phụ lục II–V). Biểu mẫu hiện trong cửa sổ văn bản, trong nguyên văn điều khoản liên quan và trong tìm kiếm toàn trang.
- Excel dữ liệu thêm sheet TuDien_ChiTiet, BieuMau; sheet DaoTao_ChuyenDe thêm cột Thời lượng và Nội dung.

## Phiên bản 3.1 – 20/10/2026
- Văn bản pháp lý, tab "Nội dung cần đọc": từng nội dung tô vàng được gán đúng lĩnh vực (Điện gió ngoài khơi; Sản phẩm mới – CCS/CCUS, dầu khí, khoáng sản, năng lượng ngoài khơi gắn dầu khí; Dùng chung – đầu tư, đấu thầu). Bộ lọc Điện gió ngoài khơi chỉ hiện 62 nội dung về ĐGNK.
- Luật Dầu khí 10/2026 và 12/2022 chuyển sang lĩnh vực Sản phẩm mới; NĐ 100/2025 chuyển sang Dùng chung.
- Mục mới "Khóa học điện gió" (Phát triển năng lực): 12 bài, 20 câu hỏi thử thách, 4 công cụ tính toán (Phân phối Weibull; Tốc độ gió theo độ cao; Công suất đầu ra; Tài nguyên gió và hiệu quả kinh tế – AEP, CF, P90, LCOE, NPV, IRR, độ nhạy).
- Excel dữ liệu thêm sheet KhoaHoc_Bai, KhoaHoc_CauHoi, KhoaHoc_Nguon, TuabinThamChieu và cột "Lĩnh vực cần đọc" ở sheet TrongTam.

## Phiên bản 3.0.1–3.0.3 – 20/10/2026
- Giảm dung lượng PDF bản quét, chia gói tải lên GitHub; trang Cập nhật dữ liệu ghi rõ vị trí tệp du-lieu.enc.js.

## Phiên bản 3.0 – 20/10/2026
- Văn bản pháp lý: bổ sung 15 văn bản nhận ngày 19/10/2026; tổng 55 văn bản.
- Tab mới "Nội dung cần đọc": 105 điều, khoản được tô vàng trong 23 văn bản; mỗi mục mở được nguyên văn (đoạn cần đọc tô vàng) và mở PDF đúng trang.
- Thư mục `tai-lieu/`: bản PDF đã đánh dấu vàng và tệp Word gốc của các văn bản công khai. Văn bản nội bộ không đưa lên.
- Bảng dẫn chiếu điều khoản: 76 dòng (thêm 26 dòng).
- Phát triển năng lực: thêm "Từ điển điện gió ngoài khơi" (1.967 thuật ngữ) và "Bản tin thị trường tuần".
- Dự án, khu vực ưu tiên: thêm danh mục dự án ĐGNK theo Bảng 18, Phụ lục III, QĐ 768/QĐ-TTg.
- Trang Tổng quan: thêm tóm tắt bản tin tuần.
- Quản trị: thêm trang "Cập nhật dữ liệu" (đọc Excel → kiểm tra → xem thử → tải `du-lieu.enc.js`, mã hóa bằng tài khoản đang đăng nhập).
- Excel dữ liệu: các sheet cần cập nhật hằng tuần có tab vàng và ô vàng; sheet `0_HuongDan` có các bước cập nhật.
- Công cụ `cong-cu/cap-nhat-du-lieu.html`: mã hóa từ Excel, đổi tài khoản và mật khẩu.
- Tìm kiếm toàn trang: tìm thêm trong từ điển và bản tin.

## Phiên bản 2.0 – 19/10/2026
- Trang đăng nhập có ảnh động điện gió, logo và khẩu hiệu PVEP; dữ liệu mã hóa AES-256-GCM.
- Kho văn bản theo lĩnh vực, bảng dẫn chiếu điều khoản (ĐGNK, CCS/CCUS), mục Đào tạo, nút Tìm kiếm và Lưu Excel.
