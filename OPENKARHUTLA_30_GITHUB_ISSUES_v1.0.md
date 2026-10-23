# OpenKarhutla — 30 GitHub Issues Awal (Backlog v1.0)

**GitHub namespace rancangan:** https://github.com/open-karhutla  
**Status:** **Belum dibuat di GitHub.** `OKH-001` sampai `OKH-030` adalah **ID backlog dokumen**, bukan issue number GitHub.  
**Dokumen induk:** `OPENKARHUTLA_MASTER_BLUEPRINT_v1.0.md`  
**Strategi:** Global Vision, Indonesia-first Execution

## Pedoman prioritas
- **P0:** prasyarat atau komponen wajib untuk public MVP; selesaikan lebih awal.
- **P1:** penguatan penting, sebagian dapat dituntaskan sebelum GA.
- **P2:** riset/fitur fase lanjut dan harus melalui review keselamatan bila relevan.
- **S/M/L:** ukuran relatif, bukan estimasi hari/jam.
- **Dependencies:** ID backlog di dokumen ini, bukan GitHub #number.
- **Repo:** semuanya hanya usulan nama repository; belum dibuat dari percakapan ini.

## Indeks 30 Issues

| ID | Prioritas | Repo | Ukuran | Judul |
|---|---|---|---|---|
| OKH-001 | P0 | `community` | S | Ratifikasi project charter dan batas keselamatan |
| OKH-002 | P0 | `community` | M | Bentuk model governance dan CODEOWNERS lintas domain |
| OKH-003 | P0 | `community` | M | Tetapkan strategi lisensi kode, dokumentasi, dan data |
| OKH-004 | P0 | `community` | S | Siapkan Code of Conduct dan kanal disclosure privat |
| OKH-005 | P0 | `community` | M | Definisikan baseline organisasi, repo, label, dan template |
| OKH-006 | P0 | `platform` | M | Lakukan threat modeling dan privacy impact review MVP |
| OKH-007 | P0 | `geo-data` | M | Susun skema katalog sumber dan kontrak lisensi |
| OKH-008 | P0 | `geo-data` | M | Tinjau ketentuan NASA FIRMS sebagai sumber pilot pertama |
| OKH-009 | P0 | `platform` | L | Rancang skema PostgreSQL/PostGIS dan migrasi pertama |
| OKH-010 | P0 | `geo-data` | M | Tetapkan standar waktu, geometri, dan kontrak observasi |
| OKH-011 | P0 | `platform` | L | Implementasikan connector ingestion pertama dengan allowlist |
| OKH-012 | P0 | `platform` | L | Bangun ingestion idempotent dan backfill terbatas |
| OKH-013 | P0 | `platform` | L | Terapkan quality gates, quarantine, dan lineage |
| OKH-014 | P0 | `platform` | M | Sediakan ingestion metrics dan indikator freshness |
| OKH-015 | P0 | `platform` | L | Implementasikan API read-only /v1 dan OpenAPI |
| OKH-016 | P0 | `platform` | L | Tambahkan query geospasial, filter temporal, dan pagination |
| OKH-017 | P1 | `geo-data` | M | Siapkan katalog batas administratif Indonesia yang sah |
| OKH-018 | P0 | `platform` | L | Bangun peta observasi Indonesia dengan MapLibre |
| OKH-019 | P0 | `platform` | M | Bangun panel detail observasi dan provenance |
| OKH-020 | P0 | `platform` | M | Bangun banner keterlambatan dan status sumber |
| OKH-021 | P0 | `community` | M | Dokumentasikan metodologi, API, dan keterbatasan sensor |
| OKH-022 | P1 | `platform` | M | Siapkan i18n Bahasa Indonesia dan Inggris |
| OKH-023 | P1 | `platform` | M | Audit WCAG dan fallback tabel pengamatan |
| OKH-024 | P0 | `platform` | M | Konfigurasi secure CI, dependency checks dan release policy |
| OKH-025 | P1 | `platform` | L | Uji performa, backup-restore dan operasional MVP |
| OKH-026 | P2 | `geo-data` | M | Rancang event clustering sebagai riset kandidat kejadian |
| OKH-027 | P1 | `community` | M | Susun SOP dual-review verifikasi dan riwayat status |
| OKH-028 | P1 | `community` | M | Buat contributor onboarding dan 10 tugas pemula |
| OKH-029 | P2 | `platform` | L | Desain prototipe laporan komunitas yang mengutamakan privasi |
| OKH-030 | P0 | `platform` | L | Laksanakan release readiness review untuk Observations Beta |


## Rincian issue siap disalin ke GitHub


### OKH-001 — Ratifikasi project charter dan batas keselamatan

**Title:** `Ratifikasi project charter dan batas keselamatan`  
**Repository:** `open-karhutla/community`  
**Priority:** `P0` · **Size:** `S`  
**Labels:** `type:docs,area:community,needs-safety-review`  
**Dependencies:** —

**Problem / Why it matters**  
Menyelaraskan visi global, pilot Indonesia, dan pembeda antara hotspot dengan kejadian terkonfirmasi.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Charter Indonesia+English menjelaskan misi, ruang lingkup MVP, non-goals, dan pembagian tanggung jawab
- [ ] Teks disclaimer untuk peta dan API disepakati reviewer keselamatan
- [ ] Keputusan dicatat sebagai RFC/ADR publik

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-002 — Bentuk model governance dan CODEOWNERS lintas domain

**Title:** `Bentuk model governance dan CODEOWNERS lintas domain`  
**Repository:** `open-karhutla/community`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:chore,area:community`  
**Dependencies:** 001

**Problem / Why it matters**  
Tanpa tata kelola yang jelas perubahan data/safety bisa digabung tanpa akuntabilitas.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Dokumen peran steward, TSC, maintainer, reviewer sains dan keamanan tersedia
- [ ] Alur RFC/ADR, konflik kepentingan, banding, serta eskalasi ditulis
- [ ] Template CODEOWNERS dan aturan dua reviewer perubahan berisiko diputuskan

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-003 — Tetapkan strategi lisensi kode, dokumentasi, dan data

**Title:** `Tetapkan strategi lisensi kode, dokumentasi, dan data`  
**Repository:** `open-karhutla/community`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:docs,area:data,needs-data-license`  
**Dependencies:** 001

**Problem / Why it matters**  
Keterbukaan kode tidak otomatis memberi izin mendistribusikan dataset pihak ketiga.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Keputusan lisensi kode (usulan Apache-2.0) dan docs (usulan CC BY 4.0) diratifikasi
- [ ] Kebijakan data per-sumber memuat hak redistribusi, atribusi dan retensi
- [ ] Panduan pemeriksaan asal kontribusi / DCO disepakati

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-004 — Siapkan Code of Conduct dan kanal disclosure privat

**Title:** `Siapkan Code of Conduct dan kanal disclosure privat`  
**Repository:** `open-karhutla/community`  
**Priority:** `P0` · **Size:** `S`  
**Labels:** `type:docs,area:community,type:security`  
**Dependencies:** 001,002

**Problem / Why it matters**  
Kontributor membutuhkan aturan perilaku dan mekanisme penanganan laporan sensitif.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Code of Conduct, prosedur moderasi dan banding bilingual dibuat
- [ ] Kanal pelaporan keamanan privat dan target triase terdokumentasi
- [ ] Panduan larangan memasukkan identitas pelapor/secrets ke Issues disertakan

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-005 — Definisikan baseline organisasi, repo, label, dan template

**Title:** `Definisikan baseline organisasi, repo, label, dan template`  
**Repository:** `open-karhutla/community`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:chore,area:community`  
**Dependencies:** 001–004

**Problem / Why it matters**  
Pola kolaborasi harus konsisten sebelum backlog dipublikasikan.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Struktur 3 repo awal beserta tanggung jawab dan kriteria pemisahan disetujui
- [ ] Template Issue/PR, label, milestones, review checklist, branch protection terdokumentasi
- [ ] Tidak ada repository yang dibuat hingga izin eksplisit diberikan

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-006 — Lakukan threat modeling dan privacy impact review MVP

**Title:** `Lakukan threat modeling dan privacy impact review MVP`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:security,needs-safety-review`  
**Dependencies:** 001,002

**Problem / Why it matters**  
Peta, endpoint data, dan penyimpanan bukti berpotensi mengungkap informasi sensitif.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Diagram trust boundary dan matriks risiko disimpan di docs/security
- [ ] Kontrol minimal: least privilege, rate limit, data minimization, secret management, logging
- [ ] Batasan pemrosesan laporan warga ditegaskan sebagai di luar MVP

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-007 — Susun skema katalog sumber dan kontrak lisensi

**Title:** `Susun skema katalog sumber dan kontrak lisensi`  
**Repository:** `open-karhutla/geo-data`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:feature,area:data,needs-data-license`  
**Dependencies:** 003

**Problem / Why it matters**  
Setiap observasi harus terkait sumber yang bisa diaudit.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] JSON Schema untuk provider, sensor, dataset, timestamp, attribution, source terms dan redistribution flag
- [ ] Ada fixture valid dan invalid, serta validator lintas repository
- [ ] Katalog memisahkan metadata sumber publik dan akses credentials privat

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-008 — Tinjau ketentuan NASA FIRMS sebagai sumber pilot pertama

**Title:** `Tinjau ketentuan NASA FIRMS sebagai sumber pilot pertama`  
**Repository:** `open-karhutla/geo-data`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:research,area:data,needs-data-license`  
**Dependencies:** 003,007

**Problem / Why it matters**  
Implementasi konektor bergantung kepada izin API, atribusi, latensi, dan redistribusi.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Dokumen resmi yang berlaku ditautkan bersama tanggal verifikasi
- [ ] Tentukan endpoint/format, syarat akses, area Indonesia, rate limits dan pembatasan cache
- [ ] Keputusan go/no-go untuk dataset pilot ditandatangani data steward

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-009 — Rancang skema PostgreSQL/PostGIS dan migrasi pertama

**Title:** `Rancang skema PostgreSQL/PostGIS dan migrasi pertama`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:feature,area:gis,area:api`  
**Dependencies:** 007

**Problem / Why it matters**  
Penyimpanan spasial dan jejak sumber perlu skema berintegritas.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Migrations untuk sources, ingestion_runs, observations dan quality checks
- [ ] Geometri EPSG:4326, timestamptz UTC, GiST + B-tree index, unik source/external/time
- [ ] Constraint dan pengujian fixture spatial valid/invalid lulus

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-010 — Tetapkan standar waktu, geometri, dan kontrak observasi

**Title:** `Tetapkan standar waktu, geometri, dan kontrak observasi`  
**Repository:** `open-karhutla/geo-data`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:docs,area:gis,area:data`  
**Dependencies:** 007,009

**Problem / Why it matters**  
Kesalahan CRS dan waktu menyebabkan interpretasi hotspot salah.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Spesifikasi UTC, EPSG:4326, validitas lon/lat, datum, null handling, frp unit tersedia
- [ ] Paket fixture antimeridian dan boundary edge case disediakan
- [ ] Perhitungan jarak menegaskan geography atau proyeksi setara meter

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-011 — Implementasikan connector ingestion pertama dengan allowlist

**Title:** `Implementasikan connector ingestion pertama dengan allowlist`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:feature,area:ingestion`  
**Dependencies:** 008–010

**Problem / Why it matters**  
MVP membutuhkan pengambilan data sumber yang sah dan tahan kesalahan.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Connector mengimplementasikan timeout, retry jitter/backoff, rate limit, allowlisted host
- [ ] Parser memetakan data mentah ke kontrak observasi dengan provenance lengkap
- [ ] Tidak ada token di log atau repo; tes mock tanpa jaringan eksternal lulus

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-012 — Bangun ingestion idempotent dan backfill terbatas

**Title:** `Bangun ingestion idempotent dan backfill terbatas`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:feature,area:ingestion`  
**Dependencies:** 009,011

**Problem / Why it matters**  
Retry dan pembaruan sumber tidak boleh menghasilkan double count.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Deterministic dedup key dan upsert transactional berjalan
- [ ] Replay 2x pada rentang identik menghasilkan jumlah observasi unik sama
- [ ] Batas time window dan resource cap untuk backfill diuji

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-013 — Terapkan quality gates, quarantine, dan lineage

**Title:** `Terapkan quality gates, quarantine, dan lineage`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:feature,area:data,area:ingestion`  
**Dependencies:** 010–012

**Problem / Why it matters**  
Data invalid harus ditahan tanpa hilang jejak penyebabnya.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Validasi koordinat/waktu/unit/sensor dan skor kelengkapan sumber berjalan
- [ ] Invalid rows masuk quarantine beserta reason code dan run ID
- [ ] Test menunjukkan data gagal tidak muncul di public API

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-014 — Sediakan ingestion metrics dan indikator freshness

**Title:** `Sediakan ingestion metrics dan indikator freshness`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:feature,area:ingestion`  
**Dependencies:** 011–013

**Problem / Why it matters**  
Data yang sudah usang tidak boleh tampak real time.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Metrics run success/failure, source lag dan oldest/newest observation
- [ ] Endpoint/public status aman memisahkan observed_at, ingested_at, last_checked
- [ ] Stale status aktif berdasarkan threshold terdokumentasi dan diuji

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-015 — Implementasikan API read-only /v1 dan OpenAPI

**Title:** `Implementasikan API read-only /v1 dan OpenAPI`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:feature,area:api`  
**Dependencies:** 009,013

**Problem / Why it matters**  
Pengguna memerlukan kontrak integrasi stabil yang tidak membeberkan data internal.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] GET /v1/sources, /v1/observations/{id}, /v1/data-freshness tersedia
- [ ] DTO whitelist fields, validation, structured errors dengan correlation ID
- [ ] Dokumentasi OpenAPI memiliki contoh respons dan tidak mengekspor kolom internal

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-016 — Tambahkan query geospasial, filter temporal, dan pagination

**Title:** `Tambahkan query geospasial, filter temporal, dan pagination`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:feature,area:api,area:gis`  
**Dependencies:** 015

**Problem / Why it matters**  
Pengambilan observasi harus efisien, aman, dan reproducible.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] GET /v1/observations menerima bbox, from/to, sensor, limit, cursor
- [ ] Input bbox dan interval dibatasi; uji out-of-range serta pagination tanpa duplikat lulus
- [ ] EXPLAIN/benchmark query periode relevan disertakan

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-017 — Siapkan katalog batas administratif Indonesia yang sah

**Title:** `Siapkan katalog batas administratif Indonesia yang sah`  
**Repository:** `open-karhutla/geo-data`  
**Priority:** `P1` · **Size:** `M`  
**Labels:** `type:research,area:gis,needs-data-license`  
**Dependencies:** 003,010

**Problem / Why it matters**  
Filter provinsi/kabupaten perlu referensi wilayah berkode dan berversi.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Sumber resmi/terpercaya beserta lisensi dan attribution dicatat
- [ ] Schema regions memuat level, codes, validity, geometry version
- [ ] Area administratif contoh diuji tanpa membuat klaim batas definitif bila data berbeda

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-018 — Bangun peta observasi Indonesia dengan MapLibre

**Title:** `Bangun peta observasi Indonesia dengan MapLibre`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:feature,area:frontend,area:gis`  
**Dependencies:** 015,016

**Problem / Why it matters**  
Produk pertama harus membuat pengamatan mudah dipahami tanpa overclaim.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Peta dapat menampilkan point observation dari API disertai legenda satelit
- [ ] Filter waktu dan sensor berfungsi, mobile layout dan loading/error state ada
- [ ] Peta tidak menggunakan label “kebakaran pasti” untuk hotspot

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-019 — Bangun panel detail observasi dan provenance

**Title:** `Bangun panel detail observasi dan provenance`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:feature,area:frontend`  
**Dependencies:** 015,018

**Problem / Why it matters**  
Pengguna perlu melihat alasan dan keterbatasan tiap titik.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Klik/keyboard focus observasi menampilkan sensor, source, observed_at, ingested_at, confidence_raw
- [ ] Tautan source/reference dan penjelasan sensor yang relevan ada
- [ ] Jelas terlihat bahwa confidence lintas sensor tidak otomatis setara

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-020 — Bangun banner keterlambatan dan status sumber

**Title:** `Bangun banner keterlambatan dan status sumber`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:feature,area:frontend,needs-safety-review`  
**Dependencies:** 014,018

**Problem / Why it matters**  
Pengguna tidak boleh salah menyangka data yang usang sebagai live.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] UI menampilkan source lag dan label stale/warning yang mudah dibaca
- [ ] Saat ingestion gagal, data terakhir tetap bertanggal dan tidak diberi status live
- [ ] Test state normal, delayed, unavailable dan no observations lulus

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-021 — Dokumentasikan metodologi, API, dan keterbatasan sensor

**Title:** `Dokumentasikan metodologi, API, dan keterbatasan sensor`  
**Repository:** `open-karhutla/community`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:docs,area:community,area:data`  
**Dependencies:** 008,015,019

**Problem / Why it matters**  
Dokumentasi ilmiah harus menjadi bagian dari rilis pertama.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Dokumentasi publik menjelaskan hotspot vs fire event, FRP, coverage, revisit, cloud/smoke limitations
- [ ] API examples dan attribution requirements ditulis
- [ ] Tautan dari setiap observation detail ke metodologi tersedia

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-022 — Siapkan i18n Bahasa Indonesia dan Inggris

**Title:** `Siapkan i18n Bahasa Indonesia dan Inggris`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P1` · **Size:** `M`  
**Labels:** `type:feature,area:frontend,good first issue`  
**Dependencies:** 018

**Problem / Why it matters**  
Misi global membutuhkan antarmuka multilingual dari awal.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Semua string user-facing di UI MVP diekstraksi ke locale files
- [ ] Istilah sumber/sensor tidak diterjemahkan dengan menghilangkan makna
- [ ] Unit test fallback bahasa dan format waktu lokal tersedia

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-023 — Audit WCAG dan fallback tabel pengamatan

**Title:** `Audit WCAG dan fallback tabel pengamatan`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P1` · **Size:** `M`  
**Labels:** `type:feature,area:frontend,good first issue`  
**Dependencies:** 018,019

**Problem / Why it matters**  
Peta visual tidak cukup bagi pengguna keyboard/screen reader.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Akses keyboard ke filter dan detail observasi berfungsi
- [ ] Daftar/tabel alternatif dengan sorting dan deskripsi tersedia
- [ ] Audit aksesibilitas mencatat dan menutup blocker kritis pada alur utama

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-024 — Konfigurasi secure CI, dependency checks dan release policy

**Title:** `Konfigurasi secure CI, dependency checks dan release policy`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `M`  
**Labels:** `type:security,type:chore`  
**Dependencies:** 005,006

**Problem / Why it matters**  
Kolaborasi publik memerlukan checks tanpa deploy otomatis yang tak terkontrol.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] CI menjalankan lint/unit tests/migration validation sesuai path perubahan
- [ ] Dependency/secret scanner dan code review rule aktif dalam rancangan
- [ ] Publish/deploy mensyaratkan approval manusia; konfigurasi non-rahasia saja

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-025 — Uji performa, backup-restore dan operasional MVP

**Title:** `Uji performa, backup-restore dan operasional MVP`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P1` · **Size:** `L`  
**Labels:** `type:chore,area:api,area:gis`  
**Dependencies:** 014–016,018,024

**Problem / Why it matters**  
Platform publik perlu diketahui kapasitas dan kemampuan pemulihannya.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Load scenario dan metrik p95 latency didokumentasikan
- [ ] Satu backup terenkripsi dipulihkan sukses di lingkungan uji
- [ ] Runbook stale source, outage, rollback dan revoked access ditinjau

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-026 — Rancang event clustering sebagai riset kandidat kejadian

**Title:** `Rancang event clustering sebagai riset kandidat kejadian`  
**Repository:** `open-karhutla/geo-data`  
**Priority:** `P2` · **Size:** `M`  
**Labels:** `type:research,area:gis,needs-science-review`  
**Dependencies:** 010,013

**Problem / Why it matters**  
Pengelompokan titik perlu bukti metodologis agar tidak menyesatkan.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] RFC mendefinisikan algorithm version, spatial/time thresholds dan failure modes
- [ ] Fixture non-fire anomaly dan hotspot berulang diuji
- [ ] Output hanya kandidat, tidak mengeluarkan klaim confirmed otomatis

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-027 — Susun SOP dual-review verifikasi dan riwayat status

**Title:** `Susun SOP dual-review verifikasi dan riwayat status`  
**Repository:** `open-karhutla/community`  
**Priority:** `P1` · **Size:** `M`  
**Labels:** `type:docs,needs-science-review,needs-safety-review`  
**Dependencies:** 001,006,021

**Problem / Why it matters**  
Proses koreksi klaim harus akuntabel sebelum laporan komunitas diaktifkan.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] State machine satellite_observed/event_candidate/under_review/community_corroborated/source_officially_reported/rejected disetujui
- [ ] Dual reviewer dengan konflik kepentingan dan audit keputusan ditentukan
- [ ] Alur challenge/correction dan panduan tidak mengungkap identitas pelapor ada

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-028 — Buat contributor onboarding dan 10 tugas pemula

**Title:** `Buat contributor onboarding dan 10 tugas pemula`  
**Repository:** `open-karhutla/community`  
**Priority:** `P1` · **Size:** `M`  
**Labels:** `type:docs,area:community,good first issue`  
**Dependencies:** 004,005,021

**Problem / Why it matters**  
Misi OpenKarhutla membutuhkan akses kontribusi non-programmer.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] CONTRIBUTING Indonesia/Inggris, panduan PR/review dan label taxonomy tersedia
- [ ] 10 kandidat good first issues terdokumentasi sesuai scope dan punya mentor
- [ ] Discussions proposal dan kebijakan anti-spam/anti-doxxing disiapkan

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-029 — Desain prototipe laporan komunitas yang mengutamakan privasi

**Title:** `Desain prototipe laporan komunitas yang mengutamakan privasi`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P2` · **Size:** `L`  
**Labels:** `type:research,area:frontend,needs-safety-review`  
**Dependencies:** 006,027

**Problem / Why it matters**  
Pelaporan warga mungkin bermanfaat, tetapi berisiko mengungkap data sensitif.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Threat model, consent, data minimization dan retention policy disetujui sebelum code produksi
- [ ] Prototype hanya memakai data sintetis, private evidence dan geolocation masking
- [ ] Tidak ada fitur pelaporan publik live hingga pilot berizin disetujui

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


### OKH-030 — Laksanakan release readiness review untuk Observations Beta

**Title:** `Laksanakan release readiness review untuk Observations Beta`  
**Repository:** `open-karhutla/platform`  
**Priority:** `P0` · **Size:** `L`  
**Labels:** `type:chore,needs-safety-review`  
**Dependencies:** 001–025 yang bertanda wajib MVP

**Problem / Why it matters**  
Peluncuran memerlukan gerbang legal, keamanan, data science, dan UX.

**Scope / Deliverables**  
Kembangkan keluaran yang dinyatakan dalam acceptance criteria sesuai ruang lingkup dan batas keselamatan Master Blueprint v1.0.

**Acceptance criteria**
- [ ] Checklist provenance, license, stale status, API, observability dan docs ditandatangani
- [ ] Tidak ada critical security finding, kebocoran pelapor, atau klaim hotspot sebagai confirmed fire
- [ ] Uji rollback/restore dan keputusan go/no-go tercatat; publikasi tetap manual

**Definition of Done**  
Artefak terdokumentasi, acceptance criteria diperiksa, quality/security/privacy review dilakukan sesuai tingkat risiko, dan tidak ada secrets maupun data pelapor dalam PR atau Issue.


## Pemetaan milestone yang disarankan

| Milestone | Issue yang dominan |
|---|---|
| M0 Foundation | 001–006, 024 (baseline) |
| M1 Data Foundation | 007–014 |
| M2 Map/API Alpha | 015–020 |
| M3 Public MVP Beta | 021–025, 028, 030 |
| M4 Verification Pilot | 026, 027, 029 (semua dengan gerbang keselamatan) |

**Catatan dependensi:** beberapa pekerjaan berjalan paralel setelah prasyarat inti. Tidak semua P1/P2 harus selesai sebelum Observations Beta; keputusan akhir ada pada release readiness review.

**Prosedur jika nanti diizinkan mengimplementasikan:** verifikasi izin organisasi terlebih dahulu; ratifikasi lisensi dan governance; buat repository dasar; impor issue satu per satu/batch setelah pengecekan duplikat; gunakan GitHub Project untuk status (Backlog/Ready/In progress/In review/Blocked/Done) dan milestone. Jangan menggunakan ID `OKH-001` sebagai nomor issue GitHub yang dijamin.
