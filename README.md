# nepnha
Giữ những điều xưa, trao nếp nhà mai sau.

Website HTML tĩnh của Nếp nhà, không cần cài thư viện hoặc chạy build.

## GitHub Pages

Địa chỉ sau khi bật Pages: https://vinhnotes.github.io/nepnha/

1. Mở https://github.com/vinhnotes/nepnha/settings/pages.
2. Trong **Build and deployment → Source**, chọn **GitHub Actions**.
3. Trong tab **Actions**, chọn **Deploy GitHub Pages → Run workflow → main** nếu lần chạy đầu chưa thành công.

Workflow tự triển khai lại sau mỗi lần push vào `main`. Các trang HTML,
tệp SEO bên dưới và `.nojekyll` được đóng gói để xuất bản.

- `index.html`: Trang chủ.
- `privacy_policy.html`: Chính sách bảo mật.
- `term.html`: Điều khoản sử dụng.
- `sitemap.xml`: Sitemap chứa URL chuẩn của 3 trang công khai.
- `robots.txt`: Khai báo cho crawler và địa chỉ sitemap.
- `llms.txt`: Tóm tắt website và liên kết nội dung dành cho trợ lý AI.
- `llm.txt`: Bản tương thích có cùng nội dung với `llms.txt`.

## SEO và nội dung cho AI

Mỗi trang có canonical URL, liên kết sitemap và liên kết đến `llms.txt`.
Sitemap dùng địa chỉ `https://vinhnotes.github.io/nepnha/`; khi đổi tên miền
hoặc đường dẫn triển khai, cập nhật URL trong các trang HTML, sitemap,
robots và cả hai tệp `llms.txt` / `llm.txt`. Giữ nội dung hai tệp này đồng bộ.
Khi thêm hoặc xóa trang công khai, cập nhật sitemap và danh sách trong hai tệp AI.

Trên GitHub Pages dạng project, `robots.txt` nằm tại `/nepnha/robots.txt`.
Crawler chỉ tự đọc robots tại gốc host (`https://vinhnotes.github.io/robots.txt`),
nên cần cấu hình tệp ở website gốc nếu muốn khai báo sitemap qua robots.
Có thể gửi trực tiếp `https://vinhnotes.github.io/nepnha/sitemap.xml` trong
Google Search Console của website. `llms.txt` hỗ trợ AI đọc hiểu nội dung,
không bảo đảm tăng thứ hạng tìm kiếm.

Các liên kết nội bộ dùng đường dẫn tương đối để hoạt động trong `/nepnha/`.
Ảnh đã được nhúng trong HTML; phông chữ tải từ Google Fonts.
Các nút App Store và Google Play hiện dùng `href="#"`; cần bổ sung URL
ứng dụng thật khi ứng dụng được phát hành.

## Xem tại máy

Chạy `python3 -m http.server 8000`, sau đó mở http://localhost:8000.
