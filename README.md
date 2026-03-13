# Web Ledger SAK EMKM - High-Fidelity Prototype

Selamat datang di prototype Web Ledger SAK EMKM! Platform akuntansi modern untuk UMKM Indonesia yang mematuhi standar SAK EMKM.

## 📁 Struktur File

```
d:\p2mw\coba\
├── index.html          # Landing Page - Hero, Features, Pricing, CTA
├── dashboard.html      # Dashboard - Stat Cards, Chart, Quick Actions
├── transaksi.html      # Transaction Module - Input Form & History Table
├── onboarding.html     # Onboarding - UMKM Type Selection
├── laporan.html        # Reports - Laba Rugi, Neraca, Arus Kas
└── README.md           # File ini
```

## 🎨 Fitur Utama

### 1. **Landing Page** (index.html)
- ✅ Hero Section dengan CTAs yang menarik
- ✅ Feature Steps (Daftar → Input → Laporan)
- ✅ Features Highlight dengan ikon
- ✅ Pricing Table (Bulanan Rp 185rb, Tahunan Rp 1.8jt)
- ✅ Footer dengan links
- ✅ Responsive Navigation Bar

### 2. **Dashboard** (dashboard.html)
- ✅ Sidebar Navigation responsif dengan hamburger menu di mobile
- ✅ Header dengan search bar dan user profile
- ✅ 3 Stat Cards:
  - Saldo Kas
  - Total Pendapatan (Bulan Ini)
  - Total Pengeluaran (Bulan Ini)
- ✅ Interactive Chart Placeholder (Arus Kas Bulanan)
- ✅ Quick Actions Cards (Tambah Transaksi, Lihat Laporan, Tutorial)

### 3. **Transaksi** (transaksi.html)
- ✅ Form Input Transaksi user-friendly:
  - Jenis (Pemasukan/Pengeluaran)
  - Kategori (dropdown)
  - Nominal (Rp)
  - Tanggal
  - Deskripsi
  - QRIS Label Checkbox
- ✅ Transaction History Table dengan:
  - Kolom: Tanggal, Kategori, Deskripsi, Nominal, Aksi
  - Edit & Delete buttons
  - Filter dropdown
  - Pagination
- ✅ Color-coded badges untuk kategori

### 4. **Onboarding** (onboarding.html)
- ✅ Progress bar (3 steps)
- ✅ 3 UMKM Type Cards (clickable):
  - Jasa (Konsultan, Akuntan, Desainer, dll)
  - Dagang (Toko retail, Warung, Marketplace)
  - Manufaktur (Produksi, Kerajinan, Industri)
- ✅ Feature list untuk setiap tipe
- ✅ Interactive card selection dengan visual feedback
- ✅ Skip option

### 5. **Laporan** (laporan.html)
- ✅ 3 Tab Reports:
  1. **Laporan Laba Rugi** (Profit & Loss):
     - Pendapatan Usaha
     - Beban Operasional
     - Laba Usaha
     - Biaya Lain-lain
     - Laba Bersih
  
  2. **Neraca** (Balance Sheet):
     - Aktiva (Lancar & Tetap)
     - Passiva & Ekuitas
     - Total Aktiva = Total Passiva & Ekuitas
  
  3. **Arus Kas** (Cash Flow):
     - Aktivitas Operasional
     - Aktivitas Investasi
     - Aktivitas Pendanaan
- ✅ Period filter (Bulan/Kuartal/Tahunan)
- ✅ Export & Print buttons
- ✅ Summary cards
- ✅ Professional table formatting

## 🎨 Design System

### Warna Utama (Light Blue)
- **Primary:** #0EA5E9 (Sky Blue) & #06B6D4 (Cyan)
- **Secondary Greens:** #10B981 (Emerald) untuk revenue
- **Secondary Reds:** #EF4444 (Red) untuk expenses
- **Backgrounds:** #F3F4F6 (Gray 100), #E0F2FE (Sky 100)

### Typography
- **Font:** Segoe UI, Tahoma, Geneva, Verdana (System fonts)
- **Sizes:** H1=4xl, H2=3xl, H3=2xl, Body=base/sm

### Components
- **Cards:** Rounded-xl (16px), shadow-md, hover effects
- **Buttons:** Gradient backgrounds, py-2 to py-4
- **Tables:** Striped rows, hover states, responsive
- **Icons:** Lucide Icons via CDN
- **Layout:** Flexbox & CSS Grid

## 🚀 Cara Menggunakan

### Metode 1: Buka di Browser (Recommended)
1. Buka file `index.html` dengan double-click atau drag ke browser
2. Atau: `Right-click → Open with → Browser pilihan Anda`

### Metode 2: Gunakan Live Preview (VSCode)
1. Install extension **Live Preview** dari Microsoft
2. Buka `index.html` → Right-click → "Show Preview"
3. Preview ditampilkan di sebelah kanan editor
4. Edit code → preview auto-refresh

### Metode 3: Local Server
```bash
# Jika punya Python 3
python -m http.server 8000

# Jika punya Node.js + http-server
npx http-server

# Kemudian buka: http://localhost:8000
```

## 🔗 Navigation Links

**Landing Page (index.html)**
- → Dashboard (dashboard.html)
- → Onboarding (onboarding.html)

**Semua Pages (Dashboard, Transaksi, Laporan, Onboarding)**
- Sidebar Navigation untuk pindah antar halaman
- Back to Landing via Logout

**Flow Rekomendasi:**
```
index.html → onboarding.html → dashboard.html → {transaksi.html | laporan.html}
```

## 💡 Tips Modifikasi

### 1. Mengubah Warna Brand
Cari dan ganti:
- `from-cyan-400 to-blue-500` → Gradient utama
- `text-cyan-600` → Text highlight
- `bg-cyan-100` → Light backgrounds
- `border-cyan-200/400` → Borders

### 2. Menambah Kategori Transaksi
Edit di `transaksi.html`:
```html
<select class="form-input">
    <option>-- Pilih Kategori --</option>
    <option>Penjualan</option>
    <option>Jasa Layanan</option>
    <!-- TAMBAH DI SINI -->
</select>
```

### 3. Mengubah Data Dummy
- **Dashboard:** Edit nominal di stat cards
- **Transaksi:** Edit table rows (copy-paste dan ubah data)
- **Laporan:** Edit nilai di tabel laporan
- **Onboarding:** Edit UMKM types di cards

### 4. Menambah Menu Sidebar
Edit semua file (dashboard, transaksi, laporan):
```html
<a href="menu-baru.html" class="flex items-center gap-3 px-4 py-3...">
    <svg>...</svg>
    <span class="font-medium">Menu Baru</span>
</a>
```

## 📱 Responsive Breakpoints

- **Mobile:** < 768px (hamburger menu sidebar)
- **Tablet:** 768px - 1024px
- **Desktop:** > 1024px (sidebar always visible)

Gunakan class:
- `hidden md:flex` → Hidden di mobile, flex di desktop
- `md:grid-cols-2 lg:grid-cols-3` → Responsive grid
- `md:px-8` → Responsive padding

## ⚡ Performance Tips

1. **Tailwind CSS via CDN** - Sudah teroptimasi
2. **Lucide Icons via CDN** - Sudah teroptimasi
3. **SVG Icons** - Gunakan inline atau dari Lucide
4. **Images** - Belum ada, siap untuk ditambah
5. **Minimal JavaScript** - Hanya untuk interaksi UI

## 🎓 Learning Resources

- **Tailwind CSS:** https://tailwindcss.com/docs
- **Lucide Icons:** https://lucide.dev
- **HTML5:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **Responsive Design:** https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design

## 📝 Catatan Penting

✅ **Prototype ini includes:**
- ✅ Responsive design (Mobile, Tablet, Desktop)
- ✅ Interactive UI components
- ✅ Dummy data realistic
- ✅ Form structures (belum fungsional backend)
- ✅ Chart placeholders (siap untuk library chart.js/d3.js)
- ✅ Professional styling dengan Tailwind CSS

❌ **Belum include (untuk phase selanjutnya):**
- ❌ Backend integration
- ❌ Database
- ❌ Authentication system
- ❌ Real chart visualizations
- ❌ Form validation & submission
- ❌ API calls

## 🤝 Support

Jika ingin memodifikasi lebih lanjut:
1. Gunakan browser DevTools (F12) untuk inspect element
2. Edit langsung di code dengan VSCode
3. Refer ke dokumentasi Tailwind CSS
4. Use Copilot untuk generate code components

---

**Version:** 1.0  
**Last Updated:** March 2026  
**Created for:** Web Ledger SAK EMKM Project
