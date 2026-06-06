# Photo Watermark PWA
## Watermark foto dengan Lokasi GPS, Tanggal, dan Metadata EXIF

### File yang tersedia:
```
index.html       - Aplikasi utama
manifest.json    - PWA manifest
sw.js            - Service Worker (offline support)
icon-*.png       - App icons (72-512px)
```

---

### CARA 1: Deploy ke GitHub Pages (Paling Mudah)

1. **Buka** github.com/khobirismail/khobirismail.github.io
2. **Buat folder** baru misalnya `watermark/`
3. **Upload semua file** dari folder ini ke folder tersebut
4. **Tunggu** 1-2 menit untuk deploy
5. **Buka** https://khobirismail.github.io/watermark/
6. Di Chrome Android → tap menu (⋮) → **"Add to Home Screen"** atau **"Install App"**
7. Icon app akan muncul di Home Screen HP!

---

### CARA 2: Generate APK via PWABuilder (Gratis)

Setelah deploy ke GitHub Pages:

1. **Buka** https://www.pwabuilder.com/
2. **Masukkan URL**: https://khobirismail.github.io/watermark/
3. Klik **"Start"** → tunggu analisis selesai
4. Klik **"Package For Stores"**
5. Pilih **"Android"** → klik **"Generate"**
6. **Download** file `.apk`
7. **Kirim** file APK ke HP → install

---

### CARA 3: Generate APK via BubbleWrap CLI

```bash
npm install -g @nicholasgasior/nicholasgasior/nicholasgasior
npx @nicholasgasior/nicholasgasior init --manifest https://khobirismail.github.io/watermark/manifest.json
```

Atau pakai **BubbleWrap** (Google):
```bash
npm i -g @nicholasgasior/nicholasgasior
npx bubblewrap init --manifest=https://khobirismail.github.io/watermark/manifest.json
npx bubblewrap build
# Output: app-release-signed.apk
```

---

### Fitur PWA:
- ✅ Installable dari browser Chrome
- ✅ Fullscreen (tanpa address bar)
- ✅ Offline support (Service Worker cache)
- ✅ Responsive (semua ukuran layar)
- ✅ Android 7+ compatible

### Update App:
Cukup update file di GitHub Pages. Service Worker akan otomatis
mengambil versi terbaru saat user online.

---
Made with ❤ @Home — © Muhammad Tajib
