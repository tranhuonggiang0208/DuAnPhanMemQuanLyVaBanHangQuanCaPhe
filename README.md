Tuyệt vời! Tôi đã cập nhật file `README.md` với thông tin **Apache NetBeans IDE 25**:

```markdown
# ☕ Phần Mềm Quản Lý Và Bán Hàng Quán Cà Phê

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Swing](https://img.shields.io/badge/Swing-007396?style=for-the-badge&logo=java&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white)
![NetBeans](https://img.shields.io/badge/NetBeans%2025-1B6AC6?style=for-the-badge&logo=apache%20netbeans%20ide&logoColor=white)

## 📝 Giới thiệu

**Đồ án môn học** - Phần mềm quản lý và bán hàng dành cho quán cà phê, được xây dựng bằng **Java Swing** trên **Apache NetBeans IDE 25** và **Microsoft SQL Server**. Hệ thống giúp chủ quán và nhân viên thu ngân quản lý hoạt động kinh doanh một cách hiệu quả, chuyên nghiệp.

## ✨ Tính năng chính

### 👥 Phân quyền người dùng
- **Chủ quán**: Toàn quyền quản lý (nhân viên, kho, báo cáo doanh thu, thống kê)
- **Thu ngân**: Quản lý bán hàng, thanh toán, xem doanh thu (không được sửa/xóa dữ liệu nhạy cảm)

### 🛒 Quản lý bán hàng
- Quản lý thực đơn đồ uống (cà phê, sinh tố, trà, bánh ngọt...)
- Quản lý bàn (trống, đang dùng, đã đặt)
- Gọi món trực tiếp tại bàn
- Thanh toán hóa đơn (tiền mặt/chuyển khoản)
- Tìm kiếm hóa đơn theo ngày, mã bàn
- In hóa đơn tạm tính

### 📊 Quản lý doanh thu
- Thống kê doanh thu theo ngày/tháng/năm
- Xem danh sách món bán chạy nhất
- Xuất báo cáo doanh thu ra Excel
- Biểu đồ doanh thu trực quan

### 👨‍💼 Quản lý nhân viên (Chủ quán)
- Thêm/xóa/sửa thông tin nhân viên
- Phân quyền tài khoản (chủ quán/thu ngân)
- Chấm công và tính lương cơ bản
- Lịch sử làm việc của nhân viên

### 📦 Quản lý kho (Chủ quán)
- Theo dõi nguyên liệu tồn kho
- Cảnh báo nguyên liệu sắp hết (dưới 10% tồn kho)
- Nhập kho, xuất kho
- Lịch sử nhập/xuất nguyên liệu

### ⚙️ Quản lý hệ thống
- Sao lưu và phục hồi dữ liệu
- Xem nhật ký hoạt động (log)
- Đổi mật khẩu người dùng

## 🛠️ Công nghệ sử dụng

| Thành phần | Công nghệ | Phiên bản |
|------------|-----------|-----------|
| **Ngôn ngữ** | Java | JDK 8/11/17 |
| **Giao diện** | Java Swing | - |
| **Cơ sở dữ liệu** | Microsoft SQL Server | 2012/2014/2016/2019/2022 |
| **IDE** | Apache NetBeans | **25** |
| **Build tool** | Apache Ant | - |
| **Kết nối CSDL** | JDBC | - |
| **Báo cáo** | JasperReports / Excel | - |

## 📁 Cấu trúc thư mục

```
DuAnPhanMemQuanLyVaBanHangQuanCaPhe/
├── src/
│   ├── quanlycaphe/
│   │   ├── view/              # Giao diện Swing (JFrame, JDialog)
│   │   │   ├── LoginJFrame.java
│   │   │   ├── MainJFrame.java
│   │   │   ├── BanJPanel.java
│   │   │   ├── ThucDonJPanel.java
│   │   │   ├── HoaDonJPanel.java
│   │   │   ├── NhanVienJPanel.java
│   │   │   ├── KhoJPanel.java
│   │   │   ├── ThongKeJPanel.java
│   │   │   └── ...
│   │   ├── controller/        # Xử lý nghiệp vụ
│   │   │   ├── BanController.java
│   │   │   ├── HoaDonController.java
│   │   │   └── ...
│   │   ├── model/             # Các đối tượng (POJO)
│   │   │   ├── Ban.java
│   │   │   ├── Mon.java
│   │   │   ├── NhanVien.java
│   │   │   ├── HoaDon.java
│   │   │   ├── ChiTietHoaDon.java
│   │   │   └── ...
│   │   ├── dao/               # Data Access Object - kết nối SQL Server
│   │   │   ├── DatabaseConnection.java
│   │   │   ├── BanDAO.java
│   │   │   ├── MonDAO.java
│   │   │   └── ...
│   │   └── utils/             # Các tiện ích
│   │       ├── FormatNumber.java
│   │       ├── DateUtils.java
│   │       ├── ExcelExporter.java
│   │       └── ...
├── nbproject/                  # Cấu hình dự án NetBeans
├── database/
│   ├── script.sql             # Script tạo CSDL
│   └── data_sample.sql         # Dữ liệu mẫu
├── lib/                        # Thư viện JAR bên ngoài (nếu có)
├── reports/                    # Mẫu báo cáo (JasperReports)
├── build.xml                   # Ant build script
├── manifest.mf                 # Manifest file
└── README.md
```

## 🚀 Hướng dẫn cài đặt chi tiết

### Yêu cầu hệ thống
- **Java JDK 8, 11 hoặc 17** ([Tải JDK](https://www.oracle.com/java/technologies/javase-downloads.html))
- **Microsoft SQL Server** 2012 trở lên ([Tải SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads))
- **SQL Server Management Studio (SSMS)** ([Tải SSMS](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms))
- **Apache NetBeans IDE 25** ([Tải NetBeans 25](https://netbeans.apache.org/download/index.html))
- **RAM tối thiểu**: 4GB (khuyến nghị 8GB)

### Các bước cài đặt

#### Bước 1: Cài đặt Apache NetBeans IDE 25
1. Truy cập [Apache NetBeans 25 Download](https://netbeans.apache.org/download/index.html)
2. Chọn phiên bản phù hợp với hệ điều hành (Windows/macOS/Linux)
3. Tải và cài đặt theo hướng dẫn

#### Bước 2: Clone dự án
```bash
git clone https://github.com/tranhuonggiang0208/DuAnPhanMemQuanLyVaBanHangQuanCaPhe.git
```
Hoặc tải ZIP và giải nén.

#### Bước 3: Tạo Database trong SQL Server
1. Mở **SQL Server Management Studio (SSMS)**
2. Đăng nhập với tài khoản (thường là **sa** hoặc Windows Authentication)
3. Tạo database mới:
```sql
CREATE DATABASE QuanLyQuanCaPhe;
USE QuanLyQuanCaPhe;
```
4. Mở file `database/script.sql` và chạy toàn bộ script để tạo bảng
5. (Tùy chọn) Chạy file `database/data_sample.sql` để thêm dữ liệu mẫu

#### Bước 4: Cấu hình kết nối CSDL
Mở file `src/quanlycaphe/dao/DatabaseConnection.java` và sửa thông tin kết nối:
```java
public class DatabaseConnection {
    private static final String SERVER = "localhost";  // hoặc IP máy chủ SQL
    private static final String PORT = "1433";         // cổng mặc định SQL Server
    private static final String DATABASE = "QuanLyQuanCaPhe";
    private static final String USERNAME = "sa";       // tài khoản SQL của bạn
    private static final String PASSWORD = "123456";   // mật khẩu của bạn
    
    public static Connection getConnection() {
        String url = "jdbc:sqlserver://" + SERVER + ":" + PORT + 
                     ";databaseName=" + DATABASE + 
                     ";encrypt=true;trustServerCertificate=true";
        // ...
    }
}
```

#### Bước 5: Thêm thư viện JDBC cho SQL Server
1. Tải **Microsoft JDBC Driver for SQL Server** từ [đây](https://docs.microsoft.com/en-us/sql/connect/jdbc/download-microsoft-jdbc-driver-for-sql-server)
2. Trong NetBeans:
   - Chuột phải vào **Libraries** của project
   - Chọn **Add JAR/Folder**
   - Dẫn đến file `mssql-jdbc-12.2.0.jre8.jar` (hoặc phiên bản mới nhất)

#### Bước 6: Mở project trong NetBeans 25
1. Khởi động **Apache NetBeans IDE 25**
2. Chọn **File** → **Open Project** (hoặc nhấn `Ctrl+Shift+O`)
3. Dẫn đến thư mục `DuAnPhanMemQuanLyVaBanHangQuanCaPhe`
4. Chọn **Open Project**
5. Đợi NetBeans load và index project (có thể mất vài phút)

#### Bước 7: Chạy chương trình
- Nhấn **F6** (Run Main Project) hoặc
- Chuột phải vào project → **Run**

## 👤 Tài khoản đăng nhập mẫu

| Vai trò | Tên đăng nhập | Mật khẩu |
|---------|---------------|----------|
| **Chủ quán** | admin | admin@123 |
| **Thu ngân 1** | thungan01 | thu ngan@01 |
| **Thu ngân 2** | thungan02 | thu ngan@02 |

*(Bạn có thể tạo thêm tài khoản trong phần Quản lý nhân viên)*

## 📸 Ảnh chụp màn hình (demo)

*(Sau khi chụp ảnh, bạn thêm vào đây)*

```
screenshots/
├── login-screen.png          # Màn hình đăng nhập
├── main-screen-admin.png     # Giao diện chính (chủ quán)
├── main-screen-cashier.png   # Giao diện chính (thu ngân)
├── order-screen.png          # Màn hình gọi món
├── payment-screen.png        # Màn hình thanh toán
├── report-screen.png         # Báo cáo doanh thu
└── inventory-screen.png      # Quản lý kho
```

## ❓ Xử lý sự cố thường gặp

### 1. Lỗi kết nối SQL Server
- **Kiểm tra dịch vụ SQL Server** đã chạy chưa (Services.msc)
- **Kiểm tra tài khoản sa** đã được kích hoạt chưa
- **Kiểm tra firewall** có chặn port 1433 không
- **Thử dùng Windows Authentication** thay vì tài khoản sa

### 2. Lỗi thiếu thư viện JDBC
- Tải đúng phiên bản JDBC driver phù hợp với JDK
- Thêm thư viện vào project trong NetBeans

### 3. Lỗi không mở được project trong NetBeans 25
- Kiểm tra phiên bản JDK đã được cài đặt đúng
- Xóa cache NetBeans: `C:\Users\YourName\AppData\Local\NetBeans\Cache\25`

## 💡 Đóng góp cho dự án

Mọi đóng góp đều được chào đón! Các bạn sinh viên có thể:
- Fork dự án và tạo Pull Request
- Báo lỗi qua [Issues](https://github.com/tranhuonggiang0208/DuAnPhanMemQuanLyVaBanHangQuanCaPhe/issues)
- Đề xuất tính năng mới
- Cải thiện tài liệu hướng dẫn

## 📞 Liên hệ

- **Tác giả:** Trần Hương Giang
- **Môn học:** Đồ án môn học - Lập trình Java
- **Trường:** [Tên trường của bạn]
- **Năm thực hiện:** 2026
- **IDE sử dụng:** Apache NetBeans 25
- **GitHub:** [@tranhuonggiang0208](https://github.com/tranhuonggiang0208)
- **Email:** (thêm email nếu muốn)

## 📄 Giấy phép

Dự án này được sử dụng cho mục đích học tập. Vui lòng liên hệ tác giả nếu muốn sử dụng cho mục đích thương mại.

---

## 🙏 Lời cảm ơn

Cảm ơn thầy/cô hướng dẫn đã giúp đỡ hoàn thành đồ án này. Cảm ơn các bạn đã quan tâm đến dự án!

---

**⭐ Nếu thấy dự án hữu ích, hãy nhấn Star để ủng hộ nhé!** 
```

## 📝 Những việc bạn cần làm tiếp theo:

1. **Thêm thông tin trường học** của bạn vào phần Liên hệ
2. **Tạo file script.sql** trong thư mục `database/`
3. **Chụp ảnh màn hình** các giao diện chính và tạo thư mục `screenshots/`
4. **Kiểm tra lại tài khoản mẫu** cho đúng với dữ liệu thực tế
5. **Thêm email** nếu muốn người khác liên hệ

Bạn có muốn tôi điều chỉnh thêm phần nào không? Hay cần tôi giúp viết file script SQL mẫu luôn? 😊
