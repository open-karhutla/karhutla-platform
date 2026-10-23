# OpenKarhutla — Master Blueprint v1.0

**Strategi:** Global Vision, Indonesia-first Execution  
**Identitas GitHub yang direncanakan:** [github.com/open-karhutla](https://github.com/open-karhutla)  
**Status:** Dokumen rancangan; **belum diimplementasikan**; tidak ada repository/issue yang dibuat dari dokumen ini  
**Tanggal rancangan:** 23 Oktober 2026  
**Bahasa kerja:** Bahasa Indonesia dan Inggris  
**Dokumen pendamping:** `OPENKARHUTLA_30_GITHUB_ISSUES_v1.0.md`

> **Batas keselamatan:** OpenKarhutla menyediakan informasi dan perangkat riset/dukungan keputusan, **bukan sistem komando pemadaman, pengganti peringatan resmi, atau petunjuk untuk memasuki daerah berbahaya**. Penanganan kebakaran tetap dilakukan oleh instansi dan personel berwenang. Kontributor komunitas tidak ditugaskan mendekati titik api.

## 1. Ringkasan eksekutif

OpenKarhutla adalah inisiatif open-source dan open-science yang membangun infrastruktur data spasial, transparansi pengamatan kebakaran hutan/lahan, verifikasi informasi, dan kolaborasi ilmiah. Proyek dirancang untuk melayani dunia pada masa depan, sementara implementasi serta validasi operasional awal difokuskan pada Indonesia. Kegunaan awalnya adalah memungkinkan masyarakat, peneliti, pengembang, dan organisasi melihat **pengamatan hotspot dari sumber terverifikasi**, mengetahui **usia data, asal data, keterbatasan, dan status verifikasi**, lalu memanfaatkan API/dataset dengan ketentuan lisensi yang benar.

### 1.1 Visi
"Teknologi terbuka, data yang dapat ditelusuri, dan kolaborasi global untuk meningkatkan pemahaman, pencegahan, serta mitigasi dampak kebakaran hutan dan lahan."

### 1.2 Misi
1. Mengintegrasikan sumber pengamatan geospasial dan cuaca yang sah, termasuk metadata provenance.
2. Menyediakan peta, API, dan dokumentasi terbuka yang mudah diakses dan diaudit.
3. Mengembangkan alur verifikasi bertingkat tanpa menyamakan *hotspot* dengan kejadian kebakaran terkonfirmasi.
4. Menumbuhkan komunitas pengembang, peneliti, praktisi GIS, penerjemah, dan masyarakat.
5. Meningkatkan interoperabilitas agar hasilnya dapat dipakai kembali di wilayah/negara lain.
6. Melindungi pelapor, masyarakat, dan lokasi sensitif serta menghormati institusi tanggap darurat.

### 1.3 Prinsip wajib
- **Safety-first:** desain tidak memberi kesan alat ini memutuskan tindakan lapangan secara resmi.
- **Evidence before assertion:** setiap status terikat ke sumber, waktu, lisensi, dan metode.
- **Open by design, not indiscriminately open:** kode terbuka; data hanya dipublikasikan jika memiliki dasar izin dan aman.
- **Indonesia-first, global-ready:** terjemahan, zona waktu, sistem koordinat, dan batas administratif tidak dikunci ke satu negara.
- **Human accountability:** informasi berisiko tinggi perlu peninjauan manusia.
- **Accessibility and low bandwidth:** kompatibel ponsel, jaringan terbatas, dan aksesibilitas.
- **Reproducible science:** pemrosesan tercatat, dapat diuji, dan dapat diulang.

## 2. Ruang lingkup dan hasil yang diharapkan

### 2.1 Sasaran pengguna
- **Publik/peneliti:** melihat peta, unduh data yang legal, memahami ketidakpastian.
- **Kontributor GitHub:** membangun perangkat lunak, dokumentasi, QA, validasi, terjemahan.
- **Tim verifikasi terlatih:** meninjau bukti dan menandai kualitas laporan.
- **Mitra institusional:** mengakses data dan ringkasan situasi sebagai masukan tambahan, bukan sumber komando tunggal.
- **Admin platform:** menjaga keselamatan, privasi, tata kelola, dan integritas sistem.

### 2.2 Produk MVP (Indonesia)
1. Peta Indonesia berbasis MapLibre yang menampilkan observasi hotspot terbaru dari satu penyedia yang izinnya tervalidasi.
2. Filter waktu, satelit/sensor, confidence, wilayah administratif, dan sumber.
3. Halaman detail setiap observasi: lokasi umum, waktu UTC/lokal, sensor, tingkat keyakinan, FRP bila tersedia, sumber, batasan interpretasi, dan tautan sumber asal.
4. Ingestion terjadwal yang idempotent; metrik freshness dan kegagalan.
5. API publik read-only, dengan pagination, geofilter, rate limit, dokumentasi OpenAPI.
6. Dashboard data quality dan pipeline health.
7. GitHub open-source foundation, kontribusi berjenjang dan dokumentasi Indonesia/Inggris.

### 2.3 Setelah MVP, bukan syarat rilis pertama
- Moderasi/verifikasi laporan komunitas dan bukti multimedia yang aman.
- Penggabungan observasi menjadi kandidat peristiwa; catatan keputusan reviewer.
- Korelasi cuaca dan indikator risiko dengan penjelasan batas ketidakpastian.
- Layanan ekspor agregat, panel penelitian, benchmark model ML.
- Portal organisasi mitra dan notifikasi berizin **setelah** persetujuan keselamatan, hukum, dan sumber resmi.
- Android/iOS dengan mode jaringan terbatas; ekspansi negara lain.

### 2.4 Secara eksplisit di luar cakupan awal
- Dispatch petugas, rute memasuki area berbahaya, komando operasional lapangan, prediksi evakuasi mandiri, atau klaim peringatan resmi.
- Publikasi koordinat pelapor ataupun data identitas yang bisa mengekspos orang.
- Model AI yang otomatis mengubah pengamatan menjadi "kebakaran terkonfirmasi".
- Pengambilan atau republishing data yang tidak diizinkan oleh penyedia.

## 3. Identitas dan struktur GitHub Organization

**Namespace rancangan:** `open-karhutla`. Alamat yang diberikan pengguna adalah halaman profil `https://github.com/open-karhutla`, **bukan sebuah repository individual**. Akses konektor saat penyusunan belum menunjukkan repository organisasi; tidak ada klaim bahwa nama repo berikut telah tersedia/dibuat.

### 3.1 Repos awal: kecil, jelas kepemilikannya
| Urutan | Repository (rencana) | Tanggung jawab | Sifat |
|---|---|---|---|
| 1 | `open-karhutla/platform` | Monorepo frontend, API, ingestion awal, infra lokal, tes | Public, jika disetujui |
| 2 | `open-karhutla/community` | Profil organisasi, governance, roadmap, code of conduct, dokumen RFC | Public |
| 3 | `open-karhutla/geo-data` | Spesifikasi data, catalog, contoh sintetis, validasi skema | Public, tanpa data terbatas |

### 3.2 Repo tahap pertumbuhan (jangan buru-buru dipecah)
`wildfire-ai`, `satellite-pipeline`, `mobile`, `documentation`, `research-benchmarks`, `integrations`. Pemecahan dilakukan berdasarkan maintainer independen, stabilitas antarmuka, kebutuhan rilis, dan beban CI—bukan sekadar tampilan organisasi.

### 3.3 Struktur `platform` yang direkomendasikan
```text
platform/
├── apps/
│   ├── web/                 # Next.js, MapLibre, aksesibilitas
│   └── api/                 # NestJS, OpenAPI, auth/admin
├── services/
│   └── ingest/              # Python, konektor data geospasial
├── packages/
│   ├── contracts/           # Zod / OpenAPI shared models
│   ├── ui/                  # Design system
│   └── geo-core/            # Fungsi pemetaan, uji geospasial
├── db/
│   ├── migrations/          # PostgreSQL/PostGIS
│   └── seed/                # Data sintetis, bukan laporan real
├── infra/
│   ├── local/               # Docker Compose
│   └── deployment/          # Contoh konfigurasi non-rahasia
├── docs/
│   ├── architecture/
│   ├── adr/
│   ├── api/
│   └── safety/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── workflows/          # CI secukupnya, bukan deploy otomatis
├── LICENSE
├── README.md
├── CONTRIBUTING.md
├── SECURITY.md
└── CODE_OF_CONDUCT.md
```

### 3.4 Standar lintas repo
- Default branch `main`, protected; perubahan via Pull Request.
- CODEOWNERS per domain (`/db/`, `/services/ingest/`, `/docs/safety/`).
- Dua reviewer untuk perubahan *safety-critical*, akses data pribadi, perizinan dan status verifikasi; minimal satu reviewer untuk perubahan biasa.
- Required checks yang relevan: lint, unit test, schema/migration test, secret scanning, dependency audit; kode yang belum aman tidak auto-deploy.
- Semantic versioning; ADR untuk keputusan arsitektur; RFC untuk perubahan API/kebijakan publik.
- Jangan menyimpan API key, private dataset, secrets, atau bahan identitas pelapor dalam Git.

## 4. Tata kelola open-source dan pengambilan keputusan

### 4.1 Struktur keputusan
| Peran | Tugas | Hak keputusan |
|---|---|---|
| Project Stewards (2–3) | Menjaga misi, kontinuitas, konflik kepentingan | Persetujuan strategi dan charter |
| Technical Steering Committee (3–5) | Standar teknis, arsitektur, ADR, rilis | Persetujuan RFC teknis utama |
| Maintainers per domain | Review dan pemeliharaan repo | Merge sesuai CODEOWNERS |
| Science & Data Advisory Group | Kualitas data, metodologi, ketidakpastian | Rekomendasi ilmiah dan veto etik atas klaim yang tidak sah melalui prosedur review |
| Safety, Privacy & Security Leads | Risk review, disclosure, moderasi | Menahan publikasi fitur berisiko hingga mitigasi terpenuhi |
| Community Moderators | Code of conduct, diskusi, mentoring | Moderasi berbasis kebijakan dan proses banding |
| Contributors | Perbaikan fitur/dokumentasi/riset | Mengusulkan RFC, issue, PR |

**Peringatan konsentrasi kewenangan:** penetapan awal dapat dilakukan oleh pendiri; evaluasi ulang tiap enam bulan dengan catatan keputusan publik. Admin GitHub organisasi tidak otomatis menjadi penilai ilmiah.

### 4.2 Jalur keputusan
- **RFC biasa:** publik 7 hari untuk umpan balik, dua reviewer lintas fungsi.
- **RFC data sensitif/keamanan/keselamatan:** wajib kajian privasi dan *threat modeling*; rilis ditunda sampai disetujui.
- **ADR:** rekam konteks, opsi, trade-off, konsekuensi, dan status (proposed/accepted/superseded).
- **Sengketa:** diskusi → maintainer → TSC → steward, dengan dokumentasi dan jalur banding.
- **Konflik kepentingan:** wajib diungkap untuk vendor data, pendanaan, dan model penilaian.

### 4.3 Lisensi dan kepatuhan
- **Kode:** usulan Apache License 2.0; putuskan dan ratifikasi sebelum kontributor eksternal masuk.
- **Dokumentasi orisinal:** usulan CC BY 4.0.
- **Data:** *tidak* menggunakan satu lisensi universal; katalog masing-masing sumber mencatat lisensi, izin redistribusi, kebutuhan atribusi, masa simpan, dan batas komersial/riset.
- **Model AI:** lisensi weights/model card ditetapkan per artefak; dataset training tidak otomatis terbuka.
- **Kontribusi:** gunakan Developer Certificate of Origin (DCO) atau kebijakan kontribusi ringan, dengan audit asal-usul kode/data; CLA hanya bila alasan hukum jelas.
- **Hukum:** lakukan penelaahan terpisah atas perlindungan data pribadi Indonesia, regulasi data geospasial, hak cipta, dan ketentuan penyedia satelit sebelum peluncuran publik. Dokumen ini bukan pendapat hukum.

## 5. Arsitektur sistem

### 5.1 Prinsip arsitektur
Mulai modular monolith API + ingestion worker terpisah, satu PostgreSQL/PostGIS, object storage opsional, dan cache Redis jika beban telah terukur. Hindari Kafka, Kubernetes, dan microservices penuh pada MVP. Pisahkan trust boundary data publik, bukti privat, admin, dan ingest.

```text
[NASA FIRMS / cuaca / geodata berizin / data institusi]
                       |
                       v
           [Connector + source registry]
                       |
                       v
        [Validation, normalization, provenance]
                       |
              [Queue / scheduled jobs]
                       |
                       v
        [PostgreSQL + PostGIS + audit tables]
             |                  |
       [Public views]     [Restricted evidence]
             |                  |
             v                  v
       [Read-only API]     [Reviewer dashboard]
             |
        [CDN / map tile cache]
             |
             v
      [Web Map + Docs + Public API Clients]
```

### 5.2 Stack referensi (versi dikunci saat implementation kickoff)
| Layer | Usulan | Alasan |
|---|---|---|
| Web | Next.js + React + TypeScript | UI lintas bahasa dan komponen stabil |
| Maps | MapLibre GL JS + OpenMapTiles/PMTiles berlisensi tepat | Bebas vendor lock-in, rendering cepat |
| API | NestJS + TypeScript + OpenAPI | DTO, validation, rate limit, RBAC |
| Ingestion | Python + Pydantic + GeoPandas/pyproj bila diperlukan | Ekosistem sains dan GIS |
| Database | PostgreSQL + PostGIS | Query spasial dan indeks GiST |
| Queue | PostgreSQL jobs untuk prototipe, atau Redis + BullMQ jika perlu | Retry/backoff dan idempotensi |
| Object storage | S3-compatible (private bucket untuk evidence) | Bukti dan artefak terpisah |
| Observability | OpenTelemetry + metrics/logs/traces | Transparansi pipeline |
| Mobile (fase berikut) | React Native + Expo | Konvergensi tipe dan pola web |
| Model AI (riset) | Python + PyTorch/scikit-learn + MLflow setara | Benchmark dan audit metodologi |

Jangan mengunci nomor versi komponen tanpa verifikasi pada hari implementasi; gunakan rilis stabil yang masih didukung dan catat SBOM.

### 5.3 Aliran dan batas kepercayaan
- **Connector:** hanya endpoint allowlisted; selalu simpan atribusi, tanggal pengambilan, checksum, versi parser.
- **Staging:** simpan snapshot asli hanya jika lisensi membolehkan; jika tidak, simpan metadata provenance dan referensi.
- **Validation:** cek CRS, koordinat, waktu, nilai fisik, duplikasi, null, skema, dan metadata sumber.
- **Observations:** *immutable raw evidence* direferensikan; pembaruan berupa rekaman kualitas/revisi, bukan edit asal diam-diam.
- **Events:** kandidat kejadian hasil pengelompokan observasi; tidak identik dengan observasi individual.
- **Publish:** data publik hanya melalui view yang menyembunyikan evidence privat/lokasi sensitif.
- **Review:** approval dan audit terpisah dari proses ingest.

## 6. Rancangan basis data geospasial

### 6.1 Standar data
- Koordinat masukan/pertukaran **EPSG:4326** (WGS84), gunakan `geometry(Point,4326)` + indeks GiST.
- Pengukuran jarak dalam meter: gunakan `geography` atau proyeksi yang sesuai, **jangan** menghitung meter pada degree.
- Semua timestamp disimpan `timestamptz` UTC, lalu dikonversi saat ditampilkan sesuai zona waktu wilayah.
- Gunakan UUID primary key, enum/status terkontrol, foreign key, `created_at`/`updated_at` (di tempat yang sesuai), dan unique constraint sumber.
- Poligon administratif memiliki `valid_from`, `valid_to`, `source`, `license_id`, `geometry_version`; wilayah bisa berubah seiring waktu.
- SRID dan validitas geometri wajib diuji, termasuk antimeridian bila ekspansi global.

### 6.2 Entitas prioritas
| Entitas | Kolom/konsep utama | Akses |
|---|---|---|
| `data_sources` | provider, dataset, sensor, URL referensi, attribution, license policy, SLA, redistribution rule | Public metadata |
| `ingestion_runs` | source_id, fetched_at, window, parser_version, checksum, row counts, status, error | Internal metadata + agregat publik |
| `satellite_observations` | uuid, source_id, external_key, observed_at, point geometry, frp, confidence_raw, confidence_normalized, brightness, scan/track, daynight, raw_reference | Public subset |
| `observation_quality` | observation_id, checks, result, uncertainty, validation_version | Public summary |
| `administrative_regions` | iso3166, level, codes, names, geom MultiPolygon, validity range | Public if licensed |
| `candidate_events` | first_seen, last_seen, extent, status, evidence_count, confidence rationale, last_review | Public curated subset |
| `event_observations` | event_id, observation_id, algorithm_id/version | Public relationships |
| `event_status_history` | event_id, from/to status, actor, evidence, timestamp | Public sanitized |
| `community_reports` | approximate public geometry, restricted exact geometry, privacy flag, content, state | **Restricted** by default |
| `report_evidence` | report_id, storage_key, mime, hash, consent, retention | **Private** |
| `verification_reviews` | reviewer, object, decision, rationale, source refs, conflicts, reviewed_at | Restricted/public summary |
| `risk_indicators` | region/time, index, model_version, input_sources, calibration, uncertainty | Public with caveats |
| `subscriptions` | opt-in, geography rounded, delivery preferences | Private |
| `api_clients` | key hash, permissions, quotas, status | Private |
| `audit_logs` | actor, action, object, timestamp, request-id, immutable event | Restricted |
| `retention_policies` | resource type, legal basis, retention period, destruction rule, legal hold | Internal governance |

### 6.3 Relasi konseptual
```text
data_sources 1──* ingestion_runs
     │
     └──* satellite_observations 1──1 observation_quality
                  │
                  *
             event_observations
                  *
                  │
           candidate_events 1──* event_status_history
                  │
                  └──* verification_reviews
community_reports 1──* report_evidence
community_reports 1──* verification_reviews
administrative_regions ── spatial containment ── observations/events
```

### 6.4 Constraint, indeks, dan partisi
- Unik `(source_id, external_key, observed_at)` dengan normalisasi identitas provider; gunakan fallback hash deterministik bila external key tidak tersedia.
- B-tree `(observed_at DESC, source_id)`; GiST `location_geom`; kombinasi query waktu + bbox untuk API.
- Partisi observasi bulanan **bila** jumlah data dan EXPLAIN ANALYZE membuktikan manfaat; retensi sesuai lisensi sumber.
- Gunakan staging table untuk ingest batch, transaksi upsert, quarantine untuk data invalid, idempotency key untuk retry.
- Buat public-facing database view yang whitelist kolom; hindari `SELECT *` dari entitas private.
- Backup encrypted + uji restore, replikasi/read replica hanya saat beban nyata memerlukannya.

### 6.5 Contoh DDL konseptual (belum production-ready)
```sql
CREATE EXTENSION IF NOT EXISTS postgis;
CREATE TABLE data_sources (
  id uuid PRIMARY KEY,
  code text UNIQUE NOT NULL,
  provider text NOT NULL,
  dataset text NOT NULL,
  attribution text NOT NULL,
  redistribution_allowed boolean NOT NULL DEFAULT false,
  license_reference text,
  created_at timestamptz NOT NULL DEFAULT now()
);
CREATE TABLE satellite_observations (
  id uuid PRIMARY KEY,
  source_id uuid NOT NULL REFERENCES data_sources(id),
  external_key text NOT NULL,
  observed_at timestamptz NOT NULL,
  ingested_at timestamptz NOT NULL DEFAULT now(),
  location_geom geometry(Point,4326) NOT NULL,
  frp_mw numeric,
  confidence_raw text,
  confidence_normalized numeric CHECK (confidence_normalized BETWEEN 0 AND 1),
  raw_reference text,
  UNIQUE (source_id, external_key, observed_at),
  CHECK (ST_IsValid(location_geom))
);
CREATE INDEX satellite_observations_geom_gix
  ON satellite_observations USING GIST (location_geom);
CREATE INDEX satellite_observations_time_idx
  ON satellite_observations (observed_at DESC, source_id);
```
Catatan: normalisasi confidence antar-sensor **tidak otomatis setara**; versi transformasi dan metodologi harus ditampilkan. Perancangan produksi perlu migrasi, hak akses DB, rekonsiliasi zona batas, kebijakan partisi/backup, dan pengujian spasial lebih lanjut.

## 7. Katalog sumber data dan aturan integrasi

| Sumber kandidat | Penggunaan | Prasyarat/keterbatasan |
|---|---|---|
| NASA FIRMS (VIIRS/MODIS) | Deteksi anomali termal/hotspot | Periksa akses API, atribusi, cakupan, resolusi, latensi, lisensi dan kebijakan redistribusi yang berlaku; hotspot bukan kebakaran terkonfirmasi |
| BMKG / sumber cuaca resmi berizin | Kondisi cuaca dan variabel risiko di Indonesia | Verifikasi API, hak pakai, refresh, atribusi; bukan otomatis indikator lokasi kebakaran |
| Copernicus/ESA Sentinel | Analisis citra dan dampak di fase riset | Cloud cover, revisit, resolusi, biaya pemrosesan, ketentuan lisensi |
| Peta administrasi BIG/instansi berwenang | Batas provinsi/kabupaten/kecamatan | Audit status keterbukaan, kualitas geometri, kode wilayah, versi batas |
| OpenStreetMap | Referensi kartografis dan POI berizin | Atribusi ODbL dan kewajiban terkait; hindari mengekspos objek sensitif |
| Sumber institusional lain (termasuk sistem nasional terkait karhutla) | Korelasi dan verifikasi | Tidak mengasumsikan tersedianya API/izin; integrasi hanya dengan perjanjian/ketentuan sah |

### 7.1 Katalog sumber wajib mencatat
`provider`, `dataset_version`, `endpoint_reference`, `sensor/platform`, `collection_interval`, `typical_latency`, `terms_checked_at`, `allowed_uses`, `redistribution_allowed`, `attribution_text`, `retention_rule`, `contact`, `quality_notes`, `fallback`, `deprecated_at`.

### 7.2 Aturan ilmiah
- Hotspot adalah *pengamatan anomali panas*, dapat mencerminkan fenomena lain; tidak boleh otomatis diklaim sebagai lokasi api aktif.
- Confidence berasal dari metodologi sensor; tidak serta-merta merupakan peluang kebakaran yang dapat dibandingkan lintas sensor.
- Data mungkin terlambat, tertutup awan/asap, atau absen akibat waktu lewat satelit. Tampilkan *observed at*, *ingested at*, *last checked*, dan freshness.
- Jangan menyamakan *tidak ada hotspot* dengan *tidak ada kebakaran*.
- Hindari pengukuran luas kebakaran dari jumlah titik hotspot semata.

## 8. Alur ingestion, kualitas, dan API

### 8.1 Alur ingestion
1. Scheduler menandai jendela waktu dan source_id.
2. Connector memanggil endpoint allowlist dengan timeout dan rate limit.
3. Simpan metadata request, checksum, waktu, dan kondisi lisensi; raw payload hanya jika legal.
4. Validasi skema, angka, koordinat, timestamp, duplikat, dan provenance.
5. Quarantine data yang gagal, beserta alasan non-rahasia.
6. Upsert berdasarkan kunci idempotent dalam transaksi.
7. Perbarui agregat/tiles/cache setelah commit.
8. Publikasikan status freshness, error rate, dan source lag ke dashboard kesehatan.

### 8.2 API read-only v1 (rancangan)
- `GET /v1/sources`
- `GET /v1/observations?bbox=...&from=...&to=...&sensor=...&limit=...&cursor=...`
- `GET /v1/observations/{id}`
- `GET /v1/regions?country=ID&level=province`
- `GET /v1/regions/{id}/summary?from=...&to=...`
- `GET /v1/data-freshness`
- `GET /v1/methodology`
- `GET /v1/health/public` (tanpa rahasia/infra detail)

Aturan: limit bbox dan rentang waktu; pagination cursor; response typed; ETag/cache-control; API versioning; rate limit IP/client dengan pengecualian yang adil untuk mitra; no bulk dump jika lisensi sumber melarang; ekspor agregat melalui job terpisah. Error mengandung correlation ID tetapi tidak memuat token/data pribadi.

### 8.3 Kriteria performa awal (target, bukan klaim)
- API list *p95* < 800 ms pada beban uji yang didefinisikan.
- Peta awal yang berisi indikator data tampil < 4 detik pada profil koneksi sedang yang didokumentasikan.
- Pekerjaan ingestion yang berhasil diproses ke basis data ≤ 15 menit setelah **data diterima**, bukan 15 menit setelah kebakaran terjadi.
- SLA observability: setiap keterlambatan sumber melewati batas yang ditetapkan menghasilkan flag *stale data* yang terlihat.
- Kualitas: 100% observasi publik memiliki source_id dan observed_at; 0 catatan lintas hak akses dalam uji keamanan.

## 9. Protokol verifikasi dan klasifikasi

### 9.1 Taksonomi status (jangan disalahartikan sebagai status resmi)
| Status | Makna | Penanggung jawab |
|---|---|---|
| `satellite_observed` | Anomali panas yang tercatat oleh sumber satelit | Data pipeline |
| `event_candidate` | Observasi terkait dikelompokkan menjadi kandidat peristiwa | Algoritme, bukan konfirmasi |
| `under_review` | Bukti sedang dikaji oleh reviewer | Reviewer |
| `community_corroborated` | Bukti independen selaras menurut SOP | Dua reviewer, bukan otoritas resmi |
| `source_officially_reported` | Ada pernyataan dari sumber resmi yang dicatat tautan/waktunya | Reviewer + referensi resmi |
| `disputed` | Bukti saling bertentangan | Reviewer |
| `rejected` | Data tidak memenuhi kriteria atau salah asosiasi | Reviewer dengan alasan |
| `archived` | Siklus ditutup dengan rekam jejak | Sistem/Reviewer |

### 9.2 Aturan perubahan status
- Satelit masuk `satellite_observed` secara otomatis, bukan `confirmed`.
- Gabungan spasial-temporal hanya membentuk `event_candidate`, dengan versi algoritme dan ambang yang terdokumentasi.
- Laporan komunitas mulai sebagai `pending_moderation`; tidak boleh langsung tampil publik.
- `community_corroborated` memerlukan minimal dua reviewer independen dan sumber bukti yang memadai; konflik kepentingan disaring.
- `source_officially_reported` hanya dari sumber pemerintah/organisasi berwenang yang terdokumentasi, bukan kesimpulan AI.
- Seluruh keputusan memiliki reviewer pseudonymous ID, waktu, alasan, referensi, versioning, dan jalur koreksi/banding.
- Jangan menerbitkan bukti yang memuat wajah, nomor telepon, lokasi rumah/pelapor, atau detail lokasi sensitif.

### 9.3 Prosedur penanganan informasi salah
Quarantine → analisis pola spoofing/duplikasi → reviewer memeriksa bukti → publikasikan klarifikasi, bukan data pribadi → blokir abuse berulang dengan proses banding. Konten yang berpotensi membahayakan petugas/masyarakat ditahan dan diteruskan hanya melalui kanal otoritas yang sah jika diperlukan.

## 10. Keamanan, privasi, dan keselamatan

### 10.1 Threat model prioritas
| Ancaman | Kontrol |
|---|---|
| API abuse/scraping berlebihan | Rate limiting, caching, WAF jika diperlukan, quota and anomaly detection |
| Data palsu/geospasial direkayasa | Provenance, signature/checksum, source allowlist, review independen |
| Kebocoran pelapor/lokasi sensitif | Data minimization, geospatial masking/agregasi, storage privat, RBAC |
| Supply-chain compromise | Dependabot/setara, lockfile, SBOM, pinned GitHub Actions SHA untuk workflow sensitif, provenance rilis |
| Injection/SSRF dari konektor | Allowlist tujuan, parser ketat, URL fetching terkendali, least privilege |
| Bukti unggahan berbahaya | MIME/magic validation, ukuran maksimum, scanning, stripping EXIF dari versi publik, isolasi objek |
| Insider misuse / admin compromise | MFA/passkeys, JIT privileged access jika ada, audit immutable, review dua pihak |
| Kesalahan klaim oleh AI | Human review, eval dataset, audit log, model card, confidence caveat |
| Downtime/kejadian besar | Backup terenkripsi, uji restore, incident response, circuit breakers |

### 10.2 Peran akses
`anonymous_public`, `registered_contributor`, `trusted_reviewer`, `data_steward`, `org_admin`, `security_responder`. Gunakan *deny-by-default*, autentikasi untuk peninjauan, dan pemisahan pelaku publik vs pengelola data privat.

### 10.3 Privasi data masyarakat
- Pengiriman laporan di fase lanjutan harus consent-based, minimal metadata, opsi anonim yang tidak mengorbankan verifikasi.
- Lokasi presisi laporan dan metadata EXIF tidak diekspos publik; sediakan ketelitian yang diturunkan sesuai kebutuhan.
- Tentukan masa retensi, penghapusan, legal hold, audit akses, dan mekanisme permintaan subjek data sebelum menerima laporan.
- Peta publik tidak menampilkan koordinat rumah pelapor maupun lokasi detail infrastruktur rentan jika menambah risiko.

### 10.4 Kesiapsiagaan incident response keamanan
- `SECURITY.md`: private disclosure dan batas scope.
- Severity: critical/high/medium/low; triage terbatas; tidak mempublikasikan detail exploit sebelum mitigasi.
- Mekanisme disable ingestion/publishing, pembatalan token, rollback, backup/restore, komunikasi status.
- Uji tabletop dua kali setahun setelah tim operasi terbentuk.

### 10.5 Keselamatan publik
Pada halaman peta harus tertulis: "Data satelit mungkin terlambat/tidak lengkap dan tidak menggantikan informasi resmi. Untuk situasi darurat, ikuti instruksi instansi berwenang." Tidak ada kontribusi yang meminta orang mendekati titik api, menerobos pembatas, atau melakukan penanganan kebakaran mandiri.

## 11. Desain pengalaman pengguna dan aksesibilitas

### 11.1 Halaman web inti
- **Landing:** misi, status data, cakupan wilayah, cara berkontribusi, batasan penggunaan.
- **Live Observation Map:** filter sensor/waktu, legenda yang jujur, freshness bar, daftar observasi, fallback tabel.
- **Observation Detail:** provenance, UTC/lokal, confidence sensor apa adanya, catatan keterbatasan, tautan metodologi.
- **Region Overview:** tren jumlah observasi (bukan estimasi area kebakaran), cakupan periode, cuaca jika legal dan tersedia.
- **Data Catalog:** provider, atribut, hak pakai, versi dan changelog.
- **Community Portal:** GitHub Projects, issue berdasarkan skill, contributor guide, code of conduct, bilingual onboarding.
- **Research Methodology:** reproducibility, sumber, model cards, evaluasi bias dan keterbatasan.
- **Status Page:** stale provider, kegagalan ingest, jadwal pemeliharaan.

### 11.2 Prinsip UX
- Bahasa awal Indonesia dan Inggris, kemudian dukungan i18n tanpa mengubah model data.
- Peta tidak menjadi satu-satunya representasi; sediakan tabel/list keyboard-accessible.
- Warna indikator tidak boleh satu-satunya pembeda; sertai bentuk/label dan tekstur.
- Dukungan reduced motion, aksesibilitas WCAG 2.2 AA sebagai sasaran audit, dan mobile-first.
- Detail observasi harus menunjukkan **apa yang diketahui** dan **apa yang tidak diketahui**.
- Penggunaan offline/PWA terbatas hanya pada data cache yang jelas usianya; tidak disajikan sebagai keadaan terkini.

## 12. Sistem kontribusi komunitas GitHub

### 12.1 Jalur kontribusi
1. **Documentation & translation** — terminologi ilmiah, panduan aksesibilitas, klarifikasi metode.
2. **Good first issue** — komponen kecil dengan acceptance criteria dan test.
3. **GIS/data quality** — fixture sintetis, validasi koordinat, quality checks.
4. **Engineering** — API, UI, ingestion, observability, test.
5. **Scientific research** — proposal benchmark, dataset legal, peer review dan reproduksi.
6. **Security & privacy** — review, threat model, responsible disclosure.

### 12.2 Template Issue wajib
`Problem`, `Why it matters`, `Scope`, `Non-goals`, `Acceptance criteria`, `Data/source constraints`, `Safety/privacy review`, `Dependencies`, `Suggested size`, `Suggested labels`.

### 12.3 Alur kontribusi
Contributor membaca `CONTRIBUTING.md` → memilih issue berlabel → menyampaikan rencana singkat untuk pekerjaan medium/large → membuat branch pada fork → PR dengan checklist keamanan, tes, dokumentasi, screenshot bila UI → review CODEOWNERS → merge → changelog/release. Buka Discussions khusus bantuan kontributor baru dan penelitian.

### 12.4 Label standar
`priority:p0`, `priority:p1`, `priority:p2`; `type:feature`, `type:bug`, `type:docs`, `type:research`, `type:security`, `type:chore`; `area:frontend`, `area:api`, `area:ingestion`, `area:gis`, `area:data`, `area:community`; `good first issue`, `help wanted`, `needs-design`, `needs-data-license`, `needs-science-review`, `needs-safety-review`, `blocked`.

### 12.5 Perlindungan komunitas
- Code of Conduct dan proses pelaporan pelanggaran yang menjaga privasi.
- Tidak menyebut data identitas pribadi pelapor di Issues.
- Data demo/test harus sintetis atau dataset yang izin pakainya jelas.
- Kontributor dari berbagai tingkat keahlian mendapat mentoring, dokumentasi, dan review yang konstruktif.
- Pengakuan kontribusi berdasarkan artefak yang terverifikasi, bukan jumlah issue atau aktivitas spam.

## 13. Roadmap, milestone, dan gerbang rilis

| Rentang rencana | Milestone | Hasil | Exit gate |
|---|---|---|---|
| Minggu 1–2 | M0 — Foundation | Charter, governance, security baseline, lisensi, ADR, 3 repos disetujui | Dua pengelola bertanggung jawab; review kebijakan selesai |
| Minggu 3–6 | M1 — Data foundation | Source registry, kontrak data, ingest satu sumber, schema PostGIS | Provenance lengkap, data idempotent, legal review sumber |
| Minggu 7–10 | M2 — Map/API alpha | API read-only, peta Indonesia, filter, detail sumber, data freshness | Uji query, error behavior, aksesibilitas dasar |
| Minggu 11–14 | M3 — Public MVP beta | API docs, quality dashboard, stabilisasi security, contributor onboarding | Security review, privacy review, usability test, stale flags |
| Minggu 15–20 | M4 — Verification pilot | Workflow laporan (jika layak), moderation, reviewer training, status histories | Dual-review dan non-public evidence proven; partner pilot |
| Minggu 21–24 | M5 — v1.0 candidate | Dokumentasi, SOP incident response, observability, reproducibility | SLO terukur, legal signoff, rollback drill, rilis publik bertahap |

Rentang waktu adalah sasaran perencanaan **bukan jadwal terjamin**, bergantung pada jumlah maintainer, izin sumber data, dan dukungan infrastruktur. Jika legalitas/privasi laporan komunitas belum siap, tunda M4 tanpa menahan rilis peta pengamatan publik.

### 13.1 Komposisi tim minimal untuk MVP
- 1 product/technical lead (dapat merangkap maintainer).
- 1–2 full-stack developer.
- 1 GIS/data engineer.
- 1 reviewer sains/domain paruh waktu.
- 1 security/privacy reviewer paruh waktu.
- 1 community/docs maintainer paruh waktu.

### 13.2 Deployment: tiga lingkungan
`local` (Docker Compose, fixture sintetis), `staging` (test dan dataset sesuai lisensi), `production` (read-only publik dan kontrol administratif lebih ketat). Secrets berada pada secret manager/hosting, bukan `.env` yang di-commit. Gunakan migrasi forward/rollback yang diuji; staging harus aman dan tidak mempublikasikan laporan pelapor.

### 13.3 Estimasi biaya
Tanpa mengklaim harga vendor saat ini, kelompok biaya yang perlu dianggarkan: hosting API/web, database PostGIS, object storage, bandwidth tiles, monitoring, DNS, backup, layanan e-mail jika digunakan, beban ingest dan beban pemrosesan citra. Mulai dengan infrastruktur kecil dan pantau permintaan aktual; buat cost ceiling dan alarm agar proyek komunitas tidak menanggung biaya tidak terkendali.

## 14. Indikator keberhasilan dan pemeriksaan kualitas

| Dimensi | Indikator fase awal | Target awal |
|---|---|---|
| Provenance | Observasi publik dengan provider, sensor, observed_at, license reference | 100% |
| Integritas ingest | Duplikasi setelah re-run interval yang sama | 0 |
| Keterlambatan sistem | Ingest-to-publish setelah data diterima | p95 ≤ 15 menit bila sumber tersedia |
| Keamanan | Temuan kritis terbuka saat rilis publik | 0 |
| Privasi | Bukti/koordinat pelapor muncul di API publik | 0 |
| Transparansi | Halaman data-freshness dan keterbatasan sumber | Wajib pada MVP |
| Aksesibilitas | Temuan blocker pada alur inti | 0 saat GA |
| Komunitas | PR dari kontributor baru yang direview secara bermakna | Pantau bulanan, tanpa target spam |
| Kualitas ilmiah | Klaim kebakaran otomatis dari satu hotspot | 0 |
| Pemulihan | Restore test dan runbook rilis | Lulus sebelum GA |

KPI adalah **sasaran usulan**, bukan hasil pengukuran. Definisi dan instrumentasi harus diputuskan sebelum pengujian.

## 15. Matriks risiko dan keputusan yang harus disahkan

| Risiko | Dampak | Mitigasi/gerbang |
|---|---|---|
| Lisensi data tidak mengizinkan mirror | Tinggi | Source catalog + review ketentuan sebelum ingest/redistribusi |
| Pembacaan hotspot sebagai kebakaran pasti | Tinggi | Label status, disclaimer, halaman metodologi, science review |
| Ekspos pelapor/lokasi berbahaya | Kritis | Tidak mengumpulkan pada MVP; private geolocation di fase pilot |
| Akses GitHub organisasi belum tersedia | Sedang | Verifikasi organisasi, owner dan permissions sebelum implementasi |
| Kompleksitas terlalu dini | Tinggi | Monorepo awal, modul bertahap, hindari microservice/k8s sebelum perlu |
| Data tidak mutakhir/penyedia terganggu | Tinggi | Tampilan source lag, fallback aman, tidak memalsukan status baru |
| Review komunitas melemah | Sedang | CODEOWNERS, mentor, triage mingguan, review SLA yang realistis |
| Model AI bias dan overclaim | Tinggi | Benchmark, model cards, abstention, human review |
| Biaya tiles/traffic melonjak | Sedang | cache, quota, CDN, cost alert |

### 15.1 Keputusan sebelum implementasi
- [ ] Konfirmasi organisasi `open-karhutla`, dua pemegang hak owner, dan batas akses token.
- [ ] Sahkan charter, lisensi kode, lisensi dokumentasi, contributor agreement/DCO, code of conduct.
- [ ] Sahkan `platform` sebagai monorepo awal dan `community`/`geo-data` sebagai repo pendamping.
- [ ] Audit legalitas dan syarat akses data dari penyedia pertama.
- [ ] Sahkan batas keselamatan: pengamatan bukan peringatan resmi.
- [ ] Tentukan host awal, cadangan dan biaya maksimum.
- [ ] Tunjuk reviewer GIS, ilmiah, keamanan, dan privasi.
- [ ] Bekukan skema API/DB v0.1 setelah review teknis.
- [ ] Pilih strategi publikasi GitHub Issues: buat secara bertahap setelah repository ada.

## 16. Definisi selesai (Definition of Done)

Sebuah issue dianggap selesai bila acceptance criteria terpenuhi, unit/integration test relevan lulus, docs serta atribusi sumber diperbarui, tidak ada secrets/data pribadi, dampak safety/privacy telah diperiksa, perubahan direview CODEOWNERS, dan telah diverifikasi pada lingkungan yang sesuai. Pekerjaan penelitian juga memerlukan metodologi, sumber legal, metrik reproduktif, serta pembahasan ketidakpastian.

## 17. Rencana rilis MVP rekomendasi

**Rilis pertama sebaiknya bertajuk “OpenKarhutla Observations Beta”**, bukan “Live Fire Emergency Command”. Rilis berfokus pada data satelit dengan provenance/freshness yang jelas. Penilaian laporan warga, inferensi AI, dan peringatan yang memengaruhi keputusan keselamatan **tidak** diaktifkan secara default.

## 18. Catatan status

Blueprint ini mengikat rancangan konseptual **v1.0 sebagai usulan untuk disahkan**. Belum ada tindakan membuat repository, issue, branch, deploy, atau perubahan GitHub. Daftar 30 issue awal ada dalam dokumen pendamping dan merupakan nomor **backlog rancangan OKH-001 s.d. OKH-030**, **bukan** nomor issue GitHub yang telah diterbitkan.

---

**Referensi sumber yang perlu diverifikasi ulang saat implementasi:** dokumentasi resmi NASA FIRMS, penyedia data cuaca nasional, BIG, Copernicus/ESA, OpenStreetMap, PostgreSQL/PostGIS, MapLibre, dan dokumentasi GitHub (GitHub Organization, issue templates, CODEOWNERS, security advisories). Ketersediaan API, lisensi, persyaratan akses, dan versi perangkat lunak dapat berubah; tidak ada klaim verifikasi web terkini dalam dokumen ini.
