# TMS3206 WebView App

Aplikasi Android WebView sederhana yang mengarah ke:
**https://tms3206.aseli2025.my.id/**

---

## 📱 Fitur
- Fullscreen WebView tanpa ActionBar
- Loading progress bar
- Navigasi tombol Back
- JavaScript enabled
- DOM Storage enabled
- Support zoom
- Auto-redirect ke URL target

---

## 🔨 Cara Build APK

### Metode 1: Android Studio (Direkomendasikan)

1. **Install Android Studio**: https://developer.android.com/studio
2. **Buka project**: File → Open → pilih folder `WebViewApp`
3. **Tunggu** Gradle sync selesai
4. **Build APK**: Build → Build Bundle(s) / APK(s) → Build APK(s)
5. **Lokasi APK**: `app/build/outputs/apk/debug/app-debug.apk`
6. **Transfer APK** ke HP via USB/Google Drive/WhatsApp
7. **Install**: Aktifkan "Unknown Sources" di Settings HP, lalu install APK

### Metode 2: Command Line (Gradle)

```bash
cd WebViewApp
chmod +x gradlew
./gradlew assembleDebug
# APK ada di: app/build/outputs/apk/debug/app-debug.apk
```

---

## ⚙️ Konfigurasi

Untuk mengubah URL target, edit file:
`app/src/main/java/com/tms3206/webview/MainActivity.java`

Cari baris:
```java
private static final String TARGET_URL = "https://tms3206.aseli2025.my.id/";
```

---

## 📋 Struktur Project

```
WebViewApp/
├── app/
│   ├── src/main/
│   │   ├── java/com/tms3206/webview/
│   │   │   └── MainActivity.java       ← Logic utama WebView
│   │   ├── res/
│   │   │   ├── layout/activity_main.xml ← Tampilan UI
│   │   │   └── values/
│   │   │       ├── strings.xml
│   │   │       └── styles.xml
│   │   └── AndroidManifest.xml         ← Konfigurasi app
│   └── build.gradle
├── build.gradle
├── settings.gradle
└── gradle.properties
```

---

## 🔒 Izin yang Dibutuhkan
- `INTERNET` - Untuk mengakses website
- `ACCESS_NETWORK_STATE` - Untuk cek koneksi

---

## ⚠️ Catatan Install di HP
1. Masuk **Settings** → **Security** → Aktifkan **Unknown Sources** (atau "Install unknown apps")
2. Buka file APK dan klik Install
3. Di Android 8+: Settings → Apps → izinkan dari sumber tertentu
