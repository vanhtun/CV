# Portfolio CV - VÌ ANH TUẤN

## Mô tả

Website portfolio cá nhân giới thiệu thông tin, kỹ năng, dự án và cách liên hệ với VÌ ANH TUẤN, định hướng Frontend Developer. Trang được xây dựng dưới dạng website tĩnh, ưu tiên bố cục responsive và có thể chạy trực tiếp trên trình duyệt hoặc qua một web server tĩnh.

## Chức năng

- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị phần giới thiệu và ảnh đại diện.
- Trình bày kỹ năng và các dự án tiêu biểu.
- Cung cấp các liên kết liên hệ qua email, GitHub và LinkedIn.
- Bố cục tương thích với màn hình điện thoại, máy tính bảng và máy tính.

> Các dự án Todo List và Weather Dashboard hiện được giới thiệu dưới dạng nội dung portfolio; chúng không phải ứng dụng tương tác được triển khai trong repo này.

## Công nghệ

- HTML5: cấu trúc nội dung và các vùng ngữ nghĩa.
- CSS3: giao diện, Flexbox, CSS Grid và responsive design.
- Docker tùy chọn: phục vụ website bằng Nginx.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để mở trực tiếp: không cần cài thêm công cụ.
- Để chạy web server cục bộ: Python 3 (hoặc Python launcher trên Windows).
- Để chạy bằng container: Docker Engine/Desktop đang hoạt động.
- Không cần Node.js, npm, cơ sở dữ liệu hay file cấu hình môi trường.

## Cài đặt

Tải mã nguồn hoặc clone repository về máy, sau đó mở terminal tại thư mục gốc của dự án (thư mục chứa `index.html`). Nếu clone từ Git, thay `<URL_REPOSITORY>` bằng URL repository thực tế:

```bash
git clone <URL_REPOSITORY>
cd CV-main
```

Nếu đã có mã nguồn trên máy, chỉ cần mở terminal tại thư mục đó. Không cần cài dependency.

## Cấu hình

Website không có bước cấu hình môi trường hay file `.env`. Có thể cá nhân hóa trực tiếp trong mã nguồn:

- Sửa tên, mô tả và nội dung các mục trong `index.html`.
- Cập nhật email, GitHub và LinkedIn ở mục Liên hệ. Các liên kết hiện tại đang dùng địa chỉ mẫu hoặc `#`.
- Thay ảnh tại `assets/img/avatar.jpg` để hiển thị ảnh đại diện.
- Cập nhật tên, mô tả và liên kết của từng dự án trong `index.html`.
- Điều chỉnh màu sắc, bố cục và breakpoint responsive trong `assets/css/styles.css`.

## Chạy thử

### Windows

Mở trực tiếp trong trình duyệt bằng PowerShell:

```powershell
Start-Process .\index.html
```

Hoặc dùng Python để chạy server cục bộ:

```powershell
py -m http.server 8000
```

Mở `http://localhost:8000` trong trình duyệt. Dừng server bằng `Ctrl+C`.

### macOS

Mở trực tiếp:

```bash
open index.html
```

Hoặc chạy server cục bộ:

```bash
python3 -m http.server 8000
```

Mở `http://localhost:8000` trong trình duyệt. Dừng server bằng `Ctrl+C`.

### Linux

Mở trực tiếp bằng trình duyệt mặc định:

```bash
xdg-open index.html
```

Hoặc chạy server cục bộ:

```bash
python3 -m http.server 8000
```

Mở `http://localhost:8000` trong trình duyệt. Dừng server bằng `Ctrl+C`.

### Docker

Cần cài và khởi động Docker trước. Chạy lệnh phù hợp với terminal từ thư mục gốc dự án.

PowerShell trên Windows:

```powershell
docker run --rm --name cv-portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

macOS hoặc Linux:

```bash
docker run --rm --name cv-portfolio -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở `http://localhost:8080`. Dừng container bằng `Ctrl+C`. Nếu cổng `8080` đang được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

Thông tin liên hệ được hiển thị trong mục Liên hệ ở cuối trang `index.html`. Hiện email `an.nguyen@example.com` và các liên kết GitHub/LinkedIn là dữ liệu mẫu; hãy thay bằng thông tin thật trước khi phát hành website.
