# Değişiklik Günlüğü

Bu projede tüm önemli değişiklikler bu dosyada belgelenir.
Biçim: [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) · Sürümleme: [SemVer](https://semver.org/lang/tr/)

---

## [2.0.0] — 2026-10-19 — 🍂 **Sezon 2 · Canlı Dünya**

### Eklendi

**İçerik**
- **Elit rütbeler:** ZIRHLI (%38 direnç), HIZLI (+%30 hız), ZEHİRLİ (ölünce zehir gölü bırakır), KADİM (+%35 can, +%50 altın)
- **Gizli odalar:** her katta 1 adet; çatlak taş duvarla örülü, haritada görünmez. Kırınca "Gizli Kapı" başarımı + sandık + 7 ganimet
- **Yeni düşmanlar:** *hayalet* (uçan, ışınlanan) ve *mantar* (3'lü spor atışı + zamanlı zehir gölü)
- **4 yeni yadigâr:** SİS BIÇAĞI (dash hasarı), BUZ ÇEKİRDEĞİ (dondurma), KIRIK AYNA (+kritik hasar), YILDIZ KÜRESİ (+%30 TP) → toplam **29**
- **2 yeni kutsama:** ALTIN KESE (+%12 altın), BİLGİ KÜRESİ (+%10 TP) → toplam **10**
- **Bilge Baykuş:** başlangıç odasında tüneyen rehber NPC; kat başına bir kez konuşur, ipucu + 8 TP verir
- **Sincap:** bahçe ve korda koşan, oyuncudan kaçan yeni canlı

**Canlı dünya**
- Yaprak burgaçları: rüzgâr esintisinde yapraklar burgaçlanır, çimenler eğilir, uğultu duyulur
- Mum, meşale ve ateş çukurlarından tüten duman
- Gece çöktüğünde her biyomda süzülen ateşböcekleri
- Gökyüzünden geçen kuş sürüleri (kanat çırpma animasyonlu)
- Kemik Tarlası'nda şimşek çakması + gecikmeli gök gürültüsü
- Yağmur damlalarının su birikintilerine düşmesi, ağaçlardan yaprak düşmesi

**Ses**
- Sürekli rüzgâr katmanı, yağmur hisirtisi, gündüz kuş cıvıltısı, gece cırcır sesi, baykuş "huu"su
- Adım sesleri (toz ve çamur izleriyle senkron)

**Arayüz ve sistemler**
- **Arayüz baştan tasarlandı** — tanıtım sayfasıyla aynı tasarım dili (cam paneller, amber vurgular, yuvarlatılmış kartlar):
  - Ana menü: kabak logosu, gradyan başlık, istatistik kartları, hap biçimli ayar düğmeleri,
    katlanabilir bilgi kartları ve süzülen sonbahar yaprakları
  - HUD: kalp/altın kutusu, kat-süre paneli ve silah göstergesi artık cam kart içinde; boss can barı üst-ortaya taşındı
  - Duraklatma, ölüm, mağaza ekranları ile Av Haritası ve yadigâr seçim ekranları yeni tasarıma uyarlandı
  - Tüm başlıklar "Segoe UI 900" + amber gradyan; ince çerçeveli yuvarlatılmış kartlar
- Tüccarda **vitrin yenileme tezgahı** (🎲 8✦)
- HUD'a **sefer süresi** sayacı ve **FPS** göstergesi
- Ayarlar: **hasar sayıları** aç/kapa, **FPS** aç/kapa, **tam ekran** düğmesi
- Menüde genişletilmiş istatistikler: toplam av, en iyi temizlenen oda, başarım sayacı
- **Duraklatma ekranında sefer özeti** (süre, kat, av, altın, ruh, yadigâr, kombo, oyuncu durumları)
- Sekme değiştirilince **otomatik duraklatma**
- Mobil için **silah değiştir** ve **fırlat** düğmeleri
- Yer silahı yanında **"F / ✋ AL"** ipucu
- Başarımlar **12 → 15** (Gizli Kapı, Yüce Büyücü, Hazine Sandığı)
- Zehir gölleri artık zamanla kaybolur (mantar ve ZEHİRLİ elit)

**Proje**
- Profesyonel tanıtım sayfası (`index.html`) — hero, özellik kartları, ekran görüntüleri, kontrol tabloları
- README, MIT lisans, sosyal önizleme görseli, issue/PR şablonları
- GitHub Pages yayını

### Değişti
- Menü düzeni kaydırılabilir ve kompakt hâle getirildi (küçük ekranlarda taşma giderildi)
- Mini harita ile silah göstergesinin çakışması giderildi
- HUD çizim sırası düzeltildi (mini harita → silah göstergesi)
- Oyun `neon-arena.html` → `kabak-avi.html` (oyun dosyası) olarak yeniden adlandırıldı

### Düzeltildi
- `updateEnemies` geri döngüsünde ölü düşman koruması (`if (!e) continue`)
- Ana döngü try/catch + hata sayacı: tek kare hatası artık oyunu kilitlemez
- **Negatif `dt` koruması:** zaman damgası geriye döndüğünde (sekme/pencereler arası geçiş) şimşek küresinin
  yarıçapı negatif hesaplanıp kare hatası üretiyordu (`arc` IndexSizeError) — `dt` artık alt sınırı 0,
  yarıçaplar güvenli aralıkta
- **Şarj göstergesi** çizimi: gölgelenen `W` değişkeni yüzünden şarj barı ve etiketi ekran dışına çiziliyordu — düzeltildi
- Eski kayıtlar (Sezon 1) otomatik göç ettirilir; ilerleme kaybı yok

---

## [1.0.0] — 2026-10-18 — 🎃 **Sezon 1**

### Eklendi
- Oda tabanlı prosedürel zindan döngüsü; mini harita, kilitli kapılar, hazine ve tüccar odaları
- **4 biyom ve 4 patron:** Balkabağı Bahçesi (Korkuluk Efendisi), Çürük Koru (Balkabağı Kralı), Kemik Tarlası (Kemik Lordu), Mezar Vadisi (Orman Cadısı)
- **Voidigo'dan ilham alan sistemler:** silah düşür/değiştir/fırlat, parçalanabilir patron parçaları, yolsuzluk zinciri, av haritası, yerel 2 kişilik kooperatif
- 5 sınıf (Büyücü, Karakabak, Cüce Demirci, Cadı Kızı, Çılgın Palyaço) ve 4 evcil hayvan
- 7 silah, mühimmat/kırılma mekaniği, nadirlik seviyeleri
- Yadigârlar, meta kutsamalar, ruh ekonomisi, zorluk modları
- Prosedürel çizim (Canvas 2D) ve sentezlenmiş müzik/ses (WebAudio)
- 12 başarım, kombo sayacı, duraklatma/ölüm/tüccar ekranları
- Dokunmatik kontroller

---

[2.0.0]: https://github.com/Saklabann/kabak-avi/compare/v1.0.0...v2.0.0
[1.0.0]: https://github.com/Saklabann/kabak-avi/releases/tag/v1.0.0
