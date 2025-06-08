# BlueMoon Fees - Hệ Thống Quản Lý Phí Dịch Vụ Cộng Đồng

![BlueMoon Fees](https://img.shields.io/badge/Version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![React](https://img.shields.io/badge/React-18.2.0-61DAFB.svg)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1.0-6DB33F.svg)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1.svg)

## Mục Lục
- [Giới Thiệu](#giới-thiệu)
- [Tính Năng](#tính-năng)
- [Công Nghệ Sử Dụng](#công-nghệ-sử-dụng)
- [Cấu Trúc Dự Án](#cấu-trúc-dự-án)
- [Cài Đặt & Chạy Dự Án](#cài-đặt--chạy-dự-án)
- [Hướng Dẫn Sử Dụng](#hướng-dẫn-sử-dụng)
- [API Documentation](#api-documentation)



## Giới Thiệu

BlueMoon Fees là một hệ thống quản lý phí dịch vụ cộng đồng toàn diện, được thiết kế để giúp các khu dân cư, tòa nhà, và cộng đồng quản lý hiệu quả các khoản thu, hộ khẩu, nhân khẩu, và dịch vụ tiện ích.

### Mục Tiêu Dự Án
- Số hóa quy trình quản lý phí dịch vụ cộng đồng
- Tăng tính minh bạch trong việc thu chi
- Giảm thiểu sai sót và tiết kiệm thời gian
- Cung cấp báo cáo thống kê chi tiết

### Vấn Đề Giải Quyết
- Quản lý thông tin hộ khẩu và nhân khẩu phức tạp
- Theo dõi các khoản thu và thanh toán khó khăn
- Thiếu công cụ thống kê và báo cáo
- Quy trình thủ công dễ sai sót

## Tính Năng

### 🏠 Quản Lý Hộ Khẩu
- Thêm, sửa, xóa thông tin hộ khẩu
- Quản lý thành viên trong hộ gia đình
- Lịch sử thay đổi hộ khẩu

### 👥 Quản Lý Nhân Khẩu
- Quản lý thông tin cá nhân chi tiết
- Theo dõi tình trạng tạm trú/tạm vắng
- Liên kết với hộ khẩu

### 💰 Quản Lý Khoản Thu
- Tạo và quản lý các khoản thu (bắt buộc/tự nguyện)
- Theo dõi tình trạng thanh toán
- Phân quyền phê duyệt

### 🔧 Quản Lý Dịch Vụ Tiện Ích
- Quản lý điện, nước, internet
- Tính toán chi phí dựa trên chỉ số
- Báo cáo tiêu thụ

### 🚗 Quản Lý Phương Tiện
- Đăng ký xe máy, ô tô
- Quản lý phí gửi xe

### 📊 Thống Kê & Báo Cáo
- Dashboard tổng quan
- Báo cáo tài chính chi tiết
- Thống kê theo thời gian

### 🔐 Phân Quyền Người Dùng
- **Admin**: Toàn quyền quản lý
- **Tổ Trưởng**: Quản lý hộ khẩu, nhân khẩu
- **Kế Toán**: Quản lý tài chính, khoản thu

## Công Nghệ Sử Dụng

### Frontend
- **React.js** 18.2.0 - Framework JavaScript
- **Material-UI** - Thư viện UI components
- **React Router** - Điều hướng ứng dụng
- **Axios** - HTTP client
- **Recharts** - Thư viện biểu đồ

### Backend
- **Java** 17 - Ngôn ngữ lập trình
- **Spring Boot** 3.1.0 - Framework backend
- **Spring Security** - Bảo mật ứng dụng
- **JWT** - Authentication token
- **JPA/Hibernate** - ORM framework
- **MySQL** 8.0 - Cơ sở dữ liệu

### DevOps & Tools
- **Maven** - Quản lý dependencies
- **Git** - Version control
- **VS Code** - IDE

## Cấu Trúc Dự Án

```
├── frontend/                    # React Frontend
│   ├── public/
│   ├── src/
│   │   ├── components/         # React Components
│   │   │   ├── auth/          # Authentication
│   │   │   ├── dashboard/     # Dashboard
│   │   │   ├── household/     # Quản lý hộ khẩu
│   │   │   ├── person/        # Quản lý nhân khẩu
│   │   │   ├── fee/           # Quản lý khoản thu
│   │   │   ├── utility/       # Dịch vụ tiện ích
│   │   │   ├── vehicle/       # Quản lý phương tiện
│   │   │   └── common/        # Components dùng chung
│   │   ├── services/          # API services
│   │   ├── utils/             # Utilities
│   │   └── App.js
│   └── package.json
├── backend/                     # Spring Boot Backend
│   ├── src/main/java/com/bluemoon/fees/
│   │   ├── config/            # Configuration
│   │   ├── controller/        # REST Controllers
│   │   ├── dto/               # Data Transfer Objects
│   │   ├── entity/            # JPA Entities
│   │   ├── repository/        # Data Repositories
│   │   ├── security/          # Security Configuration
│   │   └── service/           # Business Logic
│   └── pom.xml
└── README.md
```

## Cài Đặt & Chạy Dự Án

### Yêu Cầu Hệ Thống
- **Node.js** >= 14.0.0
- **Java Development Kit (JDK)** 17
- **MySQL** >= 8.0
- **Maven** >= 3.6.0
- **Git**

### Bước 1: Clone Repository
```bash
git clone https://github.com/lyng148/KTPM-project.git
cd KTPM-project
```

### Bước 2: Cấu Hình Database
1. Tạo database MySQL:
```sql
CREATE DATABASE bluemoon_fees;
```

2. Cập nhật file `backend/src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/bluemoon_fees
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### Bước 3: Chạy Backend
```bash
cd backend
./mvnw spring-boot:run
```
Backend sẽ chạy tại: `http://localhost:8080`

### Bước 4: Chạy Frontend
```bash
cd frontend
npm install --legacy-peer-deps
npm start
```
Frontend sẽ chạy tại: `http://localhost:3000`

## Hướng Dẫn Sử Dụng

### Đăng Nhập Hệ Thống
**Tài khoản mặc định:**
- **Username**: `admin`
- **Password**: `admin123`

### Các Chức Năng Chính

#### 1. Quản Lý Hộ Khẩu
- Truy cập: **Hộ khẩu** → **Thêm hộ khẩu**
- Điền thông tin: Chủ hộ, địa chỉ, số điện thoại
- Quản lý thành viên trong hộ

#### 2. Quản Lý Nhân Khẩu
- Truy cập: **Nhân khẩu** → **Thêm nhân khẩu**
- Nhập thông tin cá nhân đầy đủ
- Liên kết với hộ khẩu tương ứng

#### 3. Tạo Khoản Thu
- Truy cập: **Khoản thu** → **Thêm khoản thu**
- Chọn loại: Bắt buộc/Tự nguyện
- Thiết lập thời hạn và số tiền

#### 4. Quản Lý Thanh Toán
- Truy cập: **Thanh toán**
- Xác nhận các khoản đã thu
- Xuất báo cáo tài chính

## API Documentation

### Authentication
```
POST /api/auth/login
POST /api/auth/register
```

### Household Management
```
GET    /api/households
POST   /api/households
PUT    /api/households/{id}
DELETE /api/households/{id}
GET    /api/households/{id}/members
POST   /api/households/{id}/members
DELETE /api/households/{hoKhauId}/members/{nhanKhauId}
```

### Person Management
```
GET    /api/persons
POST   /api/persons
PUT    /api/persons/{id}
DELETE /api/persons/{id}
```

### Fee Management
```
GET    /api/fees
POST   /api/fees
PUT    /api/fees/{id}
DELETE /api/fees/{id}
```

### Payment Management
```
GET    /api/payments
POST   /api/payments
PUT    /api/payments/{id}
```

### Utility Services
```
GET    /api/utilities
POST   /api/utilities
PUT    /api/utilities/{id}
DELETE /api/utilities/{id}
```



⭐ **Nếu dự án này hữu ích cho bạn, hãy cho chúng tôi một star trên GitHub!**

