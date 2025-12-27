# 🔧 CARA FIX ERROR DEPLOYMENT VERCEL

## Error yang Anda Alami:
```
Error: Command "npm run build" exited with 1
at getRollupError (file:///vercel/path0/node_modules/rollup/...)
```

## ✅ SOLUSI LENGKAP:

### Opsi 1: Manual Fix di Vercel Dashboard

1. **Buka Project Settings** di Vercel
2. **Build & Development Settings**
3. Isi seperti ini:
   ```
   Build Command: npm install && npm run build
   Output Directory: dist
   Install Command: npm install
   ```
4. **Redeploy**

### Opsi 2: Download ZIP Baru (RECOMMENDED)

Saya sudah fix dan tambahkan file `vercel.json`:

**Download:** `kebaikan-kita-fixed.zip`

File baru ini sudah include:
- ✅ `vercel.json` dengan konfigurasi build yang benar
- ✅ Dependencies yang updated
- ✅ Build command yang proper

### Opsi 3: Edit Manual (Jika Sudah di GitHub)

Tambahkan file `vercel.json` di root project:

```json
{
  "buildCommand": "npm install && npm run build",
  "outputDirectory": "dist",
  "framework": "vite",
  "installCommand": "npm install"
}
```

## 🚀 Langkah Deploy Ulang:

### Via GitHub (Recommended):
1. **Delete** repository lama (atau buat baru)
2. Upload **file baru** dari `kebaikan-kita-fixed.zip`
3. Push ke GitHub
4. Di Vercel, klik **"Redeploy"** atau import ulang

### Via Vercel Drag & Drop:
1. Extract `kebaikan-kita-fixed.zip`
2. Buka [vercel.com/new](https://vercel.com/new)
3. Drag & drop **folder** kebaikan-kita
4. Deploy!

## 🔍 Penjelasan Error:

Error terjadi karena:
- Vercel gagal install dependencies sebelum build
- Rollup (bundler Vite) tidak menemukan module yang dibutuhkan
- Build command tidak eksplisit

File `vercel.json` yang saya tambahkan memastikan:
1. Dependencies di-install dulu (`npm install`)
2. Baru jalankan build (`npm run build`)
3. Output masuk ke folder `dist`

## ✅ Checklist Sebelum Deploy:

- [ ] Download `kebaikan-kita-fixed.zip` (yang baru)
- [ ] Extract file
- [ ] Upload ke GitHub / Vercel
- [ ] Pastikan semua file ter-upload (terutama `vercel.json`)
- [ ] Deploy!

---

**Kalau masih error, screenshot error barunya dan saya bantu lagi!** 🚀
