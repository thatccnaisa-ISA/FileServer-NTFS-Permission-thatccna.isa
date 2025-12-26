# File Server & NTFS Permission – thatccna.isa

## 🎯 Mục tiêu
Triển khai File Server nội bộ và phân quyền truy cập dữ liệu theo phòng ban trong domain **thatccna.isa**.

---

## 🧱 Mô hình LAB
- Domain: thatccna.isa
- File Server: Windows Server
- Ip: 192.168.189.20
- DNS: 192.168.289.10 (DC)
- Client: Windows 10 (domain member)

---

## ⚙️ Các bước triển khai

### 1️⃣ Join File Server vào Domain
![Join Domain](images/join-domain.png)

---

### 2️⃣ Tạo cấu trúc thư mục phòng ban
![Folder Structure](images/folder-structure.png)

---

### 3️⃣ Tạo Group trong Active Directory

#### OU / Group phòng Nhân sự
![AD Groups NHANSU](images/ad-groups-nhansu.png)

#### OU / Group phòng Kế toán
![AD Groups KETOAN](images/ad-groups-ketoan.png)

#### OU / Group phòng Sale
![AD Groups SALE](images/ad-groups-sale.png)

#### OU / Group phòng IT
![AD Groups IT](images/ad-groups-it.png)

---

### 4️⃣ Phân quyền NTFS theo Group

#### NTFS – Phòng Nhân sự
![NTFS NHANSU](images/ntfs-nhansu.png)

#### NTFS – Phòng Kế toán
![NTFS KETOAN](images/ntfs-ketoan.png)

#### NTFS – Phòng Sale
![NTFS SALE](images/ntfs-sale.png)

#### NTFS – Phòng IT
![NTFS IT](images/ntfs-it.png)

---

### 5️⃣ Share Folder
![Share Folder](images/share-setting.png)

---

### 6️⃣ Test truy cập từ máy Client

#### Truy cập đúng quyền
![Access OK](images/client-access-ok.png)

#### Truy cập sai quyền
![Access Denied](images/access-denied.png)

---

## ✅ Kết quả
- User đăng nhập domain chỉ truy cập được thư mục đúng phòng ban
- Phân quyền được quản lý bằng **Active Directory Group + NTFS**
