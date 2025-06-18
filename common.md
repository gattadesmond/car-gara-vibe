## Ứng dụng quản lý garage/trung tâm dịch vụ ô tô

Car Repair Garage Mobile Web App (MVP)

### 📌 Mục tiêu dự án(Project Summary)

Phát triển **Mobile Web App** hỗ trợ cố vấn dịch vụ và kỹ thuật viên tại gara thực hiện các bước kiểm tra, chẩn đoán và lập báo giá sửa chữa xe **nhanh – chuẩn – tự tin**, bám sát quy trình thực tế tại gara.

Ứng dụng ưu tiên thiết kế **Mobile-first**, có thể đóng gói thành **Mobile App** dưới hình thức PWA.

---

### 👤 Đối tượng sử dụng(User Persona)

- **Cố vấn dịch vụ (CV)**: Chọn khách hàng cũ hoặc tạo khách hàng mới, Tạo phiếu tiếp nhận, kiểm tra triệu chứng xe và lập phiếu sửa chữa.
- **Kỹ thuật viên (KTV)**: Nhận chọn task từ phiếu sửa chữa, kiểm tra xe và ghi note thông tin sửa chữa, tạo “lệnh sửa chữa”.
- **Quản lý gara**: Giám sát quy trình, kiểm tra báo giá, xuất báo cáo tổng hợp.

### ⚙️ Tính năng MVP (Giai đoạn 1) (Key Features)

- Đăng nhập & phân quyền người dùng (CV, KTV, Quản lý)
- Nhập/chọn thông tin khách hàng và xe
- Ghi nhận tình trạng xe ban đầu
- Giao diện chọn triệu chứng theo cây phân cấp (dropdown / nested menu)
- Cố vấn chẩn đoán sơ bộ & tạo lệnh phiếu sửa chữa
- Kỹ thuật viên chọn lệnh sửa chữa và ghi note & tạo lệnh sửa chữa
- Xuất báo giá và báo cáo ra PDF
- Lưu lịch sử công việc và báo giá


### Luồng sử dụng

1. Vào trang chính
2. Cố vấn đăng nhập
3. Cố vấn tạo phiếu sửa chữa
4. Cố vấn chọn lệnh sửa chữa và tạo lệnh sửa chữa
5. Kỹ thuật viên nhận lệnh sửa chữa
6. Kỹ thuật viên kiểm tra xe và ghi note
7. Kỹ thuật viên tạo lệnh sửa chữa
8. Cố vấn xem báo giá và tiến hành thanh toán
9. Cố vấn xuất báo cáo

### Mô tả giao diện (UI)

### Sitemap

#### 🔐 Auth
- `/login` – Đăng nhập
- `/forgot-password` – Quên mật khẩu

#### 📦 Cố Vấn Dịch Vụ (CV)
- `/cv/dashboard` – Tổng quan
- `/cv/customers` – Quản lý khách hàng (tạo/sửa qua modal)
- `/cv/vehicles` – Quản lý xe
- `/cv/intake-forms` – Phiếu tiếp nhận
  - `/cv/intake-forms/[id]` – Chi tiết phiếu
- `/cv/repair-orders` – Lệnh sửa chữa (tabs: Tạo, Đang xử lý, Hoàn tất)
  - `/cv/repair-orders/[id]` – Chi tiết lệnh
- `/cv/reports/summary` – Báo cáo tổng hợp

#### 🧰 Kỹ Thuật Viên (KTV)
- `/ktv/tasks` – Danh sách lệnh (tabs: Có thể nhận / Đang làm)
  - `/ktv/tasks/[id]` – Chi tiết công việc

#### 📊 Quản Lý Gara (Manager)
- `/manager/dashboard` – Tổng quan
- `/manager/users` – Quản lý người dùng
- `/manager/reports` – Tabs: ngày / tháng / theo người
- `/manager/activity-log` – Lịch sử thao tác

#### ⚙️ Cài Đặt Chung
- `/settings/profile`
- `/settings/preferences`
- `/settings/logout`

---

### 📱 Giao diện & trải nghiệm

- Thiết kế **Mobile-first**, dễ dùng cho nhân viên gara sử dụng mobile hoặc tablet
- Dùng **Tailwind CSS + ShadCN UI**
- Tích hợp **PWA** để cài như mobile app

---

### 🧱 Yêu cầu kỹ thuật
Bản MVP sẽ chưa kết nối với hệ thống quản trị gara, sau khi hoàn thành MVP sẽ dùng API riêng để kết nối.

| Thành phần | Công nghệ |
| --- | --- |
| Frontend | Next.js (App Router), Tailwind CSS, ShadCN UI |
| Auth | Supabase Auth (phân quyền theo vai trò) |
| Database | Supabase PostgreSQL |
| State | Jotai |
| Export PDF | react-pdf hoặc pdfmake |
| Deploy | Vercel |
| Mobile App | Có thể đóng gói qua Capacitor / Expo (sau MVP) |