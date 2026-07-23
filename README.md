# NOVA SUITE — Kalite & ERP Pazarlama Sitesi

**IATF 16949 & ISO 9001 uyumlu dijital kalite yönetimi + ERP.** Tek çatı, tek veri, tek platform.

📍 Canlı: <https://xnovasuite.github.io/nova-suite/>

## İçindekiler
- `index.html` — tek dosyalık, bağımlılıksız statik site (Tailwind CDN + Manrope)
- `logo-1.svg`, `logo-2.svg` — NOVA vektörel logoları
- `server.py` — *yerel* önizleme + lead toplama (yayında gerekmez)
- `start.bat` — Windows'ta çift tıkla yerelde aç

## Özellikler
- **NOVA QMS** — IATF 16949 + ISO 9001, AIAG araçları (APQP, PPAP, FMEA, MSA, SPC, 8D, CSR)
- **NOVA ERP** — QMS'e entegre stok, muhasebe, CRM, üretim, İK
- Açık tema, Manrope fontu, aurora arka plan, scroll-reveal animasyonlar
- Lead formu — **Formspree** backend (her leadde e-posta bildirimi)
- **GA4 + Meta Pixel** dönüşüm takibi (CTA + form submit)
- **Open Graph / Twitter Card** — sosyal paylaşımda logo + başlık

## Yerelde çalıştırma
```sh
python server.py        # http://localhost:8003
# veya:
start.bat              # çift tık → tarayıcı açar
```

## Canlıya güncelleme
```sh
git add -A
git commit -m "degisiklik aciklamasi"
git push               # GitHub Pages ~30 sn içinde günceller
```

## Form / e-posta bildirimi
- **Formspree endpoint:** `https://formspree.io/f/mdaqdwlg`
- Bildirim e-postası: Formspree panelinden gelir (kayıtlı mail)

## Takip kodları
**Mevcut durum:** Kodlar yerleşti ama placeholder kimlikle. Veri toplanması için kendi kimliklerinizi alıp değiştirmeniz gerekir.

### GA4 (Google Analytics 4) — ücretsiz
1. https://analytics.google.com → Google hesabıyla giriş
2. Yeni hesap/property oluştur → **Veri akışı** → **Web**
3. Site URL: `https://xnovasuite.github.io/nova-suite/`
4. Size verilen **Ölçüm Kimliği**ni kopyalayın (`G-XXXXXXXXXX` formatında)
5. `index.html` içinde **2 yerde** `G-XXXXXXXXXX` geçiyor — ikisini de gerçek kimlikle değiştirin:
   - `<script async src=...id=G-XXXXXXXXXX>`
   - `gtag('config', 'G-XXXXXXXXXX', ...)`

### Meta Pixel (Facebook/Instagram) — ücretsiz
1. https://business.facebook.com → Etkinlik Yöneticisi → **Veri Kaynağı** → **Pixel**
2. Yeni Pixel oluştur → site URL gir
3. Size verilen **Pixel ID**'yi kopyalayın (15 haneli sayı)
4. `index.html` içinde **2 yerde** `000000000000000` geçiyor — ikisini de değiştirin:
   - `fbq('init', '000000000000000');`
   - `<img ... src="https://www.facebook.com/tr?id=000000000000000&ev=PageView&noscript=1"/>`

> Kimlikleri bana verirseniz, ben de doldurup push edebilirim.

## SEO dosyaları
- `sitemap.xml` — Google'a site haritası
- `robots.txt` — tarayıcı izinleri + sitemap referansı
- Submit: https://search.google.com/search-console → site ekle → sitemap gönder

## Renk paleti
- Turuncu: `#FF6B1A`
- Mavi: `#1E6BFF`
- Açık zemin: `#F7F8FA`
- Yazı: `#0B1220`

© NOVA Software
