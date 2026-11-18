# Tạo bài Post mạng xã hội

Trang web tĩnh để tạo nhanh một bài post kiểu mạng xã hội rồi xuất thành ảnh PNG.

## Cách dùng

1. Mở trang web.
2. Chọn 1 trong 8 avatar.
3. Khi chọn avatar, ô **nickname** tự điền nickname tương ứng với ảnh đó — bạn vẫn sửa lại nickname trong ô được.
4. Nhập **địa điểm**, **thời gian** và **caption**.
5. Xem trước bài post ở khung bên phải — mọi thay đổi hiện ngay lập tức.
6. Bấm **“Xuất bài post thành ảnh PNG”** để tải file `bai-post.png` về máy.

## Avatar

Ảnh avatar là các file PNG trong thư mục `avatars/` (`avatar-1.png` … `avatar-8.png`).
Mỗi ảnh gắn với 1 nickname trong mảng `AVATARS` ở cuối file `index.html`:

```js
{ src: "avatars/avatar-1.png", nickname: "Minh Anh" }
```

Muốn đổi avatar thì thay file PNG trong `avatars/` (giữ nguyên tên file) hoặc thêm dòng mới
vào mảng `AVATARS` với đường dẫn và nickname tương ứng. Ảnh nên là hình vuông (ví dụ 512×512),
vì trang hiển thị avatar dạng hình tròn.

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
