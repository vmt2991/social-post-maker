# Tạo bài Post mạng xã hội

Trang web tĩnh để tạo nhanh một bài post kiểu mạng xã hội rồi xuất thành ảnh PNG.

## Cách dùng

1. Mở trang web.
2. Chọn 1 trong 8 avatar.
3. Nhập **nickname**, **địa điểm**, **thời gian** và **caption**.
4. Xem trước bài post ở khung bên phải — mọi thay đổi hiện ngay lập tức.
5. Bấm **“Xuất bài post thành ảnh PNG”** để tải file `bai-post.png` về máy.

## Chạy local

Mở trực tiếp file `index.html` bằng trình duyệt, hoặc chạy:

```bash
python3 -m http.server 8000
```

rồi mở http://localhost:8000

## Deploy

Repo này được deploy bằng GitHub Pages từ nhánh `main`, thư mục gốc `/`.

Trang live: https://vmt2991.github.io/social-post-maker/

## Công nghệ

- HTML + CSS + JavaScript thuần, không cần build.
- Xuất ảnh bằng [html2canvas](https://html2canvas.hertzen.com/) (tải qua CDN).
