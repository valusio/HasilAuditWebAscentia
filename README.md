# Ascentia Website — Web Developer Technical Test

## 1. Overview
Tujuan technical test ini adalah untuk melakukan audit dan perbaikan pada website [https://ascentia.co.id/](https://ascentia.co.id/). Fokus pekerjaan mencakup responsivitas, navigasi, performa, dan identifikasi *bug*.

Berdasarkan inspeksi pada workspace saat ini (`C:\Users\AN515-57\.gemini\antigravity-ide\scratch`), **tidak terdapat source code, konfigurasi, atau struktur project apa pun** yang dapat diaudit atau diperbaiki. Oleh karena itu, pendekatan yang dilakukan adalah melaporkan secara jujur bahwa seluruh implementasi tidak dapat diverifikasi dari workspace.

## 2. Audit Summary

| # | Issue | Severity | Category | Status |
|---|---|---|---|---|
| - | Tidak ada issue yang dapat diverifikasi karena workspace kosong | - | - | Documented |

*(Catatan: Tidak ada issue yang dimasukkan karena tidak ada file atau evidence dalam project yang dapat dianalisis).*

## 3. Issues Found & Fixes

**Tidak ada issue yang ditemukan atau diperbaiki.** 

Tidak terdapat kode sumber di dalam workspace, sehingga tidak ada *root cause* yang dapat ditelusuri maupun perubahan *code* yang bisa dilakukan.

## 4. Technical Approach

- **Observe:** Melakukan inspeksi pada folder workspace (`scratch`).
- **Investigate:** Menggunakan *file system list* dan pencarian (*git status*, *directory listing*).
- **Identify:** Mengidentifikasi bahwa folder project saat ini kosong dan tidak terhubung ke repository source code Ascentia.
- **Fix & Test:** Tidak dilakukan perubahan atau *testing* karena ketiadaan file *source code*.

## 5. Responsive & Cross-Browser Testing

| Area | Desktop | Tablet | Mobile | Status |
|---|---|---|---|---|
| Layout | N/A | N/A | N/A | Tidak dapat diverifikasi |
| Navigation | N/A | N/A | N/A | Tidak dapat diverifikasi |
| Forms | N/A | N/A | N/A | Tidak dapat diverifikasi |
| Images | N/A | N/A | N/A | Tidak dapat diverifikasi |

| Browser | Result | Notes |
|---|---|---|
| Chrome | N/A | Source code tidak tersedia di workspace |
| Safari | N/A | Source code tidak tersedia di workspace |
| Edge | N/A | Source code tidak tersedia di workspace |

*(Catatan: Pengujian tidak dapat dilakukan tanpa keberadaan code base yang berjalan).*

## 6. Performance Considerations

Informasi terkait optimasi *images, JavaScript, CSS, network requests,* dan *page loading* **tidak tersedia** dan **belum dapat diverifikasi** karena ketiadaan akses ke dalam konfigurasi, aset, maupun *source code* dalam workspace ini.

## 7. SEO & Accessibility

Tidak ada temuan yang dapat diverifikasi dari sisi *semantic HTML, meta tag, struktur heading*, atau aksesibilitas, mengingat absennya file komponen dan HTML di dalam workspace.

## 8. Additional Findings

| Finding | Severity | Why It Matters | Fixed? |
|---|---|---|---|
| Workspace Kosong | Critical | Mencegah proses audit, debugging, maupun testing karena tidak ada repository yang tersedia. | No |

## 9. Bonus Improvement

Tidak ada *bonus improvement* yang dilakukan.

## 10. Testing Strategy

*Testing* belum dapat dilakukan. Untuk melakukan *regression testing, route testing*, dan pengujian UI, diperlukan instalasi dan kode sumber *project* di dalam environment lokal ini.

## 11. Recommendations

1. **Inisialisasi Project di Workspace Lokal**
   Harus dilakukan cloning repository (*git clone*) atau penyediaan *source code* secara lengkap ke dalam *environment* untuk memungkinkan *debugging* secara langsung.
2. **Dokumentasi Local Setup**
   Mengingat saat ini tidak terdapat panduan atau konfigurasi *build*, proyek mendatang sebaiknya menyertakan *README* awal yang berisi *prerequisites* dan skrip instalasi yang valid.
3. **Pengaturan Environment Test**
   Sebaiknya terdapat server *staging* atau *local development server* (misal menggunakan Docker atau node server) yang jelas untuk mereplikasi permasalahan di website produksi secara akurat.

## 12. AI Usage Disclosure

**AI Assistance**
- **Tool Used:** Google Gemini / Antigravity
- **Purpose:** Digunakan untuk menginspeksi direktori aktif dan menghasilkan *README.md* yang sepenuhnya didasarkan pada kondisi empiris di workspace.
- **AI-Assisted Areas:** Pemeriksaan direktori, *code investigation* awal, dan penyusunan dokumentasi (*documentation*).
- **Human Validation:** Telah diverifikasi secara manual bahwa workspace berada dalam kondisi kosong sehingga *README* ini disusun dengan kejujuran teknis tanpa adanya asumsi atau pembuatan *issue* fiktif.

## 13. Project Structure

```text
C:\Users\AN515-57\.gemini\antigravity-ide\scratch\
└── README.md
```
*(Direktori saat ini hanya berisi file dokumentasi ini).*

## 14. Local Setup

Karena tidak ada file konfigurasi (`package.json`, `docker-compose.yml`, dsb) di dalam workspace, **tidak ada instruksi lokal** yang dapat diberikan secara spesifik saat ini.

## 15. Final Summary

Tidak ada issue utama yang dapat ditemukan atau diperbaiki pada proses ini karena repositori dan *source code* dari website [https://ascentia.co.id/](https://ascentia.co.id/) tidak tersedia di dalam workspace (`scratch`) saat ini. Pendekatan teknis yang dilakukan difokuskan pada inspeksi empiris *environment*, dan hasil akhirnya adalah dokumentasi mengenai ketidakhadiran komponen yang diperlukan untuk menyelesaikan *technical test*.
