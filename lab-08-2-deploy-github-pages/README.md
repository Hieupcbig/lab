# Lab 8.2 — Deploy lên GitHub Pages

Lab này là quy trình deploy theo tài liệu. File `index.html`, `style.css`, `script.js` là trang tĩnh mẫu để thử deploy. Tôi không thể tạo repository trong tài khoản cá nhân hoặc push thay bạn; hãy chạy lệnh dưới đây trong terminal sau khi tự tạo repository trống trên GitHub.

## 1. Kiểm tra Git

```bash
git --version
```

Nếu chưa có Git, cài Git for Windows rồi mở lại terminal.

## 2. Tạo repository và push source

Tạo repository trên GitHub (ví dụ `lab-08-2-deploy`). Trong terminal tại thư mục này, chạy:

```bash
git init
git add .
git commit -m "First commit"
git branch -M main
git remote add origin https://github.com/<username>/<repo-name>.git
git push -u origin main
```

Thay `<username>` và `<repo-name>` bằng thông tin repository thật của bạn. Nếu `origin` đã tồn tại, kiểm tra bằng `git remote -v`; không chạy `git remote add origin` lần thứ hai.

## 3. Bật GitHub Pages

1. Mở repository trên GitHub → **Settings** → **Pages**.
2. Trong **Build and deployment**, chọn **Deploy from a branch**.
3. Chọn branch `main`, folder `/(root)`, bấm **Save**.
4. Chờ GitHub build xong; địa chỉ thường có dạng `https://<username>.github.io/<repo-name>/`.

Sau khi chỉnh sửa code:

```bash
git add .
git commit -m "Update website"
git push
```

Địa chỉ deploy chỉ xuất hiện sau khi bạn tự push repository và GitHub Pages hoàn tất deploy.
