# Báo cáo kiểm thử - Portfolio CV

**Ngày kiểm thử:** 2026-10-27  
**Đối tượng:** Trang portfolio tĩnh (`index.html`, `assets/css/styles.css`)  
**Phương pháp:** Kiểm tra cấu trúc mã nguồn và mở trang bằng trình duyệt tích hợp. Đây là kiểm thử thủ công, không thay thế kiểm thử tự động hoặc đánh giá bảo mật chuyên sâu.

## 1. Tính đúng đắn

**Kết quả: Đạt có điều kiện.** Trang mở được trong trình duyệt và hiển thị tiêu đề, phần giới thiệu, kỹ năng, dự án, liên hệ và chân trang. Các mục điều hướng trỏ đến các section tương ứng (`#about`, `#skills`, `#projects`, `#contact`). Các nút và liên kết dự án được khai báo, nhưng liên kết chi tiết dự án hiện trỏ `#`; GitHub và LinkedIn cũng là placeholder. Nội dung Todo List và Weather Dashboard chỉ là mô tả dự án, không phải chức năng chạy được trên trang.

## 2. UI/UX

**Kết quả: Đạt một phần.** Giao diện desktop đã được mở và quan sát trực tiếp; cấu trúc có điều hướng, nút hành động, phân nhóm nội dung và lưới dự án. CSS triển khai mobile-first, có breakpoint tablet từ 768px và desktop từ 1280px, cùng Flexbox/Grid để sắp xếp nội dung. Chưa xác nhận trực quan trên thiết bị hoặc viewport mobile trong lần kiểm thử này. Ảnh đại diện hiện là hình minh họa, không phải ảnh chân dung.

## 3. Khả năng vận hành - xử lý lỗi

**Kết quả: Đạt trong phạm vi trang tĩnh; chưa đánh giá xử lý lỗi.** Trang HTML/CSS tải trong trình duyệt mà không cần dịch vụ backend. Vì trang hiện không có luồng dữ liệu động, biểu mẫu gửi đi hoặc xử lý API thực tế, chưa có cơ sở để đánh giá trạng thái lỗi mạng, xác thực dữ liệu hay phục hồi khi dịch vụ lỗi. Chưa chạy kiểm thử tải hoặc tự động.

## 4. Bảo mật

**Kết quả: Chưa kiểm thử chuyên sâu; rủi ro ứng dụng thấp theo phạm vi hiện tại.** Repo đang phục vụ nội dung tĩnh, không thấy mã backend, đăng nhập, lưu trữ dữ liệu nhạy cảm hoặc xử lý đầu vào người dùng trong trang. Không thực hiện quét lỗ hổng, kiểm thử cấu hình máy chủ hay đánh giá dependency. Cần kiểm tra lại nếu bổ sung API, form hoặc dịch vụ bên ngoài.

## 5. Chất lượng mã nguồn

**Kết quả: Đạt cơ bản.** HTML có khai báo ngôn ngữ, metadata, vùng ngữ nghĩa và nội dung thay thế cho ảnh; CSS được tách riêng, dùng biến thiết kế, Flexbox/Grid và breakpoint responsive. Hạn chế: nhiều chú thích mô tả dày trong HTML/CSS; một số liên kết còn là `#`; thông tin email và mạng xã hội là dữ liệu mẫu. Chưa chạy validator HTML/CSS hoặc công cụ phân tích tĩnh.

## 6. Khả năng triển khai

**Kết quả: Có thể triển khai dưới dạng website tĩnh.** Trang không yêu cầu bước build hay cài dependency; có thể phục vụ bằng web server tĩnh như Nginx. README đã mô tả cách mở/chạy trên Windows, macOS, Linux và Docker. Trong lần kiểm thử này chưa chạy Docker image hoặc triển khai lên hosting, vì vậy các bước đó chưa được xác minh thực tế.

## Minh chứng hình ảnh

Ảnh chụp trang đã được xem trong trình duyệt tích hợp khi kiểm tra desktop, nhưng chưa được lưu vào `docs/screenshots/`. Thư mục này hiện chưa có tệp ảnh; ảnh desktop và mobile cần được chụp/lưu để hoàn tất minh chứng. Báo cáo không tham chiếu đến ảnh chưa tồn tại.

## Tổng kết

Trang tĩnh tải và hiển thị được trong trình duyệt; cấu trúc responsive và các vùng nội dung chính hiện diện trong mã nguồn. Các nội dung cần ưu tiên trước khi phát hành là thay liên kết/thông tin mẫu, xác minh ảnh đại diện, kiểm tra trực quan trên mobile, và chạy thử Docker/hosting. Minh chứng ảnh lưu trong repo và các kiểm thử chuyên sâu vẫn còn thiếu.