# Sistem

Günde 3 video, sıfır abonelik, sunucu açık kalmadan.

## Sabah rutini (~10 dakika)

```
1. Claude'a uzun videonun linkini at
2. 3 klip + başlık/açıklama C:\Users\Trevo\Shorts klasörüne düşer
3. Her birini yükle, saatini ver:  1 → 10:00   2 → 14:00   3 → 18:00
4. Bilgisayarı kapat
```

4. adım önemli: **planladıktan sonra PC'nin açık kalması gerekmiyor.** Videoyu
platform yayınlıyor, biz değil. Konuştuğumuz bütün otomasyon seçeneklerinden
bu yüzden üstün — bkz. [[decisions]].

## Platformların kendi zamanlaması

| | Nereden | Ne kadar ileri | Not |
|---|---|---|---|
| **YouTube** | Studio, yükleme sırasında Visibility → Schedule | aylarca (kaynaklar 6-12 ay diyor) | Shorts için de çalışır. Telefondan da var ama sürüme göre yeri değişiyor |
| **TikTok** | **Sadece masaüstü tarayıcı** (tiktok.com) | 15 dakika – **10 gün** | Telefon uygulamasında yok. Planlanan post düzenlenemiyor, sadece silinebiliyor |
| **Instagram** | Uygulama içinde: iOS'ta Advanced settings, Android'de More options | ~75 gün (bazı kaynaklar 30 diyor) | Professional (Business/Creator) hesap gerekiyor olabilir |

TikTok masaüstü şart olduğu için **sabah rutini masaüstü PC'de yapılmalı.**

> Bu sayılar üçüncü taraf kaynaklardan, platformlar sık değiştiriyor.
> Uyuşmazlık olursa platformun kendi yardım sayfası doğrudur.

## Instagram hesabı

YouTube ile aynı isim ve fotoğraf, Reels için açıldı ve **kuruldu** (2026-11-18).
Kategori: Gaming Video Creator. Aşağıdakilerin hepsi yapıldı.

| Ayar | Olması gereken | Neden |
|---|---|---|
| Hesap tipi | **Creator** (Business değil) | Business'ta müzik kütüphanesi kısıtlanabiliyor; Creator'da trend sesler duruyor |
| Gizlilik | Herkese açık | Gizli hesapta Reels keşfete düşmez, zamanlama da çalışmaz |
| Yükleme kalitesi | *Upload at highest quality* **açık** | Kapalıyken Instagram fazladan sıkıştırıyor. Sadece telefon uygulamasında var |
| *Use less cellular data* | **kapalı** | Kaliteyi düşürüyor. Reels'i Wi-Fi'dayken yükle |
| Facebook sayfası | **Karar verilmedi** | Bilgisayardan planlamak için gerekli — aşağıya bak |

> **Business'a geçme.** Geçersen daha önce attığın Reels'lerin sesi susabilir.

### Instagram nereden planlanır

İki yol var, ikisi de bedava:

| | Nereden | Artısı | Eksisi |
|---|---|---|---|
| **Telefon** | Uygulamada, paylaşım son ekranında | Ekstra kurulum yok | Klipleri telefona taşımak gerekiyor |
| **Bilgisayar** | Meta Business Suite (business.facebook.com) | Klipler zaten PC'de, her şey tek yerde | Facebook sayfası + iş portföyü kurmak gerekiyor (~10 dk) |

Instagram'ın kendi web sitesinden Reels planlanamıyor — sadece bu iki yol.
Business Suite kullanmak hesabı Business'a çevirmez; Creator kalabilir.
(Bu son cümle doğrulanmadı, kurarken kontrol edilecek.)

**İzlenecek şey:** Instagram tamamlanma oranını ödüllündürüyor, ve bizim klipler
30-60 saniye. YouTube ve TikTok bu uzunluğu sorun etmiyor ama Instagram'da
kısa olanlar daha iyi gidebilir. [[posted]] tablosu birkaç parti sonra bunu
söyleyecek — şimdiden kuralları değiştirmeye gerek yok.

## Kaç post, ne sıklıkta

| | Günlük |
|---|---|
| **YouTube** | 3 — 10:00 / 14:00 / 18:00 |
| **Instagram** | 1-3, serbest |

### Düzeltme: önce fazla temkinli davrandım

2026-11-18'de buraya "yeni hesapta ilk 2 hafta günde 1 Reels" diye yazdım.
Yaser itiraz etti, haklıydı. Kaynaklara tekrar bakıldığında:

- Meta yeni hesaplar için **ayrı bir günlük limit yayınlamıyor**
- Resmî limit hesap başına **24 saatte 100 post**
- Korkutucu tek örnek günde **25-30 Reels** atan bir hesaptı — bizim sayımızın
  on katı
- "Isınma dönemi" tavsiyesi pazarlama bloglarından, ve büyük ölçüde **otomatik
  takip/beğeni** yapan hesaplardan geliyor — içerik paylaşmaktan değil

Hesap engelleri paylaşımdan değil, **otomatik etkileşimden** (toplu takip,
beğeni, DM) geliyor. Biz onları yapmıyoruz.

### Gerçek olan tek küçük risk

Aynı videodan çıkan 3 klibi aynı gün atmak **birbirleriyle yarıştırıyor** — aynı
kitle, aynı konu. Ban meselesi değil, verim meselesi. Saatleri ayırmak
(10/14/18) bunu zaten büyük ölçüde çözüyor.

**Karar: 3/gün at, sayılara bak.** [[posted]] tablosu bir şey söylerse o zaman
değiştiririz — blog tahminine göre değil.

## Dosyalar nerede

| | |
|---|---|
| Program | `C:\Users\Trevo\clipmaker` |
| Klip seçme kuralları | `clipmaker\PICKING.md` — düzenlenebilir, hem Claude hem rutin okuyor |
| Çıkan klipler | `clipmaker\clips\<tarih>\` |
| **Klip klasörü** | `C:\Users\Trevo\Shorts\<tarih>\` → `1.mp4` `2.mp4` `3.mp4` + `POST.txt` |
| Link kuyruğu | `clipmaker\queue.txt` (işlenenler `done.txt`) |

`POST.txt` içinde her klip için başlık, açıklama, etiketler ve planlanacak
saat var. Yüklerken oradan kopyala-yapıştır.

Eski partiler siliniyor — son 5 duruyor, disk dolmasın diye (3 klip ≈ 100 MB).

## Komutlar

Elle klip çıkarmak:

```powershell
shorts "https://www.youtube.com/watch?v=..." -Clips 3
```

Var olan klipleri klip klasörüne kopyalamak:

```powershell
C:\Users\Trevo\clipmaker\publish.ps1
```

## Günde 3 kez otomatik rutin

Claude'un scheduled task'ı 10:00 / 14:00 / 18:00'de çalışıyor:
`queue.txt`'deki sıradaki linki alır, 3 klip çıkarır, klip klasörüne atar.

**Sadece Claude uygulaması açıkken çalışır.**
