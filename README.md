# Ascentia Website — Web Developer Technical Test

## 1. Overview
Technical test ini dilakukan untuk melakukan audit, identifikasi, dan perbaikan terhadap website Ascentia. Proses pengerjaan difokuskan pada identifikasi masalah yang berdampak terhadap functionality, usability, responsiveness, navigation, content quality, serta aspek teknis website.

Pendekatan dilakukan menggunakan alur Observe → Investigate → Identify → Fix → Test, dengan prinsip *minimal necessary changes*. Namun, setelah dilakukan inspeksi mendalam terhadap kondisi FINAL project (berdasarkan `git status`, `git log`, dan *file system*), **tidak ditemukan *source code* website** di dalam repository/workspace ini. Oleh karena itu, seluruh issue yang ditemukan pada website production didokumentasikan, namun perbaikan (*fix*) tidak dapat dilakukan maupun diverifikasi secara teknis pada *source code*.

## 2. Audit Summary

| # | Issue | Severity | Category | Status |
|---|---|---|---|---|
| 1 | Public development/under-construction page | High | Functionality/UX | Documented |
| 2 | News page incomplete/empty result | High | Functionality/Navigation | Documented |
| 3 | Default WordPress post exposed | High | Content/SEO/CMS | Documented |
| 4 | Contact information inconsistency | Medium | Content/UX | Documented |
| 5 | Product taxonomy inconsistency | Medium | Content/Information Architecture | Documented |
| 6 | Empty product category UX | Medium | UX/Content | Documented |

## 3. Issues Found & Fixes

### Issue 1 — Public development / under-construction page masih dapat diakses
**Severity:** High
**Category:** Functionality / UX / Content / Routing

- **Problem:** Route `/project/home/` dapat diakses secara publik dan menampilkan halaman yang mengindikasikan website/project masih dalam kondisi "under construction", memberikan kesan tidak profesional.
- **How It Was Found:** Observasi manual pada struktur URL *live website*.
- **Root Cause:** Probable root cause: Konfigurasi *routing* atau *production content* yang masih mengekspos halaman yang belum selesai. (Tidak dapat diverifikasi di source code karena tidak ada source code di workspace).
- **Solution:** Tidak ada perbaikan yang dilakukan karena ketiadaan kode sumber.
- **Files Changed:** N/A
- **Testing / Verification:** N/A
- **Status:** Documented

### Issue 2 — Halaman News menghasilkan empty/broken result
**Severity:** High
**Category:** Functionality / Navigation / UX

- **Problem:** Halaman `/news/` dapat diakses namun menampilkan "Tak Ditemukan Hasil", menyebabkan *broken experience* pada navigasi.
- **How It Was Found:** Mengklik menu/link navigasi menuju halaman News di *live website*.
- **Root Cause:** Probable root cause: *Query logic* gagal mengambil data dari CMS, atau tidak ada konten (*content issue*) yang di-*publish* untuk kategori tersebut.
- **Solution:** Tidak ada perbaikan yang dilakukan karena ketiadaan kode sumber.
- **Files Changed:** N/A
- **Testing / Verification:** N/A
- **Status:** Documented

### Issue 3 — Default WordPress post "Halo dunia!" masih dapat diakses secara public
**Severity:** High
**Category:** Content / SEO / CMS

- **Problem:** Post bawaan instalasi WordPress "Halo dunia!" masih *live* di `/halo-dunia/`.
- **How It Was Found:** Observasi struktur sitemap/URL *live website*.
- **Root Cause:** Probable root cause: Kelalaian penghapusan *default content* CMS saat transisi ke *production*.
- **Solution:** Tidak ada perbaikan yang dilakukan karena ketiadaan kode sumber.
- **Files Changed:** N/A
- **Testing / Verification:** N/A
- **Status:** Documented

## 4. Technical Approach

Pendekatan audit mengikuti langkah:
- **Observe:** Melakukan audit awal secara visual dan fungsional terhadap website *production*.
- **Investigate:** Mencoba menelusuri struktur direktori, `git diff`, dan `git log` pada repository `HasilAuditWebAscentia` untuk mencari letak implementasi.
- **Identify:** Mengidentifikasi bahwa repository saat ini **hanya berisi dokumentasi (README.md)** tanpa adanya *codebase* (HTML/PHP/JS/CSS), sehingga *root cause* spesifik tidak dapat ditetapkan.
- **Fix:** Tidak dilakukan perubahan *code* (*minimal-change* diterapkan dengan tidak merekayasa file fiktif).
- **Test:** *Regression test* secara teknis tidak dapat dilakukan.

## 5. Performance Considerations

Audit performa (seperti analisis *image assets, JavaScript, CSS, network requests, page loading*, maupun *unnecessary dependency*) dilakukan murni secara **manual/observational audit** pada website produksi. Karena tidak ada *source code* maupun *build tool* dalam project, optimasi teknis atau pengukuran formal (seperti Lighthouse/PageSpeed) tidak dilakukan dan tidak ada metrik yang dicantumkan.

## 6. SEO & Accessibility

Dokumentasi temuan difokuskan pada observasi awal, seperti adanya *exposed default content* (Issue 3) yang dapat memengaruhi kualitas *indexing* SEO. Tidak ada verifikasi atau perubahan struktural pada *semantic structure, meta tag*, atau *alt text* yang dilakukan karena *source code* tidak tersedia.

## 7. Additional Findings

| Finding | Severity | Why It Matters | Status |
|---|---|---|---|
| Contact information inconsistency | Medium | Berpotensi membingungkan customer karena adanya nomor telepon yang berbeda (header vs footer). Needs business confirmation. | Documented |
| Product taxonomy inconsistency | Medium | Kategori produk berpotensi tidak tepat secara konteks arsitektur informasi. Needs business confirmation. | Documented |
| Empty product category UX | Medium | Kategori kosong membuat UX terkesan incomplete. | Documented |

## 8. Bonus Improvement

Tidak dilakukan *bonus improvement* secara khusus. Pekerjaan difokuskan pada identifikasi permasalahan dengan tingkat prioritas tinggi yang ditemukan selama proses audit. Namun, perbaikan langsung pada *codebase* tidak dapat dilakukan karena *source code* yang diperlukan tidak tersedia untuk diterapkan.

## 9. Testing Strategy

Tidak ada *testing strategy* (seperti *manual UI testing, route testing, regression testing*, dll.) yang dapat dieksekusi secara aktual pada repository ini karena tidak adanya aplikasi/kode sumber untuk diuji.

## 10. Recommendations

1. **Establish production content/release checklist:** 
   Buat standar prosedur peluncuran (SOP) untuk memastikan tidak ada konten instalasi bawaan (seperti *default* WordPress post) atau halaman *under-construction* yang terekspos ke *production*.
2. **Improve content/data governance:** 
   Lakukan peninjauan reguler terhadap *product taxonomy* dan konsistensi informasi kontak untuk meningkatkan kualitas *User Experience* dan kepercayaan (*trust*).
3. **Implement automated QA/regression checks:** 
   Terapkan pengecekan otomatis untuk mendeteksi responsivitas, *broken links*, dan inkonsistensi konten sebelum dipublikasikan.

## 11. AI Usage Disclosure

**AI Assistance**
- **Tool Used:** Google Gemini / Antigravity
- **Purpose:** AI digunakan sebagai *supporting tool* untuk *code investigation, debugging assistance, documentation*, dan *review*.
- **AI-Assisted Areas:** *documentation* (menyusun laporan), dan *review*.
- **Human Validation:** Seluruh perubahan dan kondisi *workspace* ditinjau serta divalidasi secara manual melalui `git log` dan *source code inspection* (yang menghasilkan temuan bahwa direktori tidak memiliki *source code*) sebelum diserahkan/submission.

## 12. Project Structure

Struktur direktori aktual di dalam repository ini:
```text
project/
├── .git/
└── README.md
```

## 13. Local Setup

Tidak terdapat file *environment requirement*, *build scripts*, `package.json`, konfigurasi framework, maupun *source code* di dalam project ini. Oleh karena itu, project ini tidak dapat dijalankan (di-*setup*) secara lokal.

## 14. Final Summary

- **Total issue utama yang ditemukan (dari hasil observasi website live):** 3
- **Issue yang berhasil diperbaiki di codebase:** 0
- **Issue yang hanya didokumentasikan:** 6 (termasuk *additional findings*)
- **Pendekatan teknis:** Melakukan observasi ketat terhadap kondisi *source code* (melalui `git status` dan list direktori) dan bersikap transparan bahwa tidak ada perubahan fiktif yang dibuat karena ketiadaan kode sumber.
- **Hasil Akhir:** Project hanya berisi dokumen `README.md` yang melaporkan temuan, tanpa manipulasi atau penambahan *source code* yang tidak ada dasarnya.
