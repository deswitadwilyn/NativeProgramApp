# Check-in App 📍

Aplikasi check-in berbasis Expo/React Native yang menggabungkan **foto selfie**, **lokasi GPS**, dan **reverse geocoding**, dengan riwayat check-in yang tersimpan secara lokal.

## Fitur Native yang Dipakai
- **Kamera & Galeri** — `expo-image-picker`
- **GPS / Lokasi** — `expo-location`
- **Reverse Geocoding** — `Location.reverseGeocodeAsync`
- **Penyimpanan Lokal** — `@react-native-async-storage/async-storage`
- **Linking** — buka Google Maps & buka Pengaturan HP

## Daftar Fitur

### Level 1 — Core
- [x] Akses kamera (dengan opsi galeri) dan GPS
- [x] Permission flow: request izin → cek `status === 'granted'` → akses fitur
- [x] Penolakan izin ditangani dengan `Alert` yang ramah, tanpa crash
- [x] Cek `hasil.canceled` sebelum mengambil `assets[0].uri`
- [x] Tampilkan foto (`Image` dengan dimensi) & koordinat lokasi
- [x] UI rapi menampilkan hasil

### Level 2 (min. 2 — proyek ini punya 5)
- [x] 📸 **Kamera + Galeri** — dialog pilihan sumber foto
- [x] 📍 **Kamera + Lokasi** — satu data check-in berisi foto & koordinat
- [x] 💾 **Persistensi** — riwayat check-in disimpan & dimuat dari AsyncStorage
- [x] 🗺️ **Buka di Maps** — tombol membuka koordinat lewat Google Maps
- [x] 🔁 **Tombol Settings** — saat izin ditolak, ada tombol `Linking.openSettings()`
- [x] 🖼️ **Galeri Multi-Foto** — riwayat check-in ditampilkan dalam `FlatList`

### Level 3 — Bonus
- [x] **Reverse geocoding** — koordinat diubah menjadi nama tempat
- [x] **app.json lengkap** — usage description untuk semua izin (kamera, galeri, lokasi)

## Screenshot
> Tambahkan minimal 3 screenshot di sini setelah uji coba di HP fisik:
1. Hasil foto & lokasi setelah check-in berhasil (<img width="738" height="1600" alt="hasil" src="https://github.com/user-attachments/assets/5d9cc511-8eff-4397-89b7-ccb7a53418cf" />)

2. Dialog permintaan izin sistem (kamera/lokasi) (<img width="738" height="1600" alt="izinapp" src="https://github.com/user-attachments/assets/c32838c2-9303-4736-a684-66f38be0259b" />)

3. Penanganan penolakan izin (Alert + tombol Pengaturan) (<img width="738" height="1600" alt="bisa" src="https://github.com/user-attachments/assets/c69ac519-2ed2-4f2f-bc4d-6a53fbdaf4d8" />)



## Cara Menjalankan
```bash
npm install
npx expo start
```
Scan QR code yang muncul menggunakan aplikasi **Expo Go** di HP kamu.

## Tech Stack
- React Native (Expo SDK 54)
- expo-image-picker, expo-location
- @react-native-async-storage/async-storage

## Link Expo Snack
> Tempel link Expo Snack (https://snack.expo.dev/@deswita/df8a86) di sini setelah kamu upload kode ini ke Snack.
