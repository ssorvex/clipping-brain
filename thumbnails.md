# Kapak görselleri

Kanalın gridini kanal yapan şey kapaklar. Bu sayfa ChatGPT'ye verilecek
prompt'u tutuyor — her seferinde sıfırdan yazmıyoruz.

## Yön değişikliği — 2026-11-19

Yaser 600K+ izlenen bir GTA kanalının gridini gösterdi. Bizimkiyle farkı tek
kelimeyle: **sadelik.**

| | Bizim eski kapaklar | Hedef |
|---|---|---|
| Yazı | 6-10 kelime, üst üste, 4 renk, kontur + gölge | **2-4 kelime**, küçük, altta, düz beyaz |
| Logo | Köşede, yazının altında kalıyor | **Büyük, ortada, dokunulmamış** |
| Arka plan | Kalabalık AI sahnesi (paraşüt, polis, skyline) | Tek konu veya yumuşak gradyan |
| Kişi | Çizilmiş sahte insanlar | **Yok** |
| Doluluk | Kare tamamen dolu | **Boşluk var** |

Telefonda kapak ~2 cm. O boyutta okunan tek şey logo ve tek bir nesne.
Altı kelimelik kontur yazı o boyutta gri bir lekeye dönüşüyor.

**Değişmeyen kural: GTA VI logosu her kapakta, aynı yerde, bozulmadan.**
Grid'e bakınca "bu kanal" dedirten şey o.

## Üç kalıp

Her klip üçünden birine giriyor.

| Kalıp | Ne zaman | Örnek |
|---|---|---|
| **B — Sahne** ⭐ | Oyun içi bir an anlatılıyor — **çoğu klip** | Klibin gerçek karesi + logo + 2 kelime |
| **A — Nesne** | Bir eşya, silah, araç, menü konuşuluyor | Gradyan üstünde havada duran polis arabası |
| **C — Sayı** | Liste, sayaç, tarih, fiyat | Dev rakam + logo |

B varsayılan: arka plan **üretilmiyor, klipten alınıyor.** A ve C ancak
klipte gösterilecek tek bir kare yoksa.

---

## A — Nesne (gradyan)

```
YouTube Shorts thumbnail, vertical 9:16, 1080x1920.

Background: a smooth studio gradient, deep violet at the top fading to
magenta and a touch of teal at the bottom. Completely clean — no city,
no skyline, no people, no texture.

Centre: the Grand Theft Auto VI logo, large, in the upper third. Crisp
and untouched: the white "GRAND THEFT AUTO" wordmark above a tall
pink-to-orange gradient "VI". Do not restyle or add effects to it.

Subject: [NESNE] floating in the lower-middle, three-quarter view, lit
from above, sharp, with a soft glowing disc of light under it as a
contact shadow. One object only.

Text: the words "[2-4 KELIME]" at the very bottom, bold condensed white
sans-serif, uppercase, small — no taller than 7% of the image. Nothing
else written anywhere.

Style: clean, high contrast, lots of empty space. No outlined word-art,
no multi-colour stacked lettering, no drop shadows on text, no arrows,
no illustrated characters, no watermarks.
```

## B — Sahne (klibin kendi karesi)  ← varsayılan

**Arka planı ChatGPT'ye hayal ettirmiyoruz.** Klibin gerçek karesini
ekliyoruz. Kapak ile video aynı şeyi gösteriyor; izleyici tıkladığında
gördüğü şey kapaktaki şey oluyor. Üretilen sahnede bu olmuyor.

Önce kareleri çıkar (aşağıda), `thumbs.jpg`'den birini seç, o kareyi
ChatGPT'ye **yükle** ve şunu yaz:

```
Use the attached image as the background. Do not redraw it, do not
change the scene — keep it photographic and untouched.

Output: vertical 9:16, 1080x1920. Fill the frame with the attached
image: scale it to cover the width, and extend the top and bottom with
a blurred, slightly darkened copy of itself rather than bars.

Overlay: the Grand Theft Auto VI logo, large, centred in the upper
third. Crisp and untouched — the white "GRAND THEFT AUTO" wordmark
above a tall pink-to-orange gradient "VI". Add a soft dark gradient
behind it so it stays readable.

Text: the words "[2-4 KELIME]" at the very bottom, bold condensed white
sans-serif, uppercase, small — no taller than 7% of the image.

Optional: one thin red arrow pointing at [NE]. Nothing else.

No outlined word-art, no stacked multi-colour lettering, no added
people or objects, no extra text, no watermarks.
```

### Kareleri çıkarma

```powershell
python -m cm.stills "clips\<parti>\<klip klasoru>" --count 6 --band 0.32:0.91
```

Klip klasörüne `thumb-1.jpg` ... `thumb-6.jpg` ve hepsini yan yana
gösteren `thumbs.jpg` düşüyor. `thumbs.jpg`'ye bak, birini seç.

| | |
|---|---|
| **Altyazı** | Kareler `captions.ass`'teki sessizliklerden alınıyor — üstünde yazı olmuyor |
| **Karanlık kare** | Çok koyu ve çok parlak kareler eleniyor |
| **Benzer kare** | Aynı sahneden iki kare gelmiyor, zamana yayılıyor |
| **`--band`** | Üstteki facecam kutusunu ve alttaki bulanık şeridi kesiyor |

`--band` kaynağa göre değişiyor. Önce `--band` olmadan çalıştır,
`thumbs.jpg`'ye bak, facecam nerede bitiyorsa oranı ver. Typical Gamer
için `0.32:0.91`.

## C — Sayı

```
YouTube Shorts thumbnail, vertical 9:16, 1080x1920.

Background: a smooth studio gradient, deep violet to magenta. Clean and
empty.

Centre: one enormous number — "[SAYI]" — in heavy white sans-serif with
a soft gold-to-orange gradient, filling the middle third. It is the
loudest thing in the frame.

Below it: the Grand Theft Auto VI logo, medium size, crisp and
untouched.

Text: the word(s) "[1-3 KELIME]" under the logo, small, uppercase,
white. Nothing else.

Style: flat, clean, huge contrast, lots of empty space. No outlined
word-art, no stacked lettering, no people, no city, no watermarks.
```

---

## Doldurma örnekleri

| Klip | Kalıp | Nesne / sahne | Kelimeler |
|---|---|---|---|
| Uçak çalma + paraşüt | B | `thumb-3.jpg` — uçaktan atlamış, şehir altta | `PLANE THEFT` |
| Polis kıyafetini tarif ediyor | A | a police cruiser's in-car computer screen | `THEY SAW YOU` |
| 62 saat sonra inceleme | C | `62` | `HOURS IN` |
| Hava durumu güncellemesi | B | a thunderstorm rolling over the beach | `WEATHER` |

## Kontrol — göndermeden önce

- [ ] Arka plan **klibin kendi karesi** mi (üretilmiş sahne değil)
- [ ] Logo büyük, net ve **değiştirilmemiş** mi
- [ ] Toplam **4 kelimeden az** yazı var mı
- [ ] Telefon boyutunda (küçült, bak) hâlâ okunuyor mu
- [ ] Çizilmiş insan **yok** mu
- [ ] Kare tamamen dolu **değil** mi

Beşinden biri hayırsa ChatGPT'ye "simplify: fewer words, more empty
space, keep the logo" yaz, yeniden üretsin.

## Neden logo her seferinde

[[posted]] tablosu hangi kapağın tuttuğunu söyleyecek. Ama grid'in
tutarlılığı ayrı bir şey: biri bir videomuzu beğenip profilimize
girdiğinde 9 kapakta aynı logoyu görürse kanal gibi duruyor, rastgele
yüklemeler gibi değil. Örnek kanal tam olarak bunu yapıyor —
618K'lık videodan 52K'lık videoya kadar hepsinde aynı logo, aynı yerde.
