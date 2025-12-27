# Kebaikan Kita - Platform Donasi Islami

Platform donasi Islami untuk Zakat, Wakaf, Infaq, dan Qurban.

## 🚀 Deploy ke Vercel

### Cara 1: Deploy via Vercel Dashboard (Paling Mudah)

1. **Upload ke GitHub:**
   - Buat repository baru di GitHub
   - Upload semua file project ini ke repository
   
2. **Deploy di Vercel:**
   - Buka [vercel.com](https://vercel.com)
   - Login dengan GitHub
   - Klik "New Project"
   - Import repository Anda
   - Klik "Deploy" (Vercel otomatis detect Vite)

### Cara 2: Deploy via Vercel CLI

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Deploy production
vercel --prod
```

## 💻 Development Lokal

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build untuk production
npm run build

# Preview production build
npm run preview
```

## 📁 Struktur Project

```
kebaikan-kita/
├── src/
│   ├── App.jsx          # Main React component
│   ├── main.jsx         # React entry point
│   └── index.css        # Tailwind CSS
├── index.html           # HTML template
├── package.json         # Dependencies
├── vite.config.js       # Vite config
├── tailwind.config.js   # Tailwind config
└── postcss.config.js    # PostCSS config
```

## 🔧 Konfigurasi

Edit konfigurasi di `src/App.jsx`:

```javascript
const CONFIG = {
  platformName: 'Kebaikan Kita',
  bankName: 'Bank Central Asia (BCA)',
  accountNumber: '00000000',
  accountHolder: 'FIRMAN SUTARMAN HASAN',
  whatsapp: '08000000000',
  email: 'Hasan@gmail.com',
  instagram: '@KebaikanKita',
  adminPassword: 'Hasan0526',
  platformFee: 0.10,
  primaryColor: '#9CAF2F',
  primaryDark: '#7A8C24'
};
```

## 🔐 Admin Panel

Akses admin: tambahkan `#admin` di URL
- URL: `https://your-site.vercel.app/#admin`
- Password: `Hasan0526` (ubah di CONFIG)

## 📦 Dependencies

- React 18
- Vite
- Tailwind CSS
- Lucide React (icons)

## 📝 License

© 2025 Kebaikan Kita
