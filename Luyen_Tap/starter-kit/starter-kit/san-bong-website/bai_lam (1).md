# BÀI LÀM – HACKATHON 02

- **Mã đề:** 01
- **Họ tên:**
- **Lớp:**
- **Link repository:**
- **Hệ điều hành (Windows/macOS):**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv
mkdir
cd
rm
cp
Get-Content
cd..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
2026-10-28 08:03:17 GET /lich-san status=200
2026-10-28 08:05:28 GET /bang-gia status=200
2026-10-28 08:07:39 GET /tin-tuc status=404
2026-10-28 08:10:50 GET /lien-he status=200
2026-10-28 08:13:01 GET /dat-san-cu status=404
2026-10-28 08:16:12 GET /js/app.js status=304
2026-10-28 08:20:23 GET /images/banner.jpg status=304
2026-10-28 08:24:34 POST /api/thanh-toan status=500
2026-10-28 08:28:45 POST /api/thanh-toan status=500
2026-10-28 08:31:56 GET / status=200
2026-10-28 08:34:07 GET /images/san-7.jpg status=404
2026-10-28 08:37:18 POST /api/thanh-toan status=500
2026-10-28 08:39:29 GET /dat-san status=200
2026-10-28 08:42:40 POST /api/dat-san status=500
2026-10-28 08:45:51 POST /api/thanh-toan status=500
2026-10-28 08:49:02 POST /api/dat-san status=500
2026-10-28 08:53:13 GET /images/banner.jpg status=304
2026-10-28 08:57:24 GET /khuyen-mai status=404
2026-10-28 08:59:35 GET /lich-san status=200
2026-10-28 09:03:46 GET /lich-san status=200

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
Get-Content .\logs\access.log | Select-String "STATUS=500" > .\logs\.\loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
2026-10-28 08:24:34 POST /api/thanh-toan status=500
2026-10-28 08:28:45 POST /api/thanh-toan status=500

```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
(Get-Content .\logs\access.log | Select-String "STATUS=404").Count
```

```text
4
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
.\tong_hop.ps1

```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO SU CO WEBSITE ===

2026-10-28 08:07:39 GET /tin-tuc status=404
2026-10-28 08:13:01 GET /dat-san-cu status=404
2026-10-28 08:34:07 GET /images/san-7.jpg status=404
2026-10-28 08:57:24 GET /khuyen-mai status=404




Count    : 6
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property : 


```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 | netword  |network.png| ghi lại tên logo |
| 2 | console | console.png |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/dat_san_thang_10.xlsx`, không cần ghi vào đây.

