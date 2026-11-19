# Kararlar

Neyi neden seçtik — ve daha önemlisi, **neyi neden reddettik.** Aynı soruyu
iki ay sonra tekrar tartışmamak için.

## Seçilenler

### Klipleri Claude elle seçiyor, program değil
**2026-11-18.** Aynı videoda ölçtük:

| Kim seçti | 1. klibin başlığı |
|---|---|
| Claude (elle) | *"GTA 6 is worth most of the hype"* |
| Yerel program | *"let you kind of tag enemies and plan your route, I was able to..."* |

Program ses yüksekliğine ve konuşma hızına bakıyor — **ilginç olana değil.**
Kurallar [[system|PICKING.md]] dosyasında, düzenlenebilir.

### Elle yükleme + platformun kendi zamanlaması
**2026-11-18.** API ile otomatik paylaşmak yerine sabah 10 dakika elle
yüklemek. Nedeni: bedava, denetim gerektirmiyor, PC'nin açık kalmasını
gerektirmiyor, ve günde 3 post için zaten yeterince hızlı.

### Klip klasörü (yerel, OneDrive değil)
**2026-11-18.** Klipler ve metinler `C:\Users\Trevo\Shorts\` altına düşüyor.
Önce OneDrive'daydı, telefondan atmak için — ama TikTok'un zamanlaması sadece
masaüstünde olduğu için yükleme zaten PC'de yapılıyor. Senkron gereksizdi.

---

## Çözülmesi gereken: YouTube'un "yeniden kullanılmış içerik" kuralı

**2026-11-18.** Hedef: 1000 abone + 90 günde 10M Shorts izlenmesi (YPP).
Rakam doğru. Ama önünde bir duvar var.

YouTube'un **reused content** kuralı telif kuralından ayrı bir **para kazanma**
kuralı. Kaynaklara göre:

- Başkasının videosunu yeniden yüklemek Shorts ödemelerinin **dışında**
- **İzin almak çözmüyor** — telif temiz olsa bile inceleme reddedebiliyor
- Yaptırım **kanal çapında**, tek video değil
- Geçenler: **yorum, tepki, inceleme** — yani kendi katkının olduğu işler

Bizim şu anki modelimiz tam sınırda: başkasının klibine altyazı, müzik ve ses
efekti ekliyoruz. Bu "düzenleme", "katkı" değil.

[[posted]] sayfasındaki ilk veri de bunu destekliyor: aynı klip Instagram'da
146, YouTube'da 6 izlenme.

**Süre baskısı:** 1 Şubat 2027'den sonra yeni başvuranlar için eşik 90 günde
**20M**'e çıkıyor. Yani ~10 hafta.

**Karar verilmedi.** Seçenekler: kendi sesiyle yorum eklemek, kendi oynanışını
kaydetmek, ya da YouTube'u bırakıp Instagram'a yüklenmek.

> Kaynaklar üçüncü taraf rehberler. YouTube'un kendi para kazanma politikası
> sayfası son sözü söyler — karar vermeden önce oradan doğrulanmalı.

---

## Reddedilenler

### Platformlara doğrudan API ile bağlanmak
**Neden olmaz:** YouTube ve TikTok denetimden (audit) geçmemiş uygulamaların
yüklediği videoları gizli yapıyor.

> ⚠️ **YouTube'un gizli kilidi KALICI.** API ile denetimden geçmeden video
> yüklersen o video asla herkese açık yapılamıyor — Studio'dan da olmuyor,
> itiraz da yok. Tek çözüm baştan yüklemek.
> Denetim formu ücretsiz ama **önce** gönderilmeli.

Instagram ayrıca Business/Creator hesap + Facebook sayfası bağlantısı istiyor.

### WoopSocial / Upload-Post gibi aracı servisler
**Şimdilik hayır.** Kod yazıldı (`cm/woop.py`) ama kullanılmıyor.
Bedava planlar: WoopSocial 2 hesap + API, ~5 YouTube postu/gün.
Upload-Post ayda 10 yükleme ve TikTok yok.
**Uyanma şartı:** elle yüklemek gerçekten yavaşlatmaya başlarsa.

### TikTok hesabı
**2026-11-18, ertelendi.** Önce YouTube ve Instagram'da düzenli post atılsın.
TikTok'un zamanlaması sadece masaüstü tarayıcıda ve 10 gün ileriye kadar.

### Web arayüzü
**Yapıldı, kenara kaldırıldı.** `server.py` + `web/` çalışıyor, uçtan uca
test edildi. Ama API anahtarı olmadan klipleri zayıf program seçiyor.
**Uyanma şartı:** Claude olmadan klip çıkarma ihtiyacı + anahtar (~$4-7/ay).

### Clips Kitty (hazır açık kaynak program)
**Kurulmadı.** github.com/ColinGPT9/clips-studio — bedava, Microsoft Store'da,
arayüzü ve 9 platforma paylaşımı var. Bizden üstün yanı: arayüz + paylaşım.
Bizim üstünlüğümüz: **klip seçimi ve ses efektleri.**
Kodunu okuduk, API bilgilerini oradan öğrendik, kod kopyalamadık (AGPL).

### Bu programı satmak
**Rafta.** Pazar kalabalık: OpusClip, Vizard, Klap, Submagic — hepsi $14-29/ay
ve aynı işi yapıyor. Önce içerik üret, kanal büyürse asıl iş o.

---

## Henüz karar verilmedi

- **API anahtarı alınsın mı?** (~$4-7/ay) — arayüzün ve rutinin Claude'suz iyi
  klip seçebilmesi için tek yol
- **YouTube denetim formu gönderilsin mi?** — ileride API ile yüklemek ihtimali
  için, şimdiden göndermek bedava ve bekleme süresini başlatır
