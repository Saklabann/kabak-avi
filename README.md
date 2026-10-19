# 🎃 KABAK AVI — Sonbahar Büyücüsü

**Tek dosyalık, prosedürel sonbahar temalı 2D aksiyon roguelite.** Tarayıcıda çalışır, kurulum istemez, hiçbir harici dosya ya da kütüphane kullanmaz. Tüm grafikler Canvas 2D ile çizilir, tüm sesler WebAudio ile sentezlenir.

![sürüm](https://img.shields.io/badge/s%C3%BCr%C3%BCm-2.0%20(Sezon%202)-ff7a2f)
![lisans](https://img.shields.io/badge/lisans-MIT-3da639)
![tek dosya](https://img.shields.io/badge/tek%20dosya-ba%C4%9F%C4%B1ml%C4%B1l%C4%B1ks%C4%B1z-8b5cf6)
![dil](https://img.shields.io/badge/dil-T%C3%BCrk%C3%A7e-ffb24a)

---

## ✨ Hemen Oyna

👉 **https://kabak-avi.example** *(GitHub Pages adresi — yayınlandığında buraya yazılır)*

ya da depoyu indirip `oyna.html` dosyasına **çift tıkla**. Hepsi bu.

```bash
git clone <depo-adresi>
cd kabak-avi
# oyna.html dosyasını tarayıcıda aç
```

Yerel bir sunucu tercih edersen:

```bash
python -m http.server 8777
# http://127.0.0.1:8777/oyna.html
```

---

## 🖼️ Ekran görüntüleri

| Balkabağı Bahçesi | Patron: Korkuluk Efendisi |
|---|---|
| ![bahçe](assets/screens/bahce.jpg) | ![patron](assets/screens/patron.jpg) |

| Kemik Tarlası (gece · yağmur) | Av Haritası |
|---|---|
| ![yağmur](assets/screens/yagmur.jpg) | ![harita](assets/screens/harita.jpg) |

---

## 🎮 Oyun

Sonbahar diyarı çürümeye teslim olmuş; sen bir sonbahar büyücüsüsün. Kat kat inen prosedürel zindanlarda,
kapılar kilitlenir, düşmanlar fışkırır, patronlar uyanır. **Voidigo'dan ilham alan beş sistem** oyunun omurgası:

| Sistem | Ne yapar |
|---|---|
| 🔫 **Silah düşür / değiştir / fırlat** | Düşmanlar silah bırakır; mühimmat biter, silah kırılır. Yerden al, kuşan ya da düşmana fırlat. |
| 🦴 **Parçalanabilir patronlar** | Kollar, boynuzlar, kaburgalar ve büyü küreleri ayrı ayrı kırılabilir; kırılan parça patronu zayıflatır. |
| 🟣 **Yolsuzluk zinciri** | Vuruşlar yolsuzluk yükler; dolan düşman patlar ve çevreye zincirleme yayılır. |
| 🗺️ **Av haritası** | Her kat sonunda 3 bölge arasından seçim; zorluk ve ödüller bölgeye göre değişir. |
| 👥 **Yerel 2 kişilik** | Aynı klavyede iki oyuncu. 2. oyuncuyu yapay zekâya bırak veya ok tuşlarıyla devral. |

### Öne çıkanlar

- **4 biyom · 4 patron** — Balkabağı Bahçesi (Korkuluk Efendisi), Çürük Koru (Balkabağı Kralı), Kemik Tarlası (Kemik Lordu), Mezar Vadisi (Orman Cadısı)
- **29 yadigâr (relic)** ve **10 kalıcı kutsama** (ölsen bile harcanabilen ruhlar)
- **5 sınıf** (Büyücü, Karakabak, Cüce Demirci, Cadı Kızı, Çılgın Palyaço) + **4 evcil hayvan**
- **7 silah** — mühimmat, kırılma, nadirlik seviyeleri ve fırlatma mekaniği
- **Elit rütbeler** — ZIRHLI, HIZLI, ZEHİRLİ, KADİM
- **Gizli odalar** — çatlak duvarı kır, haritada görünmeyen hazineyi bul
- **Başarımlar, kombo sayacı, sefer özeti, günlük/haftalık istatistikler**
- **Canlı dünya (Sezon 2)** — yaprak burgaçları, mum dumanı, gece ateşböcekleri, gökyüzünde kuş sürüleri, şimşek + gök gürültüsü, yağmur sesi, sincaplar, ayak sesleri ve **Bilge Baykuş**
- **Dokunmatik destek** — telefonda sanal joystick ve aksiyon düğmeleri

---

## ⌨️ Kontroller

### 1. Oyuncu

| Tuş | İşlev |
|---|---|
| `W` `A` `S` `D` | Hareket |
| `Fare` | Nişan alma · **sol tık** ateş · **sağ tık** ışın (beam) |
| `Boşluk` | Dash — kaçış ve çarpma hasarı |
| `E` | Etkileşim (sandık, tüccar, baykuş, yer silahı) |
| `F` / `Q` | Silah değiştir / fırlat |
| `P` / `Esc` | Duraklat |
| `M` | Sesi kapat/aç |

### 2. Oyuncu

| Tuş | İşlev |
|---|---|
| `↑` `↓` `←` `→` | Hareket ve nişan |
| `,` | Dash |
| `.` / `/` | Silah değiştir / fırlat |

> 2. oyuncu varsayılan olarak **yapay zekâ** ile oynar (menüden kapatabilirsin). Kooperatif sefer, **iki oyuncu da ölünce** biter.

### Dokunmatik

Sol yarı: joystick · Sağ düğmeler: dash, ışın, kullan, silah değiştir, fırlat.

---

## 🧠 Nasıl oynanır (özet)

1. Odaya gir — kapılar kilitlenir, düşmanlar gelir. Hepsini devir.
2. Mini haritadan hazine ve tüccar odalarını bul; çatlak duvarları kır.
3. Kat sonunda **yadigâr seç**, av haritasından bir sonraki bölgeyi belirle.
4. En uzak odadaki patronu devir; parçalarını kırmayı unutma.
5. Ölürsen ruhlar seninle kalır — menüdeki kutsamalarla bir dahaki sefere daha güçlü başla.

---

## 🛠️ Teknik

- **Tek dosya:** `oyna.html` — HTML + CSS + JavaScript, toplam ~250 KB. Harici istek yok, çevrimdışı çalışır.
- **Çizim:** Canvas 2D; odalar prosedürel üretilir (`genFloor`, `genDecor`, `renderRoomBg`), zemin/duvar/dekor katmanları önceden render edilir.
- **Ses:** WebAudio ile sentezlenen müzik ve efektler (osilatör + gürültü tamponları); rüzgâr ve yağmur döngü katmanları.
- **Yapay zekâ:** 2. oyuncu botu (`p2Brain`) hedef seçer, menzile göre konumlanır, mermilerden kaçınır ve fırlar.
- **Performans:** Sabit 60 FPS hedefi; dinamik ışık maskesi ve parçacık havuzları sayfa dışına taşmaz.
- **Kayıt:** `localStorage` (`kabakAvi_v1`) — eski kayıtlar otomatik göç ettirilir.

### Proje yapısı

```
kabak-avi/
├─ index.html            # tanıtım sayfası (GitHub Pages)
├─ oyna.html             # oyunun kendisi (tek dosya)
├─ assets/
│  └─ screens/           # ekran görüntüleri
├─ LICENSE
└─ README.md
```

---

## 🗺️ Yol haritası

- [x] Sezon 1 — temel roguelite döngüsü, 4 biyom, patronlar, yadigârlar
- [x] Sezon 2 — elit rütbeler, gizli odalar, yeni düşmanlar, canlı dünya, ortam sesleri
- [ ] Sezon 3 — günlük seferler, liderlik tablosu, yeni biyom (Sisli Liman?)
- [ ] Oyun kolu desteği
- [ ] Çevrimdışı PWA kurulumu

---

## 📄 Lisans

[MIT](LICENSE) © 2026 KABAK AVI

İlham: **Voidigo** (Pretty Beast Games) — bu proje bağımsız bir hayran çalışmasıdır; hiçbir özgün varlık kullanılmamıştır.
