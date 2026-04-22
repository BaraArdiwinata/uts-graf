# 👑 Mapping The Dynasties: Nusantara Knowledge Graph Integration

Proyek UTS Mata Kuliah Graf - Departemen Sistem Informasi, Institut Teknologi Sepuluh Nopember (ITS).

## 👥 Tim Proyek
- **Annisa Nur Fauzi** 5026231228
- **Bara Ardiwinata** 5026231232

## 📌 Deskripsi Proyek
Proyek ini mengintegrasikan data silsilah kerajaan Nusantara dari **Wikidata** (untuk topologi relasi kekerabatan) dan **DBpedia** (untuk pengayaan atribut sejarah seperti ibu kota, agama, dan suksesi). Kami membangun *Knowledge Graph* untuk mengungkap koneksi tersembunyi di balik peta kekuasaan kerajaan-kerajaan besar di Indonesia melalui pendekatan *Linked Open Data* (LOD).

Kami menggunakan strategi **Two-Step Query Optimization** untuk mengekstraksi 132 entitas kerajaan dan menghasilkan jaringan silsilah yang terdiri dari 406 relasi (edges) yang valid.

🔗 **Laporan Lengkap & Dokumentasi:** [User:Bara Ardiwinata/Mapping The Dynasties](https://www.wikidata.org/wiki/User:Bara_Ardiwinata/Mapping_The_Dynasties)

## 🛠️ Tech Stack
- **Data Acquisition:** SPARQL (Wikidata Query Service & DBpedia Endpoint)
- **Processing & Cleaning:** Python (Pandas)
- **Graph Metrics & Analysis:** NetworkX & Neo4j Graph Data Science
- **Storage:** CSV & Graph Databases

## 🚀 Alur Kerja
1. **Extraction:** Menjaring 132 Q-Nodes kerajaan dan menginjeksi ID ke kueri tahap kedua untuk menarik 486 baris data tokoh (Manusia - wd:Q5).
2. **Integration:** Melakukan *Entity Alignment* menggunakan `owl:sameAs` antara Wikidata dan DBpedia.
3. **Cleaning:** Normalisasi string dan eliminasi redundansi, menghasilkan dataset final 406 baris di `/data/dataset_gabungan_final.csv`.
4. **Analysis:** Menjalankan algoritma PageRank, Louvain Modularity, dan Jaccard Similarity.

## 📊 Hasil Analisis (Key Findings)

| Metrik | Hasil Utama | Interpretasi |
| :--- | :--- | :--- |
| **Tokoh Paling Sentral** | **Kertabhumi** (PageRank: 0.0178) | Bertindak sebagai *Central Hub* penghubung Majapahit dan Demak. |
| **Komunitas Terdeteksi** | **15 Klaster** (Louvain Modularity) | Berhasil mengelompokkan klaster alami (Sultan Banjar) dan mengisolasi residu data kotor. |
| **Kemiripan Silsilah** | **Taming Sari & Ra Kuti** (Jaccard: 1.00) | Membongkar fenomena oversimplifikasi data historis di Wikidata. |

> *"The architecture of complexity is always built on the simple rules of connection."* – Albert-László Barabási

---