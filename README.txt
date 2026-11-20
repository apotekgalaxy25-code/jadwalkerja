APOTEK GALAXY - PROYEK APK ANDROID
==================================
Isi: www/index.html (aplikasi), package.json + capacitor.config.json (Capacitor),
     .github/workflows/build-apk.yml (build otomatis di GitHub).

CARA 1 - BUILD OTOMATIS DI GITHUB (tanpa Android Studio)
1. Buat akun GitHub, buat repository baru (private), lalu upload SEMUA isi folder ini
   (termasuk folder .github).
2. Buka tab Actions > "Build APK" > Run workflow.
3. Setelah selesai (+/- 5-10 menit), buka hasil run > Artifacts > unduh "apotek-galaxy-apk".
4. Ekstrak, kirim app-debug.apk ke HP, buka, izinkan "Instal dari sumber tidak dikenal", instal.

CARA 2 - BUILD DI KOMPUTER (perlu Node.js 18+, JDK 17, Android Studio/SDK)
   npm install
   npx cap add android
   npx cap sync android
   cd android && ./gradlew assembleDebug      (Windows: gradlew.bat assembleDebug)
   APK ada di android/app/build/outputs/apk/debug/app-debug.apk

CATATAN
- Data tersimpan di HP masing-masing (tidak sinkron antar HP) dan tidak ada pembatasan Editor/Contributor.
- Tombol Print/PDF tidak berfungsi di WebView Android; gunakan Export JPEG lalu bagikan lewat WhatsApp.
- Export Excel butuh internet (pustaka SheetJS dari CDN); tanpa internet rekap disimpan sebagai CSV.
- Ini APK "debug" untuk dipakai sendiri, bukan untuk Google Play.
