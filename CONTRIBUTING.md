# Katkı Rehberi

KABAK AVI'ye katkı vermek istediğin için teşekkürler! 🎃 Bu proje **tek dosyalık, bağımlılıksız** bir oyun
olarak kalmayı hedefler; bu yüzden katkılarda aşağıdaki kurallara dikkat etmek önemlidir.

## 🎯 Temel kurallar

1. **Bağımlılık ekleme yok.** Harici kütüphane, çerçeve (framework), font dosyası, görsel veya ses dosyası kullanılmaz.
   Her şey Canvas 2D ile çizilir, WebAudio ile sentezlenir.
2. **Tek dosya.** Oyunun tamamı `oyna.html` içinde yaşar. (Tanıtım sayfası `index.html` istisnadır.)
3. **Türkçe.** Arayüz metinleri, ipuçları ve kod yorumları Türkçe olur.
4. **60 FPS.** Değişikliklerinden sonra oyunun akıcılığını kontrol et; kare başına ağır iş yapma,
   katmanları ön-render et.
5. **Göç (migration).** Kayıt yapısına alan ekliyorsan `loadSave()` içinde eski kayıtlar için varsayılan değer ata.

## 🚀 Akış

```bash
# 1) Çatalla (fork) ve klonla
git clone https://github.com/<kullanıcı>/kabak-avi.git
cd kabak-avi

# 2) Konu dalı aç
git checkout -b ozellik/yeni-biyom

# 3) Geliştir, tarayıcıda test et
python -m http.server 8777   # http://127.0.0.1:8777/oyna.html

# 4) Commit ve gönder
git commit -m "Yeni biyom: Sisli Liman"
git push origin ozellik/yeni-biyom
```

Ardından bir **Pull Request** aç. PR şablonundaki kontrol listesini doldur.

## 🧪 Test kontrol listesi

Pull request açmadan önce:

- [ ] `oyna.html` tarayıcıda hatasız açılıyor, **konsol temiz** (`F12 → Console`)
- [ ] Bir sefer başlatıldı ve **en az 2 kat** sorunsuz oynandı
- [ ] FPS göstergesi menüden açılıp kontrol edildi (hedef: 60)
- [ ] Kooperatif mod açılıp kapatıldı (2. oyuncu botu çalışıyor)
- [ ] Sayfa yenilendiğinde kayıt korunuyor (eski kayıt göçü bozulmadı)
- [ ] Yeni metinler Türkçe ve arayüze sığıyor

## 🐛 Hata bildirimi

[Issue aç](../../issues/new?template=bug_report.md) ve şablonu doldur: tarayıcı sürümü, yeniden üretme adımları,
beklenen davranış ve varsa konsol çıktısı.

## 💡 Öneri

[Öneri şablonunu](../../issues/new?template=feature_request.md) kullan. Oyunun ruhuna uygun mu? (sonbahar,
prosedürel üretim, tek dosya, hızlı tur döngüsü)

## 📜 Lisans

Katkıların [MIT lisansı](LICENSE) altında yayımlanır.
