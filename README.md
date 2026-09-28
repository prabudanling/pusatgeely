<div align="center">

```
╭──────────────────────────────────────────────────────────────────╮
│                                                                  │
│      ██████╗ ██╗   ██╗███████╗ █████╗ ████████╗                  │
│      ██╔══██╗██║   ██║██╔════╝██╔══██╗╚══██╔══╝                  │
│      ██████╔╝██║   ██║███████╗███████║   ██║                     │
│      ██╔═══╝ ██║   ██║╚════██║██╔══██║   ██║                     │
│      ██║     ╚██████╔╝███████║██║  ██║   ██║                     │
│      ╚═╝      ╚═════╝ ╚══════╝╚═╝  ╚═╝   ╚═╝                     │
│                                                                  │
│              G  E  E  L  Y                                       │
│                                                                  │
│        Partner Pembelian Geely — Bogor & Jabodetabek             │
│                     pusatgeely.web.id                            │
│                                                                  │
╰──────────────────────────────────────────────────────────────────╯
```

# 🚗 Pusat Geely — Website Konversi & SEO-Ready

**Website produksi untuk layanan konsultan penjualan independen kendaraan Geely.**
Bilingual 🇮🇩/🇬🇧 · Mobile-first · SEO-ready · Conversion-focused · Anti-fabrication data.

![Next.js](https://img.shields.io/badge/Next.js-16-black?logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-6-2D3748?logo=prisma&logoColor=white)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![Status](https://img.shields.io/badge/status-production-brightgreen)

**[🌐 Lihat Website](https://pusatgeely.web.id)** ·
**[💬 Chat WhatsApp](https://wa.me/62816611142)** ·
**[📸 Instagram](https://instagram.com/salesconsultant1972)**

</div>

---

> 🇬🇧 **English TL;DR** — Production single-page website for **Pusat Geely**, an independent Geely car-sales consulting service in Bogor & Jabodetabek, Indonesia. Bilingual (ID/EN), dark/light theme, 4 verified models, interactive financing simulator, lead-capture form → SQLite → WhatsApp deep-link, triple JSON-LD SEO, rate-limited API. Built with Next.js 16 + TypeScript + Tailwind 4 + Prisma. Developed by **PT Digital Bisnis Manajemen ([digiman.id](https://digiman.id))**, hosting & domain support system by **[juraganwebsite.web.id](https://juraganwebsite.web.id)**. Scroll to [English summary](#-english-summary) for details.

---

## 📑 Daftar Isi

- [✨ Fitur Unggulan](#-fitur-unggulan)
- [🧱 Teknologi](#-teknologi)
- [🏗️ Arsitektur](#️-arsitektur)
- [📂 Struktur Proyek](#-struktur-proyek)
- [🔌 API: `/api/leads`](#-api-apileads)
- [🌐 Dwibahasa (ID/EN)](#-dwibahasa-iden)
- [🛡️ Kebijakan Data Anti-Fabrication](#️-kebijakan-data-anti-fabrication)
- [🚀 Mulai Cepat](#-mulai-cepat)
- [🛠️ Skrip](#️-skrip)
- [☁️ Deployment](#️-deployment)
- [🧪 QA — Sudah Diverifikasi](#-qa--sudah-diverifikasi)
- [🔧 Panduan Pemeliharaan](#-panduan-pemeliharaan)
- [🏆 Kredit](#-kredit)
- [⚖️ Legal & Merek Dagang](#️-legal--merek-dagang)
- [📄 Lisensi](#-lisensi)
- [📞 Kontak](#-kontak)

---

## ✨ Fitur Unggulan

| Fitur | Detail |
| --- | --- |
| 🌐 **Dwibahasa ID/EN** | Dictionary typed penuh di `src/lib/i18n.ts`, persist di `localStorage`, `<html lang>` ikut berganti (default **id** untuk SEO). |
| 🌗 **Dark / Light Mode** | Default dark emerald-charcoal premium; light mode "warm paper". Via `next-themes`. |
| 🚗 **4 Model Terverifikasi** | EX5 (BEV), Starray EM-i (PHEV), Coolray (ICE), EX2 (BEV) — harga indikatif + chip spesifikasi + varian. |
| 🎨 **Color Switcher Foto Asli** | Kartu EX5 & EX2 punya pemilih warna interaktif dengan foto unit nyata — EX5: Snowy White / Carbon Black / Frost Grey; EX2: Putih / Krem / Hijau. |
| 💰 **Simulator Kredit Interaktif** | Slider DP 10–50%, tenor 12–72 bulan, bunga flat 3–12% → angsuran dihitung live, hasil terbawa ke WhatsApp. |
| 📋 **Lead Capture End-to-End** | Form test drive → validasi zod → simpan Prisma → tombol "Lanjutkan ke WhatsApp" membawa konteks lead + ref ID. |
| 🧲 **9 Titik Konversi WA** | Deep-link `wa.me` di hero, kartu model, simulator, footer, FAB desktop, sticky bar mobile, dan lainnya. |
| 🛡️ **Anti-Spam** | Honeypot invisible + rate-limit 5 request/menit/IP + normalisasi nomor `08xx` → `628xx`. |
| 🔍 **SEO Teknis Lengkap** | JSON-LD ×3 (AutoDealer + FAQPage + WebSite), `sitemap.xml`, `robots.txt`, manifest PWA, Open Graph, canonical, hreflang. |
| 📱 **Mobile-First** | Sticky bottom bar (Test Drive + WA) di mobile, FAB WhatsApp di desktop, Sheet menu, target sentuh ≥44px. |
| ♿ **Aksesibel** | HTML semantik, ARIA label, `sr-only`, kontras aman, navigasi keyboard. |
| 🧭 **Satu Halaman, Enam Destinasi** | Anchor-based: Beranda → Model → Layanan → Simulasi → Test Drive → FAQ → Wilayah/Kontak. |
| 🖼️ **Aset Visual Asli + Original** | 9 foto unit asli owner + 9 foto dokumentasi serah terima + ilustrasi AI original — total WebP < 1,5 MB, cepat & bebas hak cipta. Badge "Foto Unit Asli" vs "Ilustrasi" jujur di setiap kartu. |

---

## 🧱 Teknologi

| Lapisan | Teknologi |
| --- | --- |
| Framework | **Next.js 16** (App Router, RSC) + **TypeScript 5** |
| UI | **Tailwind CSS 4** + shadcn/ui (New York) + Lucide Icons + Framer Motion |
| State | **Zustand** (intent lead) + React Context (bahasa) + `next-themes` |
| Form | **react-hook-form** + **zod v4** |
| Database | **SQLite** via **Prisma ORM** (`db/custom.db`) |
| Icon Sistem | lucide-react, sonner (toast), vaul (sheet) |

---

## 🏗️ Arsitektur

```
┌──────────────────────────────────────────────────────────────────┐
│                            BROWSER                               │
│                                                                  │
│   site-header ──► site-hero ──► model-section ──► services       │
│        │                                          │              │
│        ▼                                          ▼              │
│   financing-simulator ──► test-drive-form ──► coverage ──► FAQ   │
│        │                        │                                │
│        │ zustand (lead-intent)  │ POST /api/leads                │
│        ▼                        ▼                                │
│   wa.me deep-link          Route Handler (Node)                  │
│   (9 titik konversi)             │                               │
│                                  ▼                               │
│                     zod ─► honeypot ─► rate-limit (5/menit/IP)   │
│                                  │                               │
│                                  ▼                               │
│                          Prisma → SQLite                         │
│                                  │                               │
│                                  ▼                               │
│                    Response { id, waUrl } ──► tombol WhatsApp    │
└──────────────────────────────────────────────────────────────────┘
```

**Prinsip desain:** satu *source of truth* (`src/lib/site.ts`) untuk semua data bisnis & produk; semua komponen hanya membaca dari sana. Ganti harga sekali → seluruh halaman ikut.

---

## 📂 Struktur Proyek

```
src/
├── app/
│   ├── page.tsx              # Halaman utama (satu-satunya route, anchor-based)
│   ├── layout.tsx            # Metadata, JSON-LD ×3, fonts, providers
│   ├── api/leads/route.ts    # POST — validasi, anti-spam, simpan, waUrl
│   ├── sitemap.ts            # /sitemap.xml
│   ├── robots.ts             # /robots.txt
│   ├── manifest.ts           # PWA manifest
│   └── icon.svg              # Favicon heksagon-G original
├── components/
│   ├── site-header.tsx       # Sticky glass nav + BrandMark + toggle bahasa/tema
│   ├── site-hero.tsx         # Full-viewport hero + grid background
│   ├── model-section.tsx     # 4 kartu model + CTA preselect
│   ├── services-section.tsx  # 6 layanan
│   ├── financing-simulator.tsx
│   ├── test-drive-section.tsx
│   ├── coverage-section.tsx  # 10 area Jabodetabek
│   ├── faq-section.tsx
│   ├── cta-band.tsx
│   ├── contact-footer.tsx    # Footer premium + kredit developer/hosting
│   ├── floating-cta.tsx      # FAB desktop + sticky bar mobile
│   └── language-provider.tsx # Konteks ID/EN + persist
├── lib/
│   ├── site.ts               # ⭐ SOURCE OF TRUTH — bisnis, model, harga, area
│   ├── i18n.ts               # Dictionary ID/EN typed
│   ├── faq-data.ts           # 8 FAQ bilingual
│   ├── db.ts                 # Prisma client
│   └── lead-store.ts         # Zustand lead-intent
prisma/schema.prisma           # Model Lead
db/custom.db                   # Database SQLite
public/images/                 # 24 aset WebP (hero, galeri serah terima, foto unit asli)
```

---

## 🔌 API: `/api/leads`

`POST /api/leads` — simpan lead + hasilkan WhatsApp deep-link berkonteks.

**Request**

```jsonc
{
  "name": "Budi Santoso",
  "phone": "081234567890",          // dinormalisasi → 6281234567890
  "model": "GEELY EX5",             // opsional
  "interest": "test-drive",         // test-drive | price | financing | trade-in | general
  "area": "Bogor Kota",             // opsional
  "preferredDate": "2026-10-01",    // opsional
  "message": "Saya mau tanya EX5",  // opsional
  "lang": "id",                     // id | en
  "website": ""                     // 🍯 honeypot — HARUS kosong
}
```

**Response `201`**

```jsonc
{
  "ok": true,
  "id": "clx…",                     // ref ID lead di database
  "waUrl": "https://wa.me/62816611142?text=…"  // deep-link + seluruh konteks lead
}
```

**Error:** `422` validasi gagal (zod) · `429` melebihi 5 request/menit/IP.

```bash
# Uji cepat
curl -X POST http://localhost:3000/api/leads \
  -H "Content-Type: application/json" \
  -d '{"name":"Tes","phone":"081234567890","interest":"general","lang":"id","website":""}'
```

**Skema database (Prisma):**

```prisma
model Lead {
  id            String   @id @default(cuid())
  name          String
  phone         String
  model         String?
  interest      String
  area          String?
  preferredDate String?
  message       String?
  lang          String   @default("id")
  status        String   @default("new")
  createdAt     DateTime @default(now())
}
```

---

## 🌐 Dwibahasa (ID/EN)

- Kamus terpusat & **fully-typed** di `src/lib/i18n.ts` — TSC menjamin ID dan EN selalu punya key yang sama.
- Default SSR: **Indonesia** (prioritas SEO lokal). Pilihan user persist di `localStorage` (`pusat-geely-lang`).
- `<html lang>` disinkronkan otomatis; toggle ada di header (desktop & mobile).
- Menambah bahasa baru: duplikasi objek `ID`, tambahkan tipe `Lang`, tambahkan opsi di `language-provider.tsx`.

---

## 🛡️ Kebijakan Data Anti-Fabrication

> ⭐ **Aturan paling penting proyek ini.**

1. **Harga & spesifikasi** hanya dari riset multi-sumber publik (stamp: **September 2026**) dan **wajib** ditampilkan sebagai *indikatif* + disclaimer.
2. **DILARANG KERAS** menampilkan: klaim dealer resmi, promo fiktif, testimoni fiktif, alamat fiktif, atau pernyataan atas nama PT Geely Mobil Indonesia / Geely Holding.
3. Pusat Geely dinyatakan **konsultan penjualan independen** — proses pembelian/garansi/purna jual via jaringan dealer resmi Geely Indonesia (lihat blok *Legal & Transparansi* di footer).
4. **Sebelum rilis publik**, semua angka wajib diverifikasi ulang ke kanal resmi Geely (geely.co.id / geelyauto.id).
5. **Sebagian besar visual adalah foto unit asli** milik owner (EX5 Snowy White/Carbon Black/Frost Grey, EX2, Coolray) — ditandai badge "Foto Unit Asli". Visual yang masih berupa gambar generatif (Starray) diberi badge "Ilustrasi" — dinyatakan terbuka di footer.

---

## 🚀 Mulai Cepat

```bash
# 1. Install dependensi
bun install

# 2. Siapkan database (SQLite)
bun run db:push

# 3. Jalankan development server
bun run dev            # → http://localhost:3000

# 4. Pastikan kualitas kode
bun run lint
```

> Tidak butuh environment variable — SQLite file-based dan semua data bisnis statis di `src/lib/site.ts`.

---

## 🛠️ Skrip

| Perintah | Fungsi |
| --- | --- |
| `bun run dev` | Development server (port 3000) + log ke `dev.log` |
| `bun run build` | Production build (standalone) |
| `bun run start` | Jalankan hasil production build |
| `bun run lint` | ESLint (aturan Next.js + react-hooks) |
| `bun run db:push` | Dorong `prisma/schema.prisma` ke SQLite |
| `bun run db:generate` | Generate Prisma Client |

---

## ☁️ Deployment

Sistem dukungan **hosting & domain**: [juraganwebsite.web.id](https://juraganwebsite.web.id)

**Opsi A — Node/VPS (disarankan)**

```bash
bun install
bun run db:push
bun run build
bun run start        # PORT mengikuti environment
```
Arahkan domain `pusatgeely.web.id` ke server (A record) dan proxy reverse (Nginx/Caddy) ke port aplikasi.

**Opsi B — Platform (Vercel dsb.)**

1. Push repo → import ke platform.
2. Build command: `bun run build`; output standalone sudah dikonfigurasi.
3. Database: tetap SQLite (volume persist) atau migrasi ke Postgres dengan mengganti `provider` di `prisma/schema.prisma`.

**Opsi C — Shared hosting (cPanel)**: gunakan Node.js App / Passenger pada fitur hosting; deploy folder `.next/standalone` sesuai panduan penyedia.

**Checklist pra-rilis:** ✅ verifikasi ulang harga · ✅ ganti `SITE_URL` bila domain berubah · ✅ uji form + WhatsApp di perangkat asli · ✅ `bun run lint` bersih.

---

## 🧪 QA — Sudah Diverifikasi

- [x] **Browser end-to-end** (desktop 1440 & mobile 390, dark & light, ID & EN) — render, interaksi, data mengalir.
- [x] **Form lead** — submit sukses `201`, tersimpan di DB, nomor `0812…` dinormalisasi `628…`, tombol WhatsApp membawa konteks lengkap + ref ID.
- [x] **Simulator kredit** — matematika bunga flat benar (Coolray → angsuran recompute live), parameter terbawa ke WA.
- [x] **Preselect model** — klik CTA kartu model → form test drive terisi otomatis.
- [x] **Anti-spam** — honeypot tertutup, rate-limit request ke-6 → `429`.
- [x] **SEO** — `/robots.txt`, `/sitemap.xml`, `/manifest.webmanifest` hidup; 3 JSON-LD tervalidasi; OG tags lengkap.
- [x] **Dwibahasa & tema** — toggle persist, `<html lang>` sinkron, tidak ada hydration mismatch.
- [x] **Footer** — sticky (`mt-auto`), blok Legal & Transparansi, kredit developer & hosting.
- [x] **Konsol bersih** — tanpa error runtime; ESLint PASS.

---

## 🔧 Panduan Pemeliharaan

| Kapan | Apa yang diubah | File |
| --- | --- | --- |
| Harga/promo baru | `MODELS[*].priceFrom` + `variants` | `src/lib/site.ts` |
| Spesifikasi baru | `MODELS[*].specs` | `src/lib/site.ts` |
| Perluas area layanan | `AREAS` | `src/lib/site.ts` |
| Ubah jam layanan | `BUSINESS.hours` | `src/lib/site.ts` |
| Tambah FAQ | duplikasi item di kedua bahasa | `src/lib/faq-data.ts` |
| Ubah teks apa pun | dictionary ID & EN bersamaan | `src/lib/i18n.ts` |

> 💡 Satu file (`site.ts`) mengendalikan seluruh data → risiko "harga lama tersisa di halaman lain" = nol.

---

## 🏆 Kredit

<div align="center">

| | |
| --- | --- |
| 🛠️ **Dikembangkan oleh** | **PT Digital Bisnis Manajemen** — [digiman.id](https://digiman.id) |
| 🖥️ **Sistem dukungan hosting & domain** | [juraganwebsite.web.id](https://juraganwebsite.web.id) |

*Dikembangkan & didukung oleh ekosistem digital Indonesia.* 🇮🇩

</div>

---

## ⚖️ Legal & Merek Dagang

Pusat Geely adalah **layanan konsultan penjualan independen**. Website ini **bukan** milik, bukan bagian dari, dan tidak berafiliasi dengan **PT Geely Mobil Indonesia** maupun **Geely Holding**. Nama *Geely* dan seluruh nama model adalah merek dagang milik pemiliknya masing-masing, digunakan semata untuk identifikasi produk. Pembelian, garansi, dan purna jual dijalankan melalui jaringan dealer resmi Geely Indonesia sesuai ketentuan pabrikan.

---

## 📄 Lisensi

© 2026 **Pusat Geely** — Sena Sulaeman. Seluruh hak cipta dilindungi.
Kode, desain, dan konten diserahkan untuk kepentingan pemilik situs `pusatgeely.web.id` dan tidak untuk didistribusikan ulang tanpa izin.

---

## 📞 Kontak

| | |
| --- | --- |
| 👤 **PIC** | Sena Sulaeman — Konsultan Penjualan |
| 💬 **WhatsApp** | [+62 816-6111-42](https://wa.me/62816611142) |
| ✉️ **Email** | [pusatgeely@gmail.com](mailto:pusatgeely@gmail.com) |
| 📸 **Instagram** | [@salesconsultant1972](https://instagram.com/salesconsultant1972) |
| 📍 **Wilayah** | Bogor & Jabodetabek · Setiap hari 08.00–20.00 WIB |

<div align="center">

**Dibangun dengan presisi, integritas data, dan rasa bangga.** 🚗💨

</div>

---

<a id="-english-summary"></a>
## 🇬🇧 English Summary

**Pusat Geely** (pusatgeely.web.id) is a production single-page website for an independent Geely car-sales consulting service covering Bogor and Greater Jakarta (Jabodetabek), Indonesia. It is intentionally bilingual (Indonesian-first for local SEO), dark/light themed, and conversion-focused: 9 WhatsApp deep-link touchpoints, an interactive flat-interest financing simulator, and a lead-capture form that validates (zod), stores (Prisma/SQLite), rate-limits (5/min/IP), and hands the visitor back to WhatsApp with full lead context plus a reference ID. Technical SEO ships with three JSON-LD graphs (AutoDealer, FAQPage, WebSite), sitemap, robots, PWA manifest, and Open Graph tags. A strict **anti-fabrication data policy** governs all displayed prices and specs (multi-source public research, clearly marked indicative, no fake claims, no fake testimonials). Stack: **Next.js 16, TypeScript 5, Tailwind CSS 4, shadcn/ui, Prisma + SQLite, Zustand, react-hook-form**.

**Developed by PT Digital Bisnis Manajemen ([digiman.id](https://digiman.id))** · **Hosting & domain support system by [juraganwebsite.web.id](https://juraganwebsite.web.id)** · Contact: [Sena Sulaeman](https://wa.me/62816611142) · pusatgeely@gmail.com
