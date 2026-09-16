# 🌍 Earthquake Monitoring by NICO

<div align="center">

**Dünya genelindeki depremleri anlık olarak izleyen, modern bir Android uygulaması.**

[![Sürüm](https://img.shields.io/badge/S%C3%BCr%C3%BCm-1.0.1.1-FF3B30?style=for-the-badge)](https://github.com/aayurtseven01/earthquake_monitoring)
[![Platform](https://img.shields.io/badge/Platform-Android%207.0%2B-3DDC84?style=for-the-badge&logo=android)](https://developer.android.com)
[![Kotlin](https://img.shields.io/badge/Kotlin-Jetpack%20Compose-7F52FF?style=for-the-badge&logo=kotlin)](https://kotlinlang.org)
[![Reklam](https://img.shields.io/badge/Reklam-YOK-00C853?style=for-the-badge)](https://aayurtseven01.github.io/earthquake_monitoring/)

[📄 Gizlilik Politikası](https://aayurtseven01.github.io/earthquake_monitoring/)

</div>

---

## 🔴 ÖNEMLİ UYARI — LÜTFEN DİKKATLE OKUYUN

![Önemli Uyarı](uyari.png)

### ⚠️ BU UYGULAMA BİR ERKEN UYARI SİSTEMİ DEĞİLDİR.

> **Veriler; EMSC (Avrupa-Akdeniz Sismoloji Merkezi) başta olmak üzere
> ÜÇÜNCÜ TARAF sismoloji kuruluşlarının kamuya açık servislerinden
> AKTARILMAKTADIR. Uygulamanın kendine ait bir ölçüm ağı veya veri
> üretimi YOKTUR.**

**Bilmeniz gerekenler:**

- ⏱️ **GECİKMELER OLABİLİR.** Deprem bilgisinin kaynaktan alınması,
  işlenmesi ve cihazınıza ulaşması zaman alır. Görünen veriler depremin
  gerçekleştiği anı birebir yansıtmayabilir.

- 🔄 **VERİLER REVİZE EDİLEBİLİR.** Bir depremin büyüklük, derinlik ve
  konum bilgileri ilk yayından sonra uzmanlarca düzeltilebilir. İlk
  bildirilen değerler kesin değildir.

- 🔌 **KESİNTİ OLABİLİR.** Veri sağlayıcı servislerde bakım veya erişim
  sorunu yaşanabilir. Böyle durumlarda liste güncellenmeyebilir; uygulama
  eski veri gösterdiğini açıkça belirtir.

- 🚫 **ACİL DURUM KARARLARINDA TEK BAŞINA KULLANILMAMALIDIR.** Bu uygulama
  hayati güvenlik amacıyla tek kaynak olarak alınmamalıdır.

<br>

> ### 🔴 **Resmî ve doğrulanmış bilgi için daima AFAD ve Kandilli Rasathanesi kaynaklarına başvurunuz.**

---

## ✨ Özellikler

### 🗺️ İki farklı görünüm
- **2D Harita** — OpenTopoMap topoğrafik haritası üzerinde deprem işaretçileri
- **3D Etkileşimli Küre** — depremleri dünya üzerinde üç boyutlu görün,
  parmağınızla döndürün, yakınlaştırın

### 🔔 Akıllı bildirimler
- Yeni deprem olduğunda **sesli ve titreşimli** uyarı
- **Minimum şiddet eşiği** (M2.5 – M7.0) — hangi büyüklükte uyarı alacağınızı siz seçersiniz
- Bildirimler ve ses tamamen kapatılabilir
- Eşik **yalnızca uyarıyı** etkiler; deprem listesi tüm depremleri göstermeye devam eder

### 🎛️ Gelişmiş filtreleme
- **Zaman:** Güncel (3 saat) · Son 1 saat · Son 24 saat · Son 7 gün
- **Bölge:** 15 ülke + Dünya geneli
- **Şiddet:** liste içinde alt/üst sınır

### 🌓 Tema
- Harita ve küre dokusu için **koyu / açık** tema
- Sistem temasını izler veya elle değiştirilir

### 📴 Çevrimdışı destek
- Son deprem listesi cihazda saklanır
- Bağlantı yoksa önbellek gösterilir ve **"eski veri"** olarak açıkça işaretlenir

### ⚙️ Diğer
- **Ekranı açık tut** seçeneği (varsayılan açık)
- **Türkçe / İngilizce** tam çeviri
- Otomatik yenileme: ön planda 75 saniyede bir, arka planda 15 dakikada bir

---

## 🔒 Gizlilik

| | |
|---|---|
| Reklam | ❌ Yok |
| Analitik / izleme | ❌ Yok |
| Konum izni | ❌ İstenmez |
| Hesap / üyelik | ❌ Yok |
| Veri satışı | ❌ Yok |

Uygulama yalnızca iki şey için internete bağlanır:
1. **EMSC** (Avrupa-Akdeniz Sismoloji Merkezi) — deprem verisi
2. **OpenTopoMap** — harita görüntüleri

Bu istekler her web isteğinde olduğu gibi IP adresinizi içerir. Tam açıklama
için **[gizlilik politikasını](https://aayurtseven01.github.io/earthquake_monitoring/)**
okuyun.

**İzinler:** yalnızca `INTERNET`, `ACCESS_NETWORK_STATE`, `POST_NOTIFICATIONS`, `VIBRATE`.

---

## 🛠️ Teknolojiler

| Katman | Kullanılan |
|---|---|
| **Dil / UI** | Kotlin, Jetpack Compose, Material 3 |
| **Ağ** | Retrofit, OkHttp, Gson |
| **2D Harita** | osmdroid |
| **3D Küre** | Three.js (WebView, APK içinde gömülü) |
| **Arka plan işleri** | WorkManager |
| **Mimari** | MVVM (ViewModel + StateFlow) |
| **Veri kaynağı** | EMSC FDSN event servisi |

**Minimum Android:** 7.0 (API 24) · **Hedef:** API 37

---

## 📊 Veri kaynağı

Deprem verileri, kamuya açık bir sismoloji servisi olan
**[EMSC](https://www.seismicportal.eu/)** (Avrupa-Akdeniz Sismoloji
Merkezi) FDSN event API'sinden anlık olarak çekilir.

Harita görüntüleri **[OpenTopoMap](https://opentopomap.org/)** sunucularından
gelir:

```
Kartendaten: © OpenStreetMap-Mitwirkende, SRTM
Kartendarstellung: © OpenTopoMap (CC-BY-SA)
```

---

## 🧭 Kullanılan ülkeler

Türkiye · ABD · Japonya · Yunanistan · İtalya · Şili · Endonezya ·
Filipinler · Meksika · Peru · Çin · Hindistan · Yeni Zelanda ·
Avustralya · **Dünya**

Varsayılan: **Türkiye**, **M4.0** eşiği.

---

## 📱 Ekran görüntüleri

<!--
Ekran görüntüsü eklemek için:
1. Uygulamada ekran görüntüsü alın
2. Bu depoda `screenshots/` klasörü oluşturup yükleyin
3. Aşağıdaki satırların başındaki yorum işaretini kaldırın

![2D Harita](screenshots/map.png)
![3D Küre](screenshots/globe.png)
![Ayarlar](screenshots/settings.png)
-->

---

## 👤 Geliştirici

**NICO**

---

## 📄 Lisans ve yasal

- Uygulama kodu © 2026 NICO
- Harita verisi © OpenStreetMap katkıcıları
- Harita görselleştirme © OpenTopoMap — [CC-BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)
- Deprem verisi © EMSC

Bu uygulama resmî bir erken uyarı sistemi değildir ve acil durumlar için
tek başına güvenilir bir kaynak olarak kullanılmamalıdır.

---

<div align="center">

*Son güncelleme: 16 Eylül 2026 · Sürüm 1.0.1.1*

</div>
