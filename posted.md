# Yayınlananlar

Ne çıktı, ne zaman, nasıl gitti. Hangi klibin tuttuğunu bilmeden
[[system|PICKING.md]] kurallarını iyileştiremeyiz — asıl değeri bu tablo.

## İlk gerçek veri — 2026-11-18 akşam

| Video | YouTube | Instagram |
|---|---|---|
| The GTA 6 verdict is in | **6** | **146** |
| GTA 6 police can describe... | **2** | **68** |
| You can read a GTA 6 code... | **5** | — |
| GTA 6 plane theft... | 0 (yeni) | 0 (yeni) |

Kanal: YouTube **@sixstarplay** (2 abone, 4 video) · Instagram **@6starplaysgta** (3 post, 0 takipçi)

**Instagram YouTube'u 24 kat geçiyor** — aynı klip, 146'ya 6. Takipçi sıfırken.
Örneklem küçük ve kanal yeni, ama yön net.

Görseller ChatGPT ile yapılmış özel kapaklar — iyi duruyorlar.

---


## Sistem öncesi

2026-11-17 gecesi ve 2026-11-18 sabahı YouTube'a **2 video** elle yüklendi,
bu sistem kurulmadan önce. Bu tablolara dahil değiller.

## 2026-11-18 — Typical Gamer, çalınan uçak  ✅ YAYINDA

İlk gerçek post.

Kaynak: `youtube.com/shorts/fkXgQJbj8IE` (2.0 dk, Typical Gamer)
Klip: `C:\Users\Trevo\Shorts\2026-11-18_1715\1.mp4`

| | |
|---|---|
| Başlık | GTA 6 plane theft ends with a parachute onto a skyscraper |
| Süre | 44.1 sn |
| Sabit etiketler | `#GTA6 #GTAVI #RockstarGames` |
| Değişken etiketler | **`#GTA6Planes` `#GTA6Gameplay`** |
| Müzik | tense, −18 dB |
| Yayınlandı | **YouTube** ✅  **Instagram** ✅  (TikTok yok) |

**İzlenme (bir hafta sonra doldur):**

| YouTube toplam | YT aramadan | Instagram toplam | IG takipçi dışı |
|---|---|---|---|
| | | | |

---

## 2026-11-18 — GTA 6, gameranx "Before You Buy"

Kaynak: `youtube.com/watch?v=vVVIWEGciKk` (25.7 dk)
Klipler: `C:\Users\Trevo\Shorts\2026-11-18_1007\`
Sabit etiketler: `#GTA6 #GTAVI #RockstarGames` (her postta aynı)

> Bu üçü Yaser'e göre **yayına hazır değil** (2026-11-18): müziksiz ve
> altyazı düzeltmesinden önce çıktılar.

| #   | Başlık                                                     | Süre  | Planlanan | YouTube | TikTok | Instagram |
| --- | ---------------------------------------------------------- | ----- | --------- | ------- | ------ | --------- |
| 1   | GTA 6 review: is it worth the hype                         | 31 sn | 10:00     | ⬜       | ⬜      | ⬜         |
| 2   | GTA 6 police can describe what you wore and what you drove | 51 sn | 14:00     | ⬜       | ⬜      | ⬜         |
| 3   | GTA 6 after 62 hours: not the greatest game ever           | 34 sn | 18:00     | ⬜       | ⬜      | ⬜         |

**İzlenme (1 hafta sonra doldur):**

| # | Değişken etiketler | YT toplam | YT **aramadan** | IG toplam | IG **aramadan** |
|---|---|---|---|---|---|
| 1 | #GTA6Review #GTA6Gameplay | | | | |
| 2 | #GTA6Police #GTA6Tips | | | | |
| 3 | #GTA6Review #GTA5 | | | | |

---

## Nasıl ölçüyoruz

Toplam izlenme bir şey söylemiyor — iyi giden bir video etiketler sayesinde mi
yoksa akışta şans eseri mi tuttu, oradan anlaşılmıyor. Ölçtüğümüz şey
**kaç izlenmenin aramadan geldiği.**

| Platform | Nereye bakılır |
|---|---|
| **YouTube** | Studio → video → Analytics → Reach → *Traffic source* → **YouTube search** |
| **Instagram** | Reels → İstatistikler → *Views* → **from non-followers / search** |

Aramadan gelen pay artıyorsa anahtar kelimeler işe yarıyor demektir.
Sadece toplam artıyorsa işi içerik yapıyor, etiketler değil.

## Test kurgusu

| | |
|---|---|
| **Sabit** (hiç değişmez) | `#GTA6` `#GTAVI` `#RockstarGames` |
| **Değişken** (klibe göre 2 tane) | `#GTA6Tips` `#GTA6Review` `#GTA6Police` `#GTA6Money` `#GTA6Secrets` `#Leonida` |
| **Süre** | ~30 post, yaklaşık 2 hafta |
| **Karar tarihi** | 2026-12-02 |

Sabit üçlü kontrol grubu: her postta aynı oldukları için, aradaki farkı
değişken ikiliye bağlayabiliyoruz.

> **Dürüst uyarı:** günde 3 post ile bu tam bir deney değil — konu, uzunluk ve
> saat de değişiyor. 30 postta ancak kaba bir eğilim görünür. Kesin cevap
> veren tek şey yukarıdaki *aramadan gelen izlenme* oranı.

## Ne işe yarıyor, ne yaramıyor

Üç-dört parti sonra buraya bir şeyler yazılabilir hale gelecek. Bakılacaklar:

- Hangi **uzunluk** tutuyor — 30 sn mi 50 sn mi
- Başlıkta **sayı** olması fark ediyor mu (*62 saat*, *$1.5 milyar*)
- Hangi **saat** daha iyi gidiyor
- Hangi platform bu içeriği seviyor
