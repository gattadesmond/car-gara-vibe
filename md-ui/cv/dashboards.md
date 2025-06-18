Tạo giao diện dashboard tổng quan dành cho vai trò **Cố vấn dịch vụ** trong hệ thống quản lý gara ô tô. Giao diện giống như ảnh tôi cung cấp, bao gồm các thành phần sau:

---

## 🎨 Bố cục tổng thể
- Layout chia 2 cột:
  - Sidebar bên trái
  - Phần nội dung chính bên phải
- Responsive: thiết kế ưu tiên tablet/mobile  trước, sau đó tối ưu cho desktop

---

## 📋 Sidebar (Menu bên trái)
- Logo app: "Gara Manager", dòng phụ: "Cố Vấn Dịch Vụ"
- Menu:
  - Dashboard (🏠 icon)
  - Khách hàng (👤 icon)
  - Phiếu tiếp nhận (📄 icon)
  - Báo giá (💵 hoặc 📑 icon)
- Dưới cùng:
  - Email người dùng: `cv@gara.com`
  - Nút Đăng xuất (🔓 icon + label)

---

## 📊 Nội dung chính

### A. Header
- Tiêu đề: **Dashboard Cố vấn dịch vụ**

### B. Tổng quan số lượng
- 4 ô thống kê:
  - **Tổng phiếu** (📄 icon)
  - **Chờ xử lý** (🕒 icon)
  - **Đang sửa** (🚗 icon)
  - **Hoàn thành** (✅ icon)
- Mỗi ô:
  - Bo góc, có border, padding lớn
  - Có icon nhỏ và số đếm (VD: Tổng phiếu: 3)

---

### C. Thao tác nhanh (3 block)
- Mỗi block là 1 button lớn, có icon, label, và mô tả phụ
  - **Quản lý khách hàng** (👥)
    - Label phụ: “Xem danh sách và thông tin khách hàng”
  - **Tạo phiếu tiếp nhận** (➕)
    - Label phụ: “Tạo phiếu mới cho khách hàng”
  - **Lập báo giá** (📑)
    - Label phụ: “Tạo và quản lý báo giá sửa chữa”
- Màu sắc: mỗi block có màu nền riêng (xanh nhạt, xanh lá nhạt, tím nhạt)

---

### D. Phiếu tiếp nhận gần đây
- Tiêu đề: "10 phiếu mới nhất"
- Hiển thị danh sách 2–3 phiếu tiếp nhận gần đây:
  - Họ tên khách hàng
  - Biển số – Dòng xe (năm)
  - Ngày tiếp nhận
  - Trạng thái (VD: “Chẩn đoán”, “Báo giá”)
  - Nút hành động (VD: “Tiếp tục chẩn đoán”, “Lập báo giá”)

---

## 🧩 Yêu cầu kỹ thuật
- Sử dụng React + Tailwind CSS
- Component hóa từng phần: Card, QuickActions, Stats, Sidebar, IntakeItem
- Có thể sử dụng ShadCN UI
- Font dễ đọc, spacing thoáng
- Tối ưu hiển thị cho tablet (768px+)

---

## 🧠 Ghi chú thêm
- Số lượng thống kê lấy từ props (VD: `totalOrders`, `pending`, ...)
- Các “phiếu tiếp nhận gần đây” nên cho dưới dạng danh sách có thể map từ mảng
- Sidebar có thể cố định hoặc collapsible nếu trên mobile
