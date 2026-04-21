# 👑 Mapping The Dynasties: Nusantara Knowledge Graph integration

Proyek UTS Mata Kuliah Graf - Departemen Sistem Informasi ITS.

## 👥 Tim Proyek
- **[Nama Temenmu]** (Data Engineer / Menteri Data)
- **Bara Ardiwinata** (Graph Analyst / Menteri Analisis)

## 📌 Deskripsi Proyek
Proyek ini mengintegrasikan data silsilah kerajaan Nusantara dari **Wikidata** dan **DBpedia Indonesia** untuk membangun *Knowledge Graph*. Kami menganalisis struktur kekuasaan dan hubungan kekerabatan menggunakan algoritma Centrality, Similarity, dan Community Detection.

🔗 **Laporan Lengkap (Wikidata):** [Isi Link Halaman User Wikidata Kamu di Sini]

## 🛠️ Tech Stack
- **Data Extraction:** SPARQL (Wikidata Query Service & DBpedia Endpoint)
- **Data Processing:** Python (Pandas)
- **Graph Analysis:** NetworkX & Neo4j
- **Documentation:** Wikidata Namespace

## 🚀 Cara Menjalankan
1. Eksekusi notebook di folder `/notebooks` untuk melakukan ekstraksi dan integrasi data.
2. Hasil integrasi akan tersimpan di `/data/dataset_gabungan_uts_graf.csv`.
3. Gunakan script analisis untuk mendapatkan metrik graf.

## 📊 Hasil Analisis (Preview)
- **Tokoh Paling Sentral:** [Isi Nama Tokoh]
- **Jumlah Komunitas Terdeteksi:** [Isi Jumlah]