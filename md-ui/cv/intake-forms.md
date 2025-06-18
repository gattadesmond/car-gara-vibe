Tôi muốn bạn tạo một giao diện web "Tạo phiếu tiếp nhận xe" cho một gara ô tô. Đây là giao diện mobile-first, tối ưu cho máy tính bảng (iPad mini). Toàn bộ giao diện có các phần như sau:

---

## 📋 1. Thông tin khách hàng
- Tên khách hàng (input, required)
- Số điện thoại (input, required)
- Email (input, optional)

---

## 🚗 2. Thông tin xe
- Biển số xe (required)
- Số khung VIN (optional)
- Hãng xe (dropdown)
- Dòng xe (dropdown phụ thuộc vào hãng)
- Năm sản xuất (dropdown)

---

## 🧰 3. Thông tin dịch vụ
- Textarea: "Yêu cầu của khách hàng" (required)
- Checkbox nhóm “Tình trạng ban đầu” gồm:
  - Vết xước nhỏ
  - Vết xước sâu
  - Móp méo
  - Hư hỏng đèn
  - Lốp hư
  - Kính vỡ
  - Khác

---

## 🔍 4. Triệu chứng phát hiện
- Tiêu đề: “Chọn triệu chứng”
- Có 3 tab:
  - Sửa chữa chung
  - Đồng sơn
  - Dọn xe
- Mỗi tab chứa danh sách triệu chứng theo dạng cây phân cấp (accordion nhiều cấp), có thể tick checkbox
- Có ô tìm kiếm “Tìm kiếm triệu chứng…”

---

## 📝 5. Ghi chú và ngày tiếp nhận
- Textarea: “Ghi chú thêm”
- Ngày tiếp nhận: (date picker, mặc định hôm nay)

---

## 📸 6. Hình ảnh xe
- Phần upload ảnh, cho phép:
  - Chụp ảnh
  - Tải ảnh lên
  - Hiển thị (0/10 ảnh)
- Chú thích:
  - Chụp ảnh vị trí hư hỏng, vết xước, móp méo
  - Ảnh tổng thể 4 góc
  - JPG, PNG, ≤5MB, tối đa 10 ảnh

---

## ✅ Footer cố định
- Nút chính: “Tạo phiếu tiếp nhận” (nổi bật, màu đen)
- Nút phụ: “Hủy”

---

## 🎨 Yêu cầu thiết kế
- Giao diện hiện đại, sạch sẽ
- Sử dụng Tailwind CSS
- Có thể dùng React, Next.js, hoặc component headless
- Accordion có animation mượt
- Checkbox dễ tick
- Tối ưu trên tablet (width 768px)

---

## 🧠 Ghi chú thêm cho AI
- Các field có dấu * là bắt buộc
- Sử dụng local state hoặc form lib (như React Hook Form) để kiểm tra đầu vào
- Có thể thêm field validation cơ bản
- Tab “Triệu chứng” nên giữ trạng thái khi chuyển qua lại
