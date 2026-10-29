
# Sun Rent A Car & Motorcycle — Chiang Mai

Sun Rent'in tanıtım web sitesi. Site sadece bilgi verir: scooter modelleri, günlük fiyatlar, kiralama şartları, galeri ve dükkân bilgileri. Sitede online rezervasyon ve ödeme yoktur. Müşteriler telefon, LINE veya WhatsApp ile iletişime geçer.

## Dosya yapısı

```
index.html   → Sitenin tamamı (HTML + CSS + JS + görseller tek dosyada)
README.md    → Bu dosya
```

Görseller `index.html` içine base64 olarak gömülüdür. Ayrı bir `img/` klasörü gerekmez. Dosya boyutu yaklaşık 2,3 MB.

## Sayfa bölümleri

| Bölüm | ID | İçerik |
|---|---|---|
| Hero | `#top` | Tam ekran Sun Rent banner'ı, üstünde şeffaf menü |
| Scooters & prices | `#scooters` | 11 model, günlük fiyatlar (THB), 3 grup: Maxi, Sport, Classic & city |
| Good to know | `#know` | Pasaport kopyası, depozito, ücretsiz kask, bakım, günlük/aylık kiralama, 7/24 destek |
| Gallery | `#gallery` | Müşteri fotoğrafları |
| Visit the shop | `#visit` | Dükkân görseli, telefon, adres, saatler, LINE, WhatsApp, sosyal medya |
| Map | `#map` | Google Maps haritası ve yol tarifi kartı |

## Güncel fiyat listesi

| Model | Motor | Günlük |
|---|---|---|
| Yamaha XMAX | 300cc | ฿800 |
| Yamaha NMAX | 155cc | ฿600 |
| Yamaha Aerox (beyaz / mavi) | 155cc | ฿400 |
| Honda Click | 160cc | ฿400 |
| Honda Click | 125cc | ฿350 |
| Yamaha Fazzio | 125cc | ฿350 |
| Yamaha Grand Filano Hybrid | 125cc | ฿350 |
| Honda Scoopy i | 125cc | ฿300 |
| Yamaha Fino | 125cc | ฿250 |
| Yamaha Fino moped | 125cc | ฿250 |

## Yayınlama

### GitHub Pages
1. Yeni bir repo oluştur (ör. `sunrent`).
2. `index.html` ve `README.md` dosyalarını reponun ana dizinine yükle.
3. **Settings → Pages → Source:** `Deploy from a branch`, branch: `main`, klasör: `/ (root)` seç ve kaydet.
4. Site 1–2 dakika içinde `https://KULLANICIADI.github.io/sunrent/` adresinde yayına girer.

### Vercel
1. vercel.com → **Add New → Project** → GitHub reposunu seç.
2. Framework: **Other**, build ayarı gerekmez. **Deploy**'a bas.

### Özel alan adı
GitHub Pages'te **Settings → Pages → Custom domain** alanına alan adını yaz. Alan adı sağlayıcısında `CNAME` kaydını `KULLANICIADI.github.io` adresine yönlendir.

## Sık yapılan güncellemeler

`index.html`'i bir metin editöründe (VS Code vb.) aç ve **Ctrl+F** ile ara.

**Fiyat değiştirme:** model adını ara (ör. `Yamaha NMAX`). Aynı satırdaki `<b>฿600</b>` değerini değiştir.

**Telefon numarası:** `063-163-8011`, `0631638011` ve `66631638011` geçen tüm yerleri değiştir. Sonuncusu WhatsApp linkidir (`wa.me/66...`), başına ülke kodu gelir, baştaki 0 atılır.

**Çalışma saatleri:** `08:00–19:00` metnini değiştir. "Open now / Closed now" göstergesi için script içindeki `h>=8&&h<19` kısmını da güncelle.

**Google Maps haritası:** `<iframe src="https://maps.google.com/maps?q=` ile başlayan satırı bul. Google Maps'te dükkân → **Paylaş → Harita yerleştir → HTML'yi kopyala** ile alınan kodun `src="..."` kısmını buraya yapıştır.

**Yeni dükkân eklemek:** `id="map"` bölümünü kopyalayıp altına yapıştır, yeni dükkânın iframe kodunu, adresini ve saatlerini gir. Birden fazla dükkân için sekmeli harita bölümü istenirse geliştirici ile iletişime geç.

**Görsel değiştirmek:** görseller base64 olarak gömülü olduğu için elle değiştirmek zordur. Yeni motor fotoğrafı eklemek için geliştiriciye gönder.

## Teknik notlar

- Saf HTML, CSS ve JavaScript. Framework veya build adımı yok.
- Fontlar Google Fonts'tan yüklenir: Montserrat (başlıklar), Figtree (metin).
- Mobil uyumlu. Ana kırılma noktaları: 1000px, 760px, 720px.
- Scroll animasyonları CSS `animation-timeline` ile yapıldı. Chrome ve Edge'de çalışır. Desteklemeyen tarayıcılarda site animasyonsuz ama eksiksiz görünür. Cihazda "hareketi azalt" ayarı açıksa animasyonlar kapanır.
- Üst menü hero üzerinde şeffaftır. Aşağı kaydırınca buzlu cam görünümüne geçer.
- "Open now" göstergesi ziyaretçinin saatinden bağımsız olarak Chiang Mai saatini (UTC+7) kullanır.

## İletişim bilgileri (sitede kullanılan)

- **Telefon / WhatsApp:** 063-163-8011
- **LINE:** 0631638011
- **Facebook:** Sun Rent A Scooter CM
- **Instagram:** Sun Rent A Motorcycle
- **Adres:** 19/9/1 Thippanate Road, Haiya, Muang Chiang Mai 50100
- **Saatler:** Her gün 08:00–19:00

---

Tasarım ve geliştirme: **ZOA Agency**
