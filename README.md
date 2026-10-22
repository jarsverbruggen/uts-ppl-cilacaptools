# UTS PPL – Pengujian Katalog Toolshop with Bugs (Sprint 5)

> **Mata Kuliah:** Praktikum Pengujian Perangkat Lunak  
> **Kelas:** RKS 3 ABC  
> **Nama:** Fajar Syawal Huda (JarsV)  
> **NIM:** *(sesuai data mahasiswa)*  
> **Test Plan:** TP-7: UTS PPL – Katalog Toolshop with Bugs  
> **Test Run:** TR-19: [UTS PPL] Test Run Terpadu – Katalog Toolshop with Bugs (Sprint 5)

---

## Ringkasan Test Run TR-19

| Atribut | Detail |
|---|---|
| **Nama Run** | TR-19: [UTS PPL] Test Run Terpadu – Katalog Toolshop with Bugs (Sprint 5) |
| **Test Plan** | TP-7: UTS PPL – Katalog Toolshop with Bugs |
| **Produk** | Toolshop with Bugs |
| **Versi** | Sprint 5 – Staging |
| **Build** | build-001 |
| **Manager** | JarsV |
| **Default Tester** | JarsV |
| **Mulai** | 22 Oktober 2026, 09.00 WIB |
| **Selesai** | 22 Oktober 2026, 11.30 WIB |
| **Platform Manajemen** | Kiwi TCMS (`https://localhost`) |

---

## Struktur Repositori

```
uts-ppl-cilacaptools/
├── README.md                          ← Dokumen ini
├── evidence-uts/
│   ├── session-notes/
│   │   ├── SESSION-01_Katalog-Navigasi-Filter.md
│   │   └── SESSION-02_Detail-Produk-Keranjang.md
│   └── screenshots/
│       ├── Kiwi TCMS – Setup & Navigasi
│       ├── Test Run TR-19
│       ├── Screenshot AUT (Application Under Test)
│       ├── Evidence PASS per Test Case
│       └── Evidence BUG per Defect
└── Dokumentasi.docx                   ← Dokumentasi lengkap (Word)
```

---

## Sesi Pengujian (Session-Based Test Management)

### SESSION-01 – Eksplorasi Katalog, Navigasi & Filter

**File:** [`evidence-uts/session-notes/SESSION-01_Katalog-Navigasi-Filter.md`](evidence-uts/session-notes/SESSION-01_Katalog-Navigasi-Filter.md)

Pengujian exploratory berbasis charter SBTM pada fitur:
- Navigasi antar halaman katalog
- Filter produk bertingkat (kategori, harga)
- Fungsi search/pencarian
- Pagination

---

### SESSION-02 – Detail Produk & Keranjang Belanja

**File:** [`evidence-uts/session-notes/SESSION-02_Detail-Produk-Keranjang.md`](evidence-uts/session-notes/SESSION-02_Detail-Produk-Keranjang.md)

Pengujian exploratory berbasis charter SBTM pada fitur:
- Halaman detail produk
- Manipulasi kuantitas item
- Keranjang belanja (add, update, remove)
- Transisi ke checkout

---

## Test Cases yang Dieksekusi

| TC ID | Nama | Metode | Status |
|---|---|---|---|
| TC-159 | Login valid – success | Manual | ✅ PASS |
| TC-160 | Login invalid password | Manual | ✅ PASS |
| TC-162 | Login empty validation | Manual | ✅ PASS |
| TC-167 | Search "hammer" – results | Manual | ✅ PASS |
| TC-168 | Search no results | Manual | ✅ PASS |
| TC-171 | Filter kategori hammer | Manual | ✅ PASS |
| TC-172 | Filter price slider | Manual | ✅ PASS |
| TC-174 | Sort nama A-Z | Manual | ✅ PASS |
| TC-175 | Sort harga low-high | Manual | ✅ PASS |
| TC-190 | Navigasi kategori navbar | Manual | ✅ PASS |
| TC-192 | Paginasi halaman 2 | Manual | ✅ PASS |
| TC-195 | Alur produk ke detail | Manual | ✅ PASS |
| TC-196 | [SBTM Charter 1] Exploratory Katalog & Filter | Exploratory | ✅ PASS |
| TC-197 | [SBTM Charter 2] Exploratory Detail Produk & Keranjang | Exploratory | ✅ PASS |
| TC-198 | [Cross-Browser] Kompatibilitas 8 halaman utama | Cross-Browser | ✅ PASS |
| TC-199 | [Responsive – 375x667] Mobile iPhone SE | Responsive | ✅ PASS |
| TC-200 | [Responsive – 390x844 & 412x915] Smartphone Standard | Responsive | ✅ PASS |
| TC-201 | [Responsive – 820x1180] Tablet/iPad | Responsive | ✅ PASS |
| TC-202 | [Responsive – Checkout Flow Mobile] | Responsive | ✅ PASS |
| TC-203 | [Aksesibilitas – Audit Otomatis] Halaman Detail Produk | Accessibility | ✅ PASS |
| TC-204 | [Aksesibilitas – Audit Otomatis] Halaman Form (Login & Contact) | Accessibility | ✅ PASS |
| TC-205 | [Aksesibilitas – Manual Sweep] Navigasi Keyboard | Accessibility | ✅ PASS |

---

## Defect yang Ditemukan (Bug Report)

| Bug ID | Deskripsi | Severity | Screenshot |
|---|---|---|---|
| BUG-001 | Typo pada navbar: "Contakt" → "Contact" | Minor | [`BUG-001_typo-navbar-contakt.jpg`](evidence-uts/screenshots/BUG-001_typo-navbar-contakt.jpg) |
| BUG-002 | Typo label sort: "Reltded" → "Related" | Minor | [`BUG-002_typo-sort-dan-reltded.jpg`](evidence-uts/screenshots/BUG-002_typo-sort-dan-reltded.jpg) |
| BUG-003 | Typo tombol search: "Serch" → "Search" | Minor | [`BUG-003_typo-tombol-serch.jpg`](evidence-uts/screenshots/BUG-003_typo-tombol-serch.jpg) |
| BUG-004 | Typo label contact form: "Massage" → "Message" | Minor | [`BUG-004_typo-label-massage-contact.png`](evidence-uts/screenshots/BUG-004_typo-label-massage-contact.png) |
| BUG-005 | Kuantitas bisa diset 0 di halaman detail produk | Major | [`BUG-005_kuantitas-nol-detail-produk.png`](evidence-uts/screenshots/BUG-005_kuantitas-nol-detail-produk.png) |
| BUG-006 | Produk out-of-stock masih bisa di-add to cart | Critical | [`BUG-006_out-of-stock-bisa-add-to-cart.png`](evidence-uts/screenshots/BUG-006_out-of-stock-bisa-add-to-cart.png) |
| BUG-007 | Double-click tombol cart menyebabkan duplikat item | Major | [`BUG-007_double-click-duplicate-cart.png`](evidence-uts/screenshots/BUG-007_double-click-duplicate-cart.png) |
| BUG-008 | Browser back button menyebabkan inkonsistensi filter | Major | [`BUG-008_browser-back-filter-inconsistency.jpg`](evidence-uts/screenshots/BUG-008_browser-back-filter-inconsistency.jpg) |
| BUG-009 | Aksesibilitas: Kontras warna rendah | Minor | [`BUG-009_accessibility-low-contrast.jpg`](evidence-uts/screenshots/BUG-009_accessibility-low-contrast.jpg) |
| BUG-010 | Aksesibilitas: Form label hilang/tidak deskriptif | Major | [`BUG-010_accessibility-missing-form-labels.jpg`](evidence-uts/screenshots/BUG-010_accessibility-missing-form-labels.jpg) |

---

## Screenshot Evidence

### Kiwi TCMS – Setup & Test Run
| File | Deskripsi |
|---|---|
| [`06b_run19_alt.png`](evidence-uts/screenshots/06b_run19_alt.png) | Halaman TR-19 di Kiwi TCMS |
| [`07_run19_full_top.png`](evidence-uts/screenshots/07_run19_full_top.png) | TR-19 – bagian atas |
| [`08_run19_full_mid.png`](evidence-uts/screenshots/08_run19_full_mid.png) | TR-19 – bagian tengah (attachments) |
| [`09_run19_full_bottom.png`](evidence-uts/screenshots/09_run19_full_bottom.png) | TR-19 – bagian bawah |
| [`04_plan7.png`](evidence-uts/screenshots/04_plan7.png) | TP-7 – Test Plan |

### Application Under Test (AUT)
| File | Deskripsi |
|---|---|
| [`aut_home_page_*.png`](evidence-uts/screenshots/) | Halaman utama Toolshop |
| [`aut_catalog_scrolled_*.png`](evidence-uts/screenshots/) | Katalog produk |
| [`aut_03_katalog_default_*.png`](evidence-uts/screenshots/) | Katalog default |
| [`aut_04_katalog_search_result_*.png`](evidence-uts/screenshots/) | Hasil pencarian |
| [`aut_05_katalog_filter_active_*.png`](evidence-uts/screenshots/) | Filter aktif |
| [`aut_07_detail_produk_*.png`](evidence-uts/screenshots/) | Detail produk |
| [`aut_08_keranjang_*.png`](evidence-uts/screenshots/) | Keranjang belanja |
| [`aut_09_checkout_*.png`](evidence-uts/screenshots/) | Halaman checkout |

---

## Tools yang Digunakan

| Tool | Kegunaan |
|---|---|
| **Kiwi TCMS** | Manajemen test plan, test case, dan test run |
| **Python + Selenium** | Otomasi navigasi dan pengambilan screenshot |
| **axe DevTools / WAVE / Lighthouse** | Audit aksesibilitas otomatis |
| **Chrome DevTools** | Responsive design testing |
| **Browser Stack (simulasi)** | Cross-browser testing |

---

## Lampiran Dokumen

- 📄 [`Dokumentasi.docx`](Dokumentasi.docx) – Dokumentasi lengkap UTS PPL
