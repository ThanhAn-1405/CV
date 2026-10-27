# Báo cáo kiểm thử

## Thông tin chung

- **Sản phẩm:** Website portfolio CV cá nhân
- **Ngày kiểm thử:** 27/10/2026
- **Phạm vi:** Kiểm tra tĩnh mã nguồn HTML/CSS và chạy thử `index.html` trên trình duyệt.
- **Môi trường:** Microsoft Edge; chế độ xem desktop và mobile; trang được mở cục bộ bằng `file://`.
- **Giới hạn:** Đây là kiểm tra thủ công trong phạm vi giao diện hiện có, không thay thế kiểm thử bảo mật chuyên sâu, kiểm thử nhiều trình duyệt hoặc kiểm thử triển khai trên hosting.

## Kết quả theo tiêu chí

### 1. Tính đúng đắn — Đạt một phần

- Trang mở được; tiêu đề và các khu vực Giới thiệu, Kỹ năng, Dự án, Liên hệ và chân trang được hiển thị.
- Đã kiểm tra liên kết điều hướng **Kỹ năng**; trang chuyển đến đúng đích `#skills`.
- Trong lần chạy thử, cả 5 ảnh đều tải thành công. Ở chiều rộng nội dung 375 CSS px, lưới dự án hiển thị một cột; ở desktop 1425 CSS px, lưới hiển thị ba cột.
- **Lỗi cần xử lý:** Một số nội dung viết `& amp;` thay vì `&amp;`, nên giao diện hiển thị nguyên văn “& amp;” trong chức danh và kỹ năng.
- Một số liên kết dự án, GitHub và LinkedIn vẫn dùng `href="#"`; metadata tác giả/mô tả trong `<head>` còn ghi tên Nguyễn Văn An thay vì Phạm Thành An.

### 2. UI/UX — Đạt một phần

- Bố cục có điều hướng, nội dung chia khu vực rõ ràng, thẻ dự án và liên kết quay đầu trang.
- CSS có breakpoint cho mobile, tablet và desktop; kiểm tra ở kích thước mobile và desktop cho thấy lưới dự án thay đổi số cột tương ứng.
- Có trạng thái `focus-visible` và hỗ trợ `prefers-reduced-motion`.
- Ảnh chụp mobile và desktop được lưu trong thư mục minh chứng bên dưới.
- **Hạn chế:** Nội dung một số liên kết chưa hoàn thiện; ảnh minh họa và bảng màu hiện tại có thể chưa phù hợp để phát hành như hồ sơ cá nhân chính thức. Chưa thực hiện đánh giá khả năng tiếp cận hoặc đo độ tương phản bằng công cụ chuyên dụng.

### 3. Khả năng vận hành - xử lý lỗi — Đạt một phần

- Có thể mở trực tiếp bằng trình duyệt mà không cần cài gói phụ thuộc hoặc biên dịch.
- Điều hướng nội bộ hoạt động trong lần chạy thử.
- Đây là trang tĩnh, không có luồng nhập liệu hay xử lý nghiệp vụ để kiểm thử lỗi đầu vào.
- **Hạn chế:** Ảnh được tải từ máy chủ bên ngoài; nếu mất kết nối hoặc nguồn ảnh thay đổi, ảnh có thể không hiển thị. Các liên kết `#` chưa dẫn đến nội dung dự án hoặc hồ sơ mạng xã hội thật.

### 4. Bảo mật — Đạt trong phạm vi trang tĩnh

- Trong mã nguồn được kiểm tra, trang không có biểu mẫu nhập liệu, mã JavaScript, xác thực, lưu trữ dữ liệu người dùng hoặc dịch vụ backend.
- Chưa thấy luồng xử lý dữ liệu đầu vào để kiểm tra các lỗi như injection trong phạm vi chức năng hiện tại.
- **Giới hạn đánh giá:** Không thực hiện pentest, quét lỗ hổng, kiểm tra HTTP security headers hoặc đánh giá cấu hình hosting. Ảnh được tải từ các tên miền bên ngoài, vì vậy trình duyệt sẽ gửi yêu cầu đến các nguồn đó.

### 5. Chất lượng mã nguồn — Đạt một phần

- Cấu trúc nội dung dùng HTML có ngữ nghĩa; CSS tách riêng, có tổ chức theo khu vực và dùng Flexbox/Grid cùng biến CSS.
- Dự án không có phụ thuộc build hoặc framework bên thứ ba.
- **Các điểm cần cải thiện:** Sửa các entity `& amp;`; đồng bộ metadata với tên hiển thị; thay các URL mẫu/`#` bằng liên kết thật. Chưa chạy HTML validator, linter hoặc kiểm tra tự động về khả năng tiếp cận.

### 6. Khả năng triển khai — Đạt một phần

- Cấu trúc hiện tại phù hợp để triển khai như website tĩnh: `index.html` cùng thư mục `assets/`; không cần bước build.
- Đã mở trang cục bộ thành công trên trình duyệt. README có hướng dẫn chạy máy chủ cục bộ và phục vụ bằng Nginx/Docker.
- **Chưa xác minh:** Chưa triển khai lên hosting hoặc chạy thử qua máy chủ HTTP trong lần kiểm thử này; chưa kiểm tra cấu hình domain, HTTPS, cache, bảo mật headers hay pipeline CI/CD.
- Trước khi phát hành công khai, cần cập nhật email/liên kết mẫu và cân nhắc lưu ảnh trong dự án để giảm phụ thuộc vào nguồn bên ngoài.

## Minh chứng hình ảnh

Ảnh do người kiểm thử chụp từ trang đang chạy trong trình duyệt:

- Desktop: [desktop.png](./screenshots/desktop.png)
- Mobile: [mobile.png](./screenshots/mobile.png)

## Kết luận

Trang portfolio tĩnh có thể mở và hiển thị các khu vực chính; điều hướng nội bộ và bố cục responsive cơ bản hoạt động trong các kích thước đã kiểm tra. Trước khi phát hành chính thức, nên sửa lỗi entity và metadata, thay liên kết mẫu, đồng thời kiểm thử lại trên hosting qua HTTP/HTTPS.