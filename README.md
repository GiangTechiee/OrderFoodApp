# Food Delivery App 🍕

Ứng dụng đặt món ăn Android được phát triển bằng Java với giao diện XML truyền thống, sử dụng Room ORM và SQLite database.

## 📱 Tính năng chính

- **Quản lý món ăn**: Thêm, sửa, xóa và xem danh sách món ăn
- **Đặt hàng**: Tạo và quản lý đơn hàng
- **Tìm kiếm**: Tìm kiếm món ăn theo tên, loại hoặc giá
- **Quản lý danh mục**: Phân loại món ăn theo danh mục
- **Lịch sử đặt hàng**: Xem lại các đơn hàng đã đặt

## 🛠 Công nghệ sử dụng

- **Ngôn ngữ**: Java
- **Giao diện**: XML Layout (Traditional)
- **Database**: SQLite
- **ORM**: Room Database
- **Architecture**: MVVM Pattern
- **IDE**: Android Studio

## 📋 Yêu cầu hệ thống

- Android API Level 21+ (Android 5.0)
- Java 8+
- Android Studio 4.0+
- RAM tối thiểu: 2GB

## 🏗 Cấu trúc dự án

```
app/
├── src/main/java/com/fooddelivery/
│   ├── activity/           # Các Activity chính
│   ├── adapter/            # RecyclerView Adapters
│   ├── database/           # Room Database & DAO
│   ├── model/              # Data Models/Entities
│   ├── repository/         # Data Repository
│   ├── viewmodel/          # ViewModels
│   └── utils/              # Utility classes
├── src/main/res/
│   ├── layout/             # XML Layout files
│   ├── drawable/           # Images & Icons
│   ├── values/             # Colors, Strings, Styles
│   └── menu/               # Menu resources
└── build.gradle           # Dependencies
```

## 🗄 Database Schema

### Entities

**Food**
- id (Primary Key)
- name
- description
- price
- category_id
- image_url
- is_available

**Category**
- id (Primary Key)
- name
- description

**Order**
- id (Primary Key)
- customer_name
- phone
- address
- total_amount
- order_date
- status

**OrderItem**
- id (Primary Key)
- order_id (Foreign Key)
- food_id (Foreign Key)
- quantity
- price

## 🚀 Cài đặt và chạy dự án

1. **Clone repository**
```bash
git clone [URL_REPOSITORY]
cd food-delivery-app
```

2. **Mở project trong Android Studio**
```
File > Open > Chọn thư mục dự án
```

3. **Sync Gradle files**
```
Chờ Android Studio tự động sync hoặc click "Sync Now"
```

4. **Chạy ứng dụng**
```
Click nút Run hoặc Shift + F10
```

## 📦 Dependencies chính

```gradle
// Room Database
implementation "androidx.room:room-runtime:2.4.3"
implementation "androidx.room:room-rxjava2:2.4.3"
annotationProcessor "androidx.room:room-compiler:2.4.3"

// ViewModel & LiveData
implementation "androidx.lifecycle:lifecycle-viewmodel:2.6.2"
implementation "androidx.lifecycle:lifecycle-livedata:2.6.2"

// RecyclerView
implementation "androidx.recyclerview:recyclerview:1.3.1"

// Material Design
implementation "com.google.android.material:material:1.9.0"
```

## 👥 Thành viên nhóm

| Vai trò | Tên | Nhiệm vụ chính |
|---------|-----|----------------|
| **Team Leader** | Trần Trường Giang | Quản lý dự án, Database design, Core features |
| **Developer** | Quách Việt | UI/UX Design, XML Layouts |
| **Developer** | Mạnh | Testing, Bug fixes, Documentation |

## 📱 Screenshots

*Thêm screenshots của ứng dụng tại đây*

## 🔧 Hướng dẫn sử dụng

### Thêm món ăn mới
1. Mở màn hình quản lý món ăn
2. Nhấn nút "Thêm món"
3. Điền thông tin món ăn
4. Chọn danh mục
5. Lưu món ăn

### Đặt hàng
1. Duyệt danh sách món ăn
2. Chọn món và số lượng
3. Thêm vào giỏ hàng
4. Điền thông tin giao hàng
5. Xác nhận đặt hàng

### Tìm kiếm món ăn
1. Sử dụng thanh tìm kiếm ở đầu màn hình
2. Nhập tên món hoặc từ khóa
3. Kết quả hiển thị real-time

## 🐛 Báo cáo lỗi

Nếu phát hiện lỗi, vui lòng:
1. Mô tả chi tiết lỗi
2. Các bước tái tạo lỗi
3. Screenshots (nếu có)
4. Tạo issue trên GitHub

## 🔄 Changelog

### Version 1.0.0 (Current)
- ✅ CRUD operations cho món ăn
- ✅ Tìm kiếm cơ bản
- ✅ Quản lý đơn hàng
- ✅ Database với Room ORM

### Planned Features
- 🔲 Đăng nhập/Đăng ký user
- 🔲 Payment integration
- 🔲 Push notifications
- 🔲 Rating & Reviews

## 📄 License

Dự án này được phát triển cho mục đích học tập.

## 📞 Liên hệ

- **Team Leader**: [giangtt8726@gmail.com]

---

*Được phát triển với ❤️ bởi nhóm sinh viên*
