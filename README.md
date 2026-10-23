# 🔑 SmartKey — AI-Driven Cryptographic Digital Signature

SmartKey adalah aplikasi riset (PoC) berbasis Streamlit untuk menganalisis dan mengoptimasi parameter kecerdasan buatan (AI) dalam membangkitkan kunci kriptografi (*seed*) untuk Tanda Tangan Digital yang memiliki entropi tinggi.

## 🌟 Fitur Utama
1. **AI Key Generators**: Mendukung Genetic Algorithm (GA), Artificial Neural Network (ANN), dan Ant Colony Optimization (ACO) untuk membangun *seed* kunci kriptografi secara pseudorandom.
2. **Standard Kriptografi**: Pembuatan *keypair*, *Signing*, dan *Verifying* menggunakan algoritma RSA, DSA, dan ElGamal.
3. **NIST & Entropy Evaluation**: Seluruh *seed* yang dihasilkan dievaluasi tingkat keacakannya menggunakan Shannon Entropy dan NIST Statistical Test Suite (Frequency, Block Frequency, Runs).
4. **Interactive Dashboard**: Visualisasi uji dan skor parameter secara interaktif menggunakan komponen Streamlit.

## 🚀 Cara Menjalankan Aplikasi

1. **Persyaratan Sistem**:
   - Python 3.10 atau yang lebih baru.
   - Disarankan menggunakan Virtual Environment (`venv`).

2. **Instalasi**:
   ```bash
   python -m venv venv
   # Windows
   .\venv\Scripts\activate
   # Linux/Mac
   source venv/bin/activate
   
   pip install -r requirements.txt
   ```

3. **Menjalankan Aplikasi (UI)**:
   ```bash
   streamlit run app.py
   ```
   Aplikasi akan otomatis terbuka di browser pada alamat `http://localhost:8501`.

4. **Menjalankan Pengujian (Unit Tests)**:
   ```bash
   pytest tests/ -v
   ```

## 📁 Struktur Direktori
- `modules/ai/`: Kerangka modul generator bit menggunakan algoritma kecerdasan buatan (GA, ANN, ACO).
- `modules/crypto/`: Pengonversi *seed* dari AI menjadi kunci privat & publik serta eksekusi operasi Tanda Tangan (RSA, DSA, ElGamal).
- `modules/evaluation/`: Alat pengukur efektivitas kunci (Kalkulator Entropi dan subset Uji Keacakan NIST).
- `ui/`: Kerangka antarmuka pengguna Streamlit (Sidebar, Dashboard, Signing Panel, dan Ekspor Output).
- `tests/`: Kumpulan skrip pengujian unit otomatis (*Pytest*).
- `app.py`: Titik masuk (entry point) utama untuk menjalankan aplikasi Streamlit.
- `requirements.txt`: Daftar pustaka Python yang dibutuhkan.

---
**SmartKey Project** - Riset Analisis Versi Terbaik AI pada Digital Signature
