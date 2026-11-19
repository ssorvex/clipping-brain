# Clipping

Uzun videolardan kısa dikey klipler çıkarıp günde 3 tane yayınlamak.

## Şu an nerede

| | |
|---|---|
| **Durum** | İlk 3 klip hazır — **henüz hiçbiri yayınlanmadı** |
| **Günlük hedef** | 3 video: 10:00 / 14:00 / 18:00 |
| **Yayın şekli** | Elle yükle + platformun kendi zamanlaması ([[system]]) |
| **Maliyet** | $0 |

## Sıradaki adım

- [ ] 2026-11-18 GTA 6 kliplerini yükle ve saatlerini ver
- [ ] Birkaç gün paylaş, **neyin yavaşlattığını gör**, sonra onu otomatikleştir

## Her gün buraya bak

**`posts/<bugünün tarihi>.md`** — o gün yüklenecek 3 video, alt alta.
Her alan kendi kod bloğunda; sağ üstteki kopyala düğmesi tam olarak
yapıştırılacak metni veriyor. Link, başlık, açıklama, etiketler, saat.

Kendiliğinden yazılıyor — elle düzenlemeye gerek yok.

## Sayfalar

- `posts/` — **günlük kopyala-yapıştır sayfası** (otomatik)
- [[system]] — sistem nasıl çalışıyor, sabah rutini
- [[thumbnails]] — kapak görseli promptu (ChatGPT'ye yapıştır)
- [[posted]] — ne yayınlandı, nasıl gitti
- [[decisions]] — neyi neden seçtik, neyi reddettik
- `journal/` — günlük kayıt

## Kurulu olanlar

| Ne | Nerede | Durum |
|---|---|---|
| clipmaker | `C:\Users\Trevo\clipmaker` | ✅ çalışıyor |
| Klip seçme kuralları | `clipmaker\PICKING.md` | ✅ |
| Klip klasörü | `C:\Users\Trevo\Shorts\` | ✅ |
| Günde 3 kez rutin | Claude scheduled task | ✅ 10:00/14:00/18:00 |
| YouTube kanalı | — | ✅ 2 video yüklendi |
| Instagram hesabı | Creator, herkese açık | ✅ kuruldu, henüz post yok |
| TikTok hesabı | — | ⬜ yok |

## Kenarda duranlar

Çalışıyorlar ama kullanılmıyorlar — bir ihtiyaç doğarsa uyandırılır.

| Ne | Uyanma şartı |
|---|---|
| Web arayüzü (`server.py` + `web/`) | Claude olmadan klip çıkarma ihtiyacı + API anahtarı (~$4-7/ay) |
| WoopSocial paylaşımı (`cm/woop.py`) | Elle yüklemek yavaşlatmaya başlarsa + bedava hesap |
