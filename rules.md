# 🎨 Prompt: Halaman Daftar Harga Komisi — Tema "Amai"

> **Tujuan:** Membuat halaman web daftar harga komisi ilustrasi dengan estetika manis & kawaii ("amai" / 甘い).
> **Tone Visual:** Soft, hangat, sweet — kombinasi pastel rose, mauve, krim, dan aksen pink cerah.

---

## 🎨 Palet Warna Tema "Amai"

```css
/* Tema "Amai" — Sweet Pastel Rose & Cream */
--color-amai-bg:         #1a0e14;   /* Background utama: deep plum/maroon gelap */
--color-amai-surface:    #2a1520;   /* Surface card: dark rose-brown */
--color-amai-border:     #4d2535;   /* Border: mauve-maroon */
--color-amai-accent:     #e8638c;   /* Aksen utama: rose pink cerah */
--color-amai-soft:       #f5a8c0;   /* Aksen soft: pastel pink */
--color-amai-cream:      #fde8ef;   /* Text terang: pink cream */
--color-amai-muted:      #b07090;   /* Text muted: dusty mauve */
--color-amai-gold:       #f0c0a0;   /* Highlight harga/badge: peach gold */
--color-amai-success:    #c084a8;   /* Success/add-on: soft lilac */
--color-amai-tag:        #ff8fab;   /* Tag badge: hot pink lembut */
```

---

## 📐 Struktur Halaman

```
┌─────────────────────────────────────────────────────┐
│  🌸 HEADER — Nama/Brand + Tagline                   │
│  "甘い Art — Commission Price List"                 │
├─────────────────────────────────────────────────────┤
│  📋 TABEL HARGA UTAMA                               │
│  Kolom: Paket | Harga IDR | Harga USD               │
├─────────────────────────────────────────────────────┤
│  ⚡ SHORTCUT BUTTONS (Quick Price Reference)        │
│  Klik tombol → menyalin/highlight harga tersebut   │
├─────────────────────────────────────────────────────┤
│  🛠️ ADD-ON / PRINTILAN SECTION                    │
│  Daftar tambahan harga                              │
└─────────────────────────────────────────────────────┘
```

---

## 📋 Data Harga Komisi

### Tabel Utama

| Paket                          | 🇮🇩 IDR       | 🌍 USD              |
|--------------------------------|----------------|---------------------|
| Bust Up                        | Rp 140.000     | $25                 |
| Genshin Avatar Icon            | Rp 100.000     | $30                 |
| Half Body                      | Rp 250.000     | $40                 |
| Full Body                      | Rp 300.000     | $60                 |
| Character Sheet (Simple)       | Mulai Rp 350.000~ | Start from $85~  |
| Genshin Drip Marketing         | Rp 400.000     | $70                 |
| Character Sheet (Overdetailed) | Mulai Rp 700.000~ | Start from $140 / $145 / $150~ |

> **Catatan tilde (~):** Tanda `~` berarti harga bisa naik tergantung detail & kompleksitas karakter.

---

## ⚡ Shortcut Quick-Price Buttons

Buat tombol klik cepat untuk setiap harga. Saat diklik, tombol menampilkan tooltip "Disalin!" / state aktif.
Susun dalam **grid 2 kolom (IDR | USD)**, grouping per paket:

```
[ Bust Up — Rp 140k ]        [ Bust Up — $25 ]
[ Avatar Icon — Rp 100k ]    [ Avatar Icon — $30 ]
[ Half Body — Rp 250k ]      [ Half Body — $40 ]
[ Full Body — Rp 300k ]      [ Full Body — $60 ]
[ CS Simple — Rp 350k~ ]     [ CS Simple — $85~ ]
[ Drip Marketing — Rp 400k ] [ Drip Marketing — $70 ]
[ CS Overdetailed — Rp 700k~ ] [ CS Overdetailed — $140~ ]
                               [ CS Overdetailed — $145~ ]
                               [ CS Overdetailed — $150~ ]
```

> **Penting:** Paket **Character Sheet Overdetailed (USD)** memiliki **3 tombol shortcut terpisah**:
> `$140~` · `$145~` · `$150~` — karena rentang harganya bergantung pada tingkat detail.

---

## 🛠️ Add-on / Printilan (Tambahan Harga)

Tampilkan dalam card/badge section terpisah di bawah tabel utama:

| Tambahan                              | 🇮🇩 IDR                       | 🌍 USD             |
|---------------------------------------|--------------------------------|--------------------|
| 🖼️ Background Art                    | Rp 50.000                      | $10                |
| ⚡ Rush Fee (Priority Express)        | +Rp 10.000 ~ Rp 50.000 (10k, 15k, 20k, 25k, 30k, 35k, 40k, 50k) | +$3 ~ $10 ($3, $4, $5, $6, $7, $8, $9, $10) |
| 🎨 Details Fee (Costume / Complexity) | +Rp 50.000 ~ Rp 200.000 (50k, 100k, 150k, 200k) | +$10 ~ $35 ($10, $18, $25, $35) |
| 💼 Commercial Use                     | +100% harga dasar (2× lipat)   | +100% base price (2×) |
| 👫 Couple Artwork                     | 2× harga dasar                 | 2× base price      |
| 🔄 Revisi Ekstra                      | Mulai +Rp 10.000 / revisi      | Start from +$2 / rev |

---

## 🖥️ Spesifikasi Teknis & Gaya Visual

### Font (Import dari Google Fonts)
- **Heading / Judul:** `Playfair Display` atau `Cormorant Garamond` — serif elegan, feminin
- **Body / Label / Harga:** `DM Sans` atau `Nunito` — rounded, friendly, mudah dibaca

### Background & Surface
- **Background halaman:** Gradient gelap `#1a0e14` → `#0f080f` (deep plum/maroon malam)
- **Card/tabel surface:** `background: rgba(42, 21, 32, 0.7)` + `backdrop-filter: blur(12px)` (glassmorphism)
- **Border:** `1px solid rgba(232, 99, 140, 0.25)` (rose pink transparan)

### Efek & Animasi
- **Hover baris tabel:** `box-shadow: 0 0 16px rgba(232, 99, 140, 0.18)` + background sedikit lebih terang
- **Shortcut Buttons:** Pill shape `border-radius: 9999px`, gradient `#e8638c → #f5a8c0` saat hover
- **Hover card:** Scale `transform: scale(1.02)` + `transition: all 0.25s ease`
- **Dekorasi background:** Blur bubble / bokeh warna pink dan mauve di sudut-sudut halaman (`position: absolute`, `filter: blur(80px)`)
- **Custom scrollbar:** Warna rose/mauve sesuai tema

### Elemen Dekoratif Tambahan
- Emoji aksen di section title: 🌸 🌷 🎀 ✨
- Badge status **"OPEN COM"** / **"CLOSED"** di sudut header (toggle atau static)
- Underline dekoratif di bawah heading menggunakan gradient rose-pink

---

## ✅ Checklist Fitur Halaman

- [ ] Header brand dengan nama artis + tagline manis ("甘い Art" atau nama bebas)
- [ ] Badge status OPEN/CLOSED di header
- [ ] Tabel harga utama, responsif (mobile + desktop)
- [ ] Row hover glow effect (rose pink)
- [ ] Tanda `~` (estimasi) dengan keterangan tooltip/catatan
- [ ] Grid shortcut buttons per paket (IDR & USD kolom terpisah)
- [ ] **3 tombol shortcut USD khusus CS Overdetailed:** `$140~` · `$145~` · `$150~`
- [ ] State "Disalin!" / highlight saat tombol shortcut diklik
- [ ] Section Add-on / Printilan dalam card badge terpisah
- [ ] Warna tema "Amai": deep plum bg, rose-pink accent, cream text, peach-gold harga
- [ ] Font: serif elegan untuk heading, rounded sans untuk body
- [ ] Glassmorphism card dengan blur backdrop
- [ ] Fully responsive (mobile-first)

---

## 🔖 Catatan / Notes Section

Tampilkan di bagian paling bawah halaman:

```
✦ Tanda (~) = harga perkiraan, dapat bertambah sesuai tingkat detail & kompleksitas.
✦ Commercial use = 2× harga dasar.
✦ Rush fee dikenakan apabila deadline kurang dari 3 hari kerja.
✦ Background termasuk dalam add-on terpisah, default tanpa background.
✦ Harga dapat berubah sewaktu-waktu. Konfirmasi harga final via DM.
```

---

*Blueprint ini adalah prompt lengkap untuk membangun halaman web daftar harga komisi.*
*Gunakan sebagai referensi saat memberi instruksi ke AI / developer.*
