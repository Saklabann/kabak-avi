# KABAK AVI — Android

`oyna.html` oyununu tam ekran bir WebView içinde çalıştıran Android sarmalayıcısı.

## Derleme

1. Oyunu varlıklara kopyala:

   ```bash
   cp ../oyna.html app/src/main/assets/index.html
   ```

2. `android/` klasörünü Android Studio'da aç veya Gradle ile derle:

   ```bash
   gradle assembleDebug
   ```

3. Çıktı: `app/build/outputs/apk/debug/app-debug.apk`

## Gereksinimler

- JDK 17
- Android SDK 34 + build-tools 34.0.0
- Gradle 8.5 veya üzeri

## Ayrıntılar

| | |
|:--|:--|
| Paket | `com.saklabann.kabakavi` |
| Sürüm | 2.1.0 (versionCode 21) |
| minSdk / targetSdk | 23 / 34 |
| Yön | Yatay (sensorLandscape), immersive tam ekran |
| İzinler | Yalnızca `VIBRATE` — internet izni yok |
| İçerik | `app/src/main/assets/index.html` (derleme sırasında kopyalanır) |

Geri tuşu oyun sırasında oyunu duraklatır; menüdeyken uygulamadan çıkar.
