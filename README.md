# Remak Backend (NestJS + TypeScript)

Đây là hệ thống quản trị và cung cấp API (Backend) phục vụ cho dự án website **Remak (tieuam.com)**. Hệ thống được xây dựng trên nền tảng **NestJS** - một Node.js framework cấp tiến, mạnh mẽ, dễ mở rộng và viết bằng TypeScript.

---

## 🚀 Các chức năng cốt lõi (Core Features)

1. **API Tư vấn & Yêu cầu giải pháp**: Tiếp nhận thông tin tìm kiếm, giải quyết bài toán không gian (cách âm, cách nhiệt,...) gửi về từ giao diện frontend.
2. **Quản lý Danh mục & Sản phẩm**: Cung cấp dữ liệu sản phẩm, vật liệu tiêu âm, cách âm, cách nhiệt, bảo ôn,... cho website.
3. **Quản trị cấu hình**: Quản lý thông tin liên hệ, hotline, các thẻ từ khóa phổ biến của hệ thống.

---

## 🛠️ Công nghệ sử dụng (Tech Stack)

* **Framework**: [NestJS](https://nestjs.com/) (với bộ CLI quản lý mạnh mẽ)
* **Ngôn ngữ**: TypeScript
* **Kiểm thử**: Jest & Supertest (E2E và Unit Test)
* **Định dạng code**: ESLint & Prettier

---

## 📂 Cấu trúc dự án (Project Structure)

```text
backend/
├── src/
│   ├── app.controller.ts    # Controller tiếp nhận request chính
│   ├── app.module.ts        # Module gốc kết nối cơ sở dữ liệu và controller
│   ├── app.service.ts       # Xử lý logic nghiệp vụ chính
│   └── main.ts              # File khởi chạy ứng dụng (Port mặc định: 3000/3001)
├── test/
│   ├── app.e2e-spec.ts      # Kiểm thử tích hợp đầu cuối (E2E)
│   └── jest-e2e.json        # Cấu hình Jest cho kiểm thử E2E
├── nest-cli.json            # Cấu hình NestJS CLI
├── tsconfig.json            # Cấu hình TypeScript compiler
└── package.json             # Danh sách dependencies và npm scripts
```

---

## 💻 Hướng dẫn chạy dự án (Getting Started)

### 1. Cài đặt các thư viện phụ thuộc
Di chuyển vào thư mục `backend` và cài đặt:
```bash
npm install
```

### 2. Thiết lập biến môi trường (Environment Variables)
Sao chép file `.env.example` thành file `.env` cục bộ và cập nhật các cấu hình kết nối (Cơ sở dữ liệu, Cổng chạy,...):
```bash
cp .env.example .env
```
*Lưu ý: File `.env` chứa mật khẩu thực tế đã được chặn thông qua `.gitignore` không đẩy lên Git.*

### 3. Vận hành dự án (Compile and run)

```bash
# Chạy ở chế độ phát triển (Phát hiện thay đổi và tự khởi động lại - Khuyên dùng)
npm run start:dev

# Chạy ở chế độ thường
npm run start

# Chạy bản build production
npm run start:prod
```

### 4. Chạy kiểm thử (Testing)

```bash
# Chạy Unit Tests
npm run test

# Chạy E2E (End-to-End) Tests
npm run test:e2e

# Đo lường độ bao phủ kiểm thử (Test Coverage)
npm run test:cov
```

---

## 🏗️ Biên dịch đóng gói (Build Production)
Biên dịch ứng dụng TypeScript thành mã nguồn Javascript thuần trong thư mục `/dist` để sẵn sàng deploy lên môi trường Production:
```bash
npm run build
```
