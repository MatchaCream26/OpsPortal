# CEOD Portal - Currencies Education & Operation Digital Portal

Aplikasi web berbasis **SPA (Single Page Application)** yang dirancang sebagai portal pembelajaran interaktif untuk Front Office (Teller dan Customer Service) di perbankan.

## 🎯 Fitur Utama

### 1. **Katalog Valas (11 Mata Uang)**
- USD, SGD, AUD, EUR, GBP, JPY, CNY, MYR, SAR, HKD, IDR
- Galeri gambar denominasi (Obverse & Reverse)
- Ciri fisik dan informasi keamanan
- Panduan anti-uang palsu dengan hotspot interaktif
- Status emisi (berlaku/ditarik)

### 2. **Portal Operasional Transfer Domestik**
- RTGS: Transfer nilai besar real-time
- SKN/LLG: Transfer ritel dengan sistem kliring
- BI-Fast: Transfer modern 24/7 dengan Proxy Address
- Kliring Warkat: Panduan pemrosesan warkat debet
- Tabel komparasi interaktif

### 3. **FAQ Interaktif**
- Accordion dengan animasi smooth
- Search bar khusus untuk penemuan cepat
- Solusi operasional harian

### 4. **Forum Diskusi Internal**
- Komunitas antar teller dan CS
- Topik berdasarkan kategori (Valas, Transfer, Warkat, Keaslian Uang)
- Sistem komentar realtime dengan LocalStorage

### 5. **Manajemen CMS**
- Tambah informasi dan denominasi baru
- Edit materi yang sudah ada
- Update status validitas emisi
- Manajemen pengguna

### 6. **Smart Search & Filter**
- Pencarian global di seluruh portal
- Filter dinamis berdasarkan kategori, benua, status emisi

## 🛠️ Tech Stack

- **Frontend:** React.js 18 + Vite
- **Styling:** Tailwind CSS + Framer Motion
- **Storage:** LocalStorage (Serverless)
- **Routing:** React Router v6
- **Icons:** Lucide React

## 🚀 Instalasi & Menjalankan

### Prerequisites
- Node.js 16+ dan npm/yarn

### Steps

```bash
# Clone repository
git clone https://github.com/MatchaCream26/OpsPortal.git
cd OpsPortal

# Install dependencies
npm install

# Menjalankan development server
npm run dev

# Build untuk production
npm run build

# Preview production build
npm run preview
```

Aplikasi akan terbuka di `http://localhost:3000`

## 📁 Struktur Direktori

```
src/
├── main.jsx              # Entry point React
├── App.jsx               # Router dan layout utama
├── styles/
│   └── index.css         # Custom styles dengan Tailwind
├── data/
│   └── initialData.js    # Data dummy awal (11 valas, transfer, FAQ)
├── utils/
│   └── storage.js        # Helper untuk LocalStorage CRUD
├── components/
│   ├── Navbar.jsx        # Navigasi responsif
│   ├── Sidebar.jsx       # Sidebar menu (mobile & desktop)
│   ├── CurrencyCard.jsx  # Card untuk mata uang
│   ├── FAQ.jsx           # Accordion FAQ
│   ├── SearchBar.jsx     # Search global
│   └── LoadingSpinner.jsx # Loading indicator
├── pages/
│   ├── Dashboard.jsx     # Halaman utama
│   ├── CurrencyDetail.jsx # Detail mata uang
│   ├── DomesticTransfer.jsx # Transfer domestik
│   ├── Forum.jsx         # Forum diskusi
│   ├── FAQ.jsx           # FAQ page
│   ├── AdminCMS.jsx      # Manajemen konten
│   └── NotFound.jsx      # 404 page
└── assets/
    └── images/           # Placeholder gambar valas
```

## 💾 Data Storage (LocalStorage)

Semua data disimpan di LocalStorage dengan struktur:

```javascript
{
  currencies: [...],      // 11 mata uang
  transfers: [...],       // 4 jalur transfer
  faqs: [...],           // FAQ items
  forum_topics: [...],    // Topik forum
  users: [...],          // User profiles (untuk CMS)
  transactions: [...]    // Riwayat transaksi
}
```

## 🎨 Desain UI

### Palet Warna ("Cheerful Professional")
- **Primary:** Vibrant Blue (#3B82F6)
- **Accent:** Soft Yellow (#FBBF24)
- **Success:** Mint Green (#10B981)
- **Background:** Clean White/Light Gray (#F9FAFB)

### Typography
- **Font:** Poppins (header), Inter (body)
- **Rounded Corners:** 2xl (large radius pada cards)
- **Animasi:** Framer Motion untuk transisi smooth

## 📝 Panduan Penggunaan

### Untuk Teller/CS:
1. Login (optional)
2. Jelajahi katalog 11 mata uang
3. Baca panduan anti-uang palsu
4. Pelajari jalur transfer domestik
5. Cari solusi di FAQ
6. Diskusi di Forum

### Untuk Admin/Supervisor:
1. Akses Manajemen CMS
2. Tambah informasi/denominasi baru
3. Edit status validitas emisi
4. Update instruksi kerja

## 🔐 Keamanan

- Data sensitif disimpan di LocalStorage (client-side)
- Tidak ada transmisi data ke server eksternal
- Cocok untuk deployment offline atau di intranet bank

## 📱 Responsive Design

- Mobile-first approach
- Desktop, Tablet, dan Mobile optimized
- Sidebar collapsible untuk mobile
- Touch-friendly UI elements

## 🚢 Deployment ke GitHub Pages

```bash
# Build untuk production
npm run build

# Deploy (jika sudah konfigurasi)
git add .
git commit -m "Deploy CEOD Portal"
git push origin develop
```

## 📄 Lisensi

MIT License

## 👨‍💻 Kontribusi

Untuk kontribusi, silakan buat Pull Request atau buka Issue.

---

**Created with ❤️ for Banking Front Office Education**
