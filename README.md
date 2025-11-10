# Sentiment Analysis MotoGP Mandalika

Proyek analisis sentimen untuk menganalisis opini publik terkait event MotoGP dan Sirkuit Mandalika berdasarkan data dari berbagai sumber media sosial dan platform online.

## Deskripsi

Proyek ini menganalisis sentimen masyarakat terhadap:
- **Event Sentiment**: Sentimen terhadap penyelenggaraan event MotoGP
- **Circuit Sentiment**: Sentimen terhadap Sirkuit Mandalika sebagai venue

Dataset mencakup teks/caption dari berbagai platform media sosial (thread, x, dan google maps) yang dianalisis menggunakan teknik Natural Language Processing dan Machine Learning.

## Struktur Proyek

```
sentiment-analysis-mandalika/
├── sentiment-analysis.ipynb          # Notebook utama untuk analisis sentimen
├── labeling_dataset.csv              # Dataset dengan label sentimen (643KB)
├── unlabeled_dataset.csv             # Dataset belum dilabeli (1.5MB)
└── library/                          # Submodules untuk data collection
    ├── tweet-harvest/                # Scraping data dari Twitter/X
    │   └── scraping_mandalika.ipynb
    ├── thread/                       # Scraping data dari Threads
    └── gmaps-review/                 # Scraping data dari Google Maps Reviews
```

## Dataset

### Labeling Dataset (`labeling_dataset.csv`)
Dataset yang sudah dilabeli dengan kolom:
- `caption`: Teks/konten dari posting
- `created_at`: Timestamp posting
- `event_sentiment`: Label sentimen untuk event (positive/neutral/negative)
- `circuit_sentiment`: Label sentimen untuk sirkuit (positive/neutral/negative)

### Unlabeled Dataset (`unlabeled_dataset.csv`)
Dataset mentah yang belum diberi label sentimen, siap untuk proses pelabelan atau prediksi.

## Cara Menggunakan

### Prerequisites
- Python 3.8+
- Jupyter Notebook/Lab
- Libraries: pandas, numpy, scikit-learn, nltk, dan dependencies lainnya (lihat di notebook)

### Menjalankan Analisis
0. **Gunakan Notebook**
   Gunakan layanan notebook

1. **Jalankan notebook utama**
   ```bash
   jupyter notebook sentiment-analysis.ipynb
   ```

2. **Untuk scraping data baru** (opsional)
   - Twitter/X: `library/tweet-harvest/scraping_mandalika.ipynb`
   - Threads: `library/thread/`
   - Google Maps: `library/gmaps-review/`

## Metodologi

Proyek ini menggunakan pendekatan:
1. **Data Collection**: Scraping data dari berbagai sumber (Twitter, Threads, Google Maps)
2. **Data Preprocessing**: Cleaning dan normalisasi teks
3. **Labeling**: Pelabelan manual untuk training data
4. **Model Training**: Pelatihan model klasifikasi sentimen
5. **Evaluation**: Evaluasi performa model
6. **Prediction**: Prediksi sentimen pada data baru

## Kategori Sentimen

- **Positive**: Opini positif/mendukung
- **Neutral**: Opini netral/objektif
- **Negative**: Opini negatif/kritik

## Kontribusi

Proyek ini dibuat untuk keperluan akademis/riset. Kontribusi dan saran sangat diterima.

## Lisensi

NA

## Kontak

condro.wiyono@ui.ac.id

---

*Proyek Analisis Sentimen MotoGP Mandalika - Memahami Opini Publik Terhadap Event Balap Motor Dunia di Indonesia*
