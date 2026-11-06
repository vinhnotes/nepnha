# nepnha
Giữ những điều xưa, trao nếp nhà mai sau.

Website HTML tĩnh của Nếp nhà, không cần cài thư viện hoặc chạy build.

## GitHub Pages

Địa chỉ sau khi bật Pages: https://vinhnotes.github.io/nepnha/

1. Mở https://github.com/vinhnotes/nepnha/settings/pages.
2. Trong **Build and deployment → Source**, chọn **GitHub Actions**.
3. Trong tab **Actions**, chọn **Deploy GitHub Pages → Run workflow → main** nếu lần chạy đầu chưa thành công.

Workflow tự triển khai lại sau mỗi lần push vào `main`. Chỉ các trang HTML
và `.nojekyll` được đóng gói để xuất bản.

- `index.html`: Trang chủ.
- `privacy_policy.html`: Chính sách bảo mật.
- `term.html`: Điều khoản sử dụng.

Các liên kết nội bộ dùng đường dẫn tương đối để hoạt động trong `/nepnha/`.
Ảnh đã được nhúng trong HTML; phông chữ tải từ Google Fonts.
Các nút App Store và Google Play hiện dùng `href="#"`; cần bổ sung URL
ứng dụng thật khi ứng dụng được phát hành.

## Xem tại máy

Chạy `python3 -m http.server 8000`, sau đó mở http://localhost:8000.
