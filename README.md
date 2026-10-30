
I. Bản thiết kế phân quyền an toàn (Permission Matrix)

Để bảo vệ thông tin nhạy cảm (SĐT, mức lương kỳ vọng), hệ thống quyền truy cập được phân cấp nghiêm ngặt như sau:

Đối tượng	Mức quyền thiết lập	Hành vi được phép	Hành vi bị cấm / Giới hạn
Trưởng phòng Nhân sự (Chủ sở hữu)	Owner / Editor	Toàn quyền chỉnh sửa, duyệt các đóng góp, quản lý chia sẻ và xem lịch sử chỉnh sửa.	Không chia sẻ quyền Editor cho bất kỳ ai ngoài bộ phận HR.
Các Trưởng bộ phận (Chuyên môn)	Commenter (Người nhận xét)	Xem toàn bộ danh sách, tạo nhận xét (Comment), viết đề xuất chỉnh sửa qua Suggesting Mode.	Không được sửa trực tiếp vào ô dữ liệu, không được tải về (Download), sao chép (Copy) hoặc in ấn.
Ứng viên / Đối tác bên ngoài	Không có quyền (No Access)	Không thể mở link, không thể tìm thấy file.	Bị chặn hoàn toàn quyền truy cập.

Cấu hình bảo mật bổ sung (Bắt buộc):
• Trong cài đặt chia sẻ nâng cao của file, Owner phải bỏ tích tùy chọn: "Người chỉnh sửa có thể thay đổi quyền và chia sẻ" (Editors can change permissions and share).
• Bật tính năng chặn sao chép: Tích chọn "Tắt tùy chọn tải xuống, in và sao chép đối với người xem và người nhận xét" (Disable options to download, print, and copy for commenters and viewers).

II. Kịch bản xử lý sự cố: Quy trình 3 bước khẩn cấp

Khi phát hiện link quyền Editor bị gửi nhầm cho ứng viên, bộ phận HR cần thực hiện ngay lập tức quy trình 3 bước sau:

Bước 1: Thu hồi quyền truy cập và Đổi trạng thái chia sẻ (Revoke & Restrict)

• Hành động:
	• Vào mục Chia sẻ (Share) của file danh sách \(\rightarrow \) Tìm tên hoặc email của ứng viên (nếu chia sẻ đích danh) và nhấn Xóa quyền (Remove access).
	• Nếu link được gửi ở chế độ "Bất kỳ ai có liên kết đều có quyền Chỉnh sửa" (Anyone with the link can edit), lập tức đổi trạng thái link về Hạn chế (Restricted). Lúc này, chỉ những email được chỉ định đích danh mới mở được file.
• Mục đích: Ngắt kết nối của ứng viên với file ngay lập tức (trong vòng dưới 5 giây).

Bước 2: Kiểm tra lịch sử để xác định mức độ rò rỉ (Access Audit Log)

• Hành động:
	• Mở Nhật ký hoạt động (Activity Dashboard / Audit Log) của file (Biểu tượng mũi tên hình răng cưa hoặc trong menu Tệp \(\rightarrow \) Lịch sử phiên bản).
	• Kiểm tra xem tài khoản của ứng viên (hoặc các tài khoản vô danh - Anonymous) đã truy cập vào file vào khung giờ nào.
	• Xem kỹ Lịch sử phiên bản (Version History) để xác nhận xem họ có thực hiện hành vi sửa đổi dữ liệu nào trên file hay không.
• Giải bẫy dữ liệu (Kiểm tra xem họ đã kịp copy/tải về chưa?):
	• Nếu ứng viên truy cập bằng tài khoản Google/Microsoft cá nhân: Hệ thống sẽ ghi nhận lịch sử xem của tài khoản đó. Nếu bạn đã bật tính năng "Chặn sao chép/tải về" từ trước, họ chắc chắn không thể tải hay copy.
	• Nếu bạn chưa bật tính năng chặn sao chép: Nhật ký hệ thống Cloud thông thường chỉ ghi nhận hành vi "Xem" (View) và "Sửa" (Edit), không ghi nhận hành vi Copy (Ctrl+C) hoặc Tải xuống (Download) của người dùng. Do đó, nếu nhật ký hiển thị ứng viên đã từng trực tuyến (Online) trong file, bạn phải giả định theo Kịch bản rủi ro cao nhất: Ứng viên đã lấy được dữ liệu.

Bước 3: Đóng băng dữ liệu cũ, Tạo bản sao mới và Xử lý khủng hoảng (Migrate & Mitigate)

• Hành động:
	• Tạo file mới: Chọn Tệp \(\rightarrow \) Tạo bản sao (Make a copy) để chuyển toàn bộ dữ liệu sạch sang một file hoàn toàn mới với URL mới. Bật đầy đủ các tính năng chặn sao chép/tải về cho file mới này.
	• Xóa file cũ: Xóa vĩnh viễn file cũ bị lộ liên kết để đảm bảo link cũ vô hiệu hóa hoàn toàn.
	• Liên hệ ứng viên (Nếu cần): Bộ phận HR gửi thư xin lỗi lịch sự, thông báo về sự cố kỹ thuật gửi nhầm liên kết và yêu cầu ứng viên bảo mật thông tin nội bộ (nếu họ vô tình đọc được) để thể hiện sự chuyên nghiệp của doanh nghiệp.
