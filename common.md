## Ứng dụng quản lý garage/trung tâm dịch vụ ô tô

Car Repair Garage Mobile Web App (MVP)

### 📌 Mục tiêu dự án(Project Summary)

Phát triển **Mobile Web App** hỗ trợ cố vấn dịch vụ và kỹ thuật viên tại gara thực hiện các bước kiểm tra, chẩn đoán và lập báo giá sửa chữa xe **nhanh – chuẩn – tự tin**, bám sát quy trình thực tế tại gara.

Ứng dụng ưu tiên thiết kế **Mobile-first**, có thể đóng gói thành **Mobile App** dưới hình thức PWA.

---

### 👤 Đối tượng sử dụng(User Persona)

- **Cố vấn dịch vụ (CV)**: Chọn khách hàng cũ hoặc tạo khách hàng mới, Tạo phiếu tiếp nhận, kiểm tra triệu chứng xe và lập phiếu sửa chữa.
- **Quản lý gara (ADMIN)**: Tiếp nhận phiếu sửa chữa, phần công KTV nhận task. Giám sát quy trình, kiểm tra báo giá, xuất báo cáo tổng hợp.
- **Kỹ thuật viên (KTV)**: Nhận task từ phiếu sửa chữa, kiểm tra xe và ghi note thông tin sửa chữa, tạo “lệnh sửa chữa”.


### Luổng sử dụng

- **CV** đăng nhập -> Tạo phiếu tiếp nhận --> Chọn hoặc tạo mới khách hàng --> Chọn thông tin xe hoặc tạo mới -> Tạo Phiếu sửa chữa -> Hoàn thành
- **ADMIN** đăng nhập -> Tiếp nhận phiếu sửa chữa -> Phân công KTV -> Kiểm tra báo giá -> Xuất báo cáo
- **KTV** đăng nhập -> Nhận task -> Kiểm tra xe -> Ghi note thông tin sửa chữa -> Tạo lệnh sửa chữa




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

Đăng nhập hệ thống (All User)
Nhập/chọn thông tin khách hàng (CVDV)
Nhập/chọn thông tin xe (CVDV)
Thu thập tình trạng xe (CVDV)
Chẩn đoán sơ bộ  (CVDV, có thể không thực hiện bước này)
Lập lệnh kiểm tra xe: Dọn Dẹp, Đồng Sơn, Cơ, Điện, Lạnh (CVDV)
Phân công kỹ thuật viên (Manager)
Kiểm tra và đánh giá (KTV)
Duyệt báo cáo toàn diện (Manager/ CVDV)
Xem báo cáo toàn diện (CVDV)
Quản lý dữ liệu triệu chứng (Manager)
Quản lý người dùng và phân quyền (Manager)


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

│   ├── 📁 cv/                        # Cố vấn dịch vụ
│   │   ├── dashboard/               # Tổng quan
│   │   ├── customers/               # Tạo + quản lý khách hàng (tạo/edit trong modal)
│
│   ├── 📁 manager/                  # Manager
│   │   ├── dashboard/               # Tổng quan
│   │   ├── customers/               # Tạo + quản lý khách hàng (tạo/edit trong modal)