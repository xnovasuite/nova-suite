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
- **GA4:** `index.html` içinde `G-XXXXXXXXXX` → kendi ölçüm kimliğinizle değiştirin
- **Meta Pixel:** `000000000000000` → kendi Pixel ID'nizle değiştirin

## Renk paleti
- Turuncu: `#FF6B1A`
- Mavi: `#1E6BFF`
- Açık zemin: `#F7F8FA`
- Yazı: `#0B1220`

© NOVA Software
