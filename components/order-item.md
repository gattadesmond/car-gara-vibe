# 📦 Component: OrderItem
Đơn sửa chữa

## 🎯 Mục tiêu
Hiển thị một đơn hàng được tạo ra từ `CV` hoặc `ADMIN`
Mỗi `OrderItem` đại diện cho một xe đang trong quá trình tiếp nhận  tại garage.
1 `OrderItem` có thể nhiều hơn 1 task, TaskItem (xem file `components/task-item.md`)

## 🖼️ Giao diện
- Khung bo góc nhẹ, có bóng đổ nhẹ.
- Trái: tên công việc, mã công việc, ghi chú ngắn (nếu có)
- Phải: nút “Chi tiết”

## 🖼️ UI
### Thông tin khách hàng
- **Tên khách hàng**: Nguyễn Văn An / Trần Thị Bình
- **Biển số xe**: VD: `51A-96695`, `52B-12345`
- **Loại xe + đời xe**: VD: `Toyota Camry (2020)`, `Honda City (2019)`

### Button
- `Chi tiết`: vào trang chi tiết đơn của `OrderItem`

### Danh sách task
- Hiển thị danh sách `TaskItem` được tạo ra từ `OrderItem` (xem file `components/task-item.md`)
- **Status**: 
  - `Đang chờ` (màu vàng)
  - `Đang chuẩn đoán` (màu xanh dương)
  - `Hoàn thành` (Màu xanh lá)
- Mỗi `TaskItem` có thể có 1 trong 3 trạng thái: `Đang chờ`, `Đang chuẩn đoán`, `Hoàn thành`
- Mỗi `TaskItem` có thể có 1 trong 2 nút thao tác: `Phân công KTV`, `Xem chi tiết`
- **KTV phụ trách**: (hiện tại có thể là `Chưa phân công`)



