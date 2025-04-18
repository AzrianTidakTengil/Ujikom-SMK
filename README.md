# 🎓 The Final Exams – Popping Ecommerce

## 📁 Project Overview

**Nama Proyek:** Popping Ecommerce  
**Tanggal Mulai:** 30 Januari 2025  
**Pengembang:** Azrian Muhammadin Hanif  

**Tujuan:**  
Aplikasi E-commerce berbasis web yang memungkinkan pengguna untuk berbelanja online secara mudah, cepat, dan aman. Dibangun menggunakan **Next.js** di frontend dan **Express.js** di backend.

**Latar Belakang:**  
Pertumbuhan e-commerce menuntut adanya platform belanja online yang fleksibel, aman, dan responsif. Popping Ecommerce hadir untuk memenuhi kebutuhan tersebut dengan teknologi modern dan pengalaman pengguna yang optimal.

**Teknologi:**
- **Frontend:** Next.js  
- **Backend:** Express.js (Node.js)  
- **State Management:** Redux Toolkit  
- **UI Library:** Material UI  
- **HTTP Client:** Axios  
- **Payment:** Midtrans  
- **Middleware:** Passport.js  

---

## ⚙️ Cara Persiapan Proyek

### ✅ System Requirements
- Node.js 22.x or above  
- npm

### 📦 Instalasi

#### Frontend
```bash
git clone https://github.com/AzrianTidakTengil/Ujikom-Client.git
cd Ujikom-Client
npm install
```

#### Backend
```bash
git clone https://github.com/AzrianTidakTengil/Ujikom-API.git
cd Ujikom-API
npm install
```

### 🔐 Environment Variables

#### Frontend
```env
SECRET=9cbca2053003153f505011885d2f60c53c20e3a6
NEXT_PUBLIC_API_BASE_URL=http://localhost:3001/api
GOOGLE_OUTH_CLIENT_ID=...
GOOGLE_OUTH_CLIENT_SECRET_ID=...
MIDTRANS_CLIENT_KEY=...
CLOUDINARY_API_KEY=...
CLOUDINARY_API_SECRET=...
```

#### Backend
```env
PORT=3001
SECRET=...
MIDTRANS_SERVER_KEY=...
CLOUDINARY_API_KEY=...
CLOUDINARY_API_SECRET=...
GOOGLE_OUTH_CLIENT_ID=...
GOOGLE_OUTH_CLIENT_SECRET=...
```

### ▶️ Menjalankan Proyek
```bash
npm run dev
```

---

## 📁 Struktur Folder

### Frontend
```
/public/assets
/src
  /components
  /config
  /pages
  /services
  /store
```

### Backend
```
/config
/controllers
/middlewares
/models
/router
/seeders
```

---

## 🧠 State Management

```js
const store = configureStore({
  reducer: {
    auth,
    user,
    product,
    trolley,
    transaction,
    address,
    shop,
    region,
    keyword,
  },
});
```

Contoh penggunaan:
```js
this.props.getUser();
```

---

## 🧭 Halaman & Navigasi

| Path                      | Komponen           | Akses    | Keterangan               |
|---------------------------|--------------------|----------|--------------------------|
| `/`                       | Main               | Public   | Halaman utama            |
| `/checkout`              | CheckOut           | Private  | Checkout produk          |
| `/p/:name?id`            | Product            | Public   | Detail produk            |
| `/profile`               | Profile            | Private  | Profil pengguna          |
| `/register`              | Register           | Public   | Registrasi               |
| `/register/openshop`     | RegisterOpenShop   | Private  | Daftar sebagai seller    |
| `/register/setpassword`  | SetPassword        | Private  | Atur ulang password      |
| `/search?keyword`        | Search             | Public   | Hasil pencarian produk   |
| `/t?id`                  | ItemsTransaction   | Private  | Detail transaksi         |
| `/trolley`               | Trolley            | Private  | Daftar produk di cart    |
| `/seller`                | Seller             | Seller   | Dashboard seller         |
| `/seller/balance`        | Balance            | Seller   | Saldo seller             |
| `/seller/order`          | SellerOrder        | Seller   | Order masuk              |
| `/seller/product`        | SellerProduct      | Seller   | Manajemen produk         |
| `/seller/product/add`    | SellerProductAdd   | Seller   | Tambah produk            |
| `/seller/setting`        | SellerSetting      | Seller   | Pengaturan toko          |

---

## 🔌 API Endpoints

**Base URL:** `http://localhost:3001/api/`

> Lihat dokumen lengkap `The_Final_Exams_API_Endpoints.docx` untuk tabel detail semua endpoint.

### 🔄 Contoh Response
```json
{
  "status": "success",
  "message": "get an addresses user",
  "data": [ ... ]
}
```

---

## 🔐 Authentication

- JWT-based login
- Role-based access (Public, Auth, Seller)
- Middleware: Express + Passport.js

---

## 🎨 Styling & UI

- Material UI (MUI)
- Custom Theme via ThemeProvider
- Responsive layout with Grid & Flex

---

## 📋 Aturan Proyek

- Penamaan branch: `feat/`, `fix/`, `hotfix/`
- Pull request selalu ke `main`
- Cek dan test kode sebelum PR

---

## 📃 Acknowledgments & License

- Icons: [Material Icons](https://fonts.google.com/icons)  
- UI: [Material UI](https://mui.com/)  
- Detail: [Dokumentasi Uji Kompotensi WebSite - Azrian M Hanif](https://docs.google.com/document/d/1oR0J4acHkWtQK1LCWs5VhL47mCLh-SJFZGEuytsX5Mc/edit?usp=sharing)
- License: MIT
