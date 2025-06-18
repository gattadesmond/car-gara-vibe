Tạo màn hình **Quản lý khách hàng** cho hệ thống sửa chữa ô tô (Garage Manager). Giao diện giống như ảnh tôi cung cấp, và gồm các thành phần sau:

---

## 🧭 Tổng quan UI

- Trang hiển thị danh sách khách hàng dạng card
- Mỗi card bao gồm:
  - Tên khách hàng (có label “Khách cũ” nếu là khách quay lại)
  - Số điện thoại 📞
  - Email 📧
  - Danh sách các xe của khách (biển số + tên xe + năm sản xuất)
  - Ngày sửa cuối cùng
  - Hai nút:
    - **Lịch sử** (icon đồng hồ + label)
    - **Tạo phiếu mới** (nút đen nổi bật)

---

## 🔍 Phần tìm kiếm
- Ô input phía trên cùng:
  - Placeholder: `Tìm kiếm theo tên, SĐT, biển số...`
  - Full width
- Bên phải ô tìm kiếm là nút **“+ Thêm khách hàng”**
  - Kiểu: primary, đậm, biểu tượng ➕

---

## 📋 Mỗi khách hàng hiển thị:
- **Họ tên** (font lớn, đậm)
- **Số điện thoại** với icon 📞
- **Email** với icon 📧
- Dòng "Xe của khách:" với icon 🚗
- Danh sách các xe:
  - VD: `51A-96695 – Toyota Camry (2020)`
- Dòng: "Lần sửa cuối: [ngày]"

---

## 🧩 Yêu cầu kỹ thuật
- Dùng React + Tailwind CSS
- Component hóa:
  - `CustomerCard`
  - `SearchBar`
  - `ActionButton`
- Dữ liệu khách hàng nên được truyền qua props (có thể là mảng `customers[]`)
- Có responsive: layout grid 1 cột trên mobile, 2 cột trên tablet
- Nút “Tạo phiếu mới” có thể mở form intake mới hoặc chuyển route `/intake-forms/create?customerId=...`

---

## 🧠 Ghi chú thêm
- Danh sách khách hàng nên hỗ trợ scroll nếu dài
- Lưu ý spacing thoáng, font dễ đọc, màu sắc nhẹ
- Có thể cho label "Khách cũ" nằm trong badge (rounded-sm, border)

