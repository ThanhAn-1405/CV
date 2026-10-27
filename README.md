# Portfolio CV - Phạm Thành An

## Tên dự án

**Portfolio CV cá nhân của Phạm Thành An**

## Mô tả

Website giới thiệu hồ sơ cá nhân dành cho Frontend Developer. Trang trình bày phần giới thiệu, kỹ năng, các dự án tiêu biểu và thông tin liên hệ; bố cục được thiết kế responsive để sử dụng trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị thông tin cá nhân, vai trò nghề nghiệp và mô tả ngắn.
- Trình bày kỹ năng và dự án bằng bố cục dạng lưới.
- Cung cấp liên kết liên hệ qua email, GitHub và LinkedIn.
- Tương thích với các kích thước màn hình khác nhau.

## Công nghệ

- HTML5: cấu trúc nội dung và các vùng ngữ nghĩa.
- CSS3: giao diện, Flexbox, CSS Grid và responsive design.
- Không sử dụng framework, thư viện JavaScript, công cụ build hoặc cơ sở dữ liệu.
- Ảnh minh họa hiện được tải từ các URL bên ngoài; cần kết nối Internet để hiển thị các ảnh này.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để mở trực tiếp: không cần cài thêm phần mềm.
- Để chạy máy chủ cục bộ: Python 3 (tùy chọn).
- Để chạy bằng container: Docker Engine hoặc Docker Desktop đang hoạt động (tùy chọn).
- Không cần Node.js, npm hoặc bước biên dịch.

## Cài đặt

Tải hoặc sao chép mã nguồn về máy, sau đó mở thư mục dự án. Cấu trúc chính:

```text
.
├── index.html
├── README.md
└── assets/
	├── css/
	│   └── styles.css
	└── img/
```

Không cần cài đặt các gói phụ thuộc. Có thể mở `index.html` trực tiếp bằng trình duyệt hoặc chạy máy chủ cục bộ theo hướng dẫn bên dưới.

## Cấu hình và tùy chỉnh

- Nội dung, tiêu đề trang, mô tả SEO và các liên kết nằm trong `index.html`.
- Giao diện, màu sắc, bố cục và breakpoint nằm trong `assets/css/styles.css`.
- Thay ảnh mẫu bằng ảnh cá nhân hoặc ảnh dự án phù hợp. Có thể lưu ảnh trong `assets/img/` rồi cập nhật đường dẫn `src` trong `index.html`.
- Cập nhật email `an.pham@example.com` cùng các liên kết GitHub và LinkedIn mẫu trước khi phát hành.
- Các liên kết dự án hiện đang là `#`; hãy thay bằng URL dự án thật nếu có.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Nếu lệnh `py` không có sẵn nhưng Python đã được cài, thử `python -m http.server 8000`. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Nếu chưa có Python 3, cài Python 3 bằng trình quản lý gói của bản phân phối hoặc mở `index.html` trực tiếp. Dừng máy chủ bằng `Ctrl+C`.

### Docker

Cần cài và khởi động Docker trước. Tại thư mục dự án, chạy lệnh tương ứng:

**Windows PowerShell:**

```powershell
docker run --rm --name portfolio-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS hoặc Linux:**

```bash
docker run --rm --name portfolio-cv -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Sau khi container khởi động, truy cập [http://localhost:8080](http://localhost:8080). Lệnh trên dùng Nginx để phục vụ trực tiếp thư mục dự án, không cần Dockerfile. Dừng container bằng `Ctrl+C`; nếu chạy container ở chế độ nền, dùng `docker stop portfolio-cv`.

## Thông tin liên hệ

- **Tên:** Phạm Thành An
- **Email:** an.pham@example.com (địa chỉ mẫu, cần thay bằng email thật)
- **GitHub:** github.com/phamthanhan (liên kết mẫu)
- **LinkedIn:** linkedin.com/in/phamthanhan (liên kết mẫu)

Vui lòng cập nhật các thông tin trên trong `index.html` trước khi chia sẻ website.
