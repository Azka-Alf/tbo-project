# Otomata.lab — Capstone Individu Teori Bahasa & Otomata

Aplikasi web terintegrasi yang mengimplementasikan empat topik inti mata kuliah **Teori Bahasa dan Otomata (TBO)**: Finite State Automata, Regular Expression, Pushdown Automata & Context-Free Grammar, serta Hierarki Chomsky & Chomsky Normal Form.

Dibuat sebagai Capstone Project Individu — Semester IV, Tahun Akademik 2025/2026 Genap.

**Live demo:** https://[nim-atau-nama].my.id
**Video demo (YouTube):** [tautan video demo]

---

## Daftar Isi

- [Deskripsi Proyek](#deskripsi-proyek)
- [Fitur per Modul](#fitur-per-modul)
- [Tech Stack](#tech-stack)
- [Cara Instalasi Lokal](#cara-instalasi-lokal)
- [Struktur Folder](#struktur-folder)
- [Format Input](#format-input)
- [Penggunaan Alat Bantu AI Generatif](#penggunaan-alat-bantu-ai-generatif)
- [Penulis](#penulis)

---

## Deskripsi Proyek

Otomata.lab adalah aplikasi web satu halaman (single-page application) yang memungkinkan pengguna mendefinisikan, mensimulasikan, dan memvisualisasikan berbagai model komputasi formal secara interaktif langsung dari browser, tanpa instalasi tambahan di sisi pengguna. Proyek ini disusun untuk memenuhi capaian pembelajaran mata kuliah TBO (CPMK1–CPMK4) dengan mengintegrasikan teori dan implementasi dalam satu produk yang dapat diakses publik.

## Fitur per Modul

### 1. Finite State Automata
- Simulator DFA/NFA berbasis definisi teks (states, alphabet, start, final, transitions)
- Uji penerimaan string dengan penelusuran (trace) langkah demi langkah dan visualisasi state aktif
- Konversi NFA → DFA melalui konstruksi subset (subset construction), lengkap dengan tabel transisi hasil
- Simulator Moore Machine dan Mealy Machine dengan urutan keluaran (output sequence)
- Visualisasi diagram state otomatis (SVG)

### 2. Regular Expression
- Parser regular expression (literal, `|`, `*`, `+`, `?`, pengelompokan `( )`)
- Konversi regex → NFA melalui konstruksi Thompson
- Pencocokan (matching) string terhadap pola
- Konversi NFA hasil ke DFA
- Penurunan otomatis aturan produksi grammar reguler (tipe-3 / right-linear) yang setara

### 3. Pushdown Automata & Context-Free Grammar
- Definisi CFG bebas oleh pengguna
- Simulasi penerimaan string oleh PDA berbasis CFG (pendekatan top-down/backtracking pada stack)
- Tampilan derivasi leftmost dan rightmost langkah demi langkah
- Visualisasi pohon penurunan (parse tree) secara grafis

### 4. Hierarki Chomsky & Chomsky Normal Form
- Konversi CFG sembarang ke Bentuk Normal Chomsky (CNF) secara bertahap:
  1. Eliminasi produksi-ε
  2. Eliminasi unit production
  3. Eliminasi simbol tak berguna (unreachable & non-generating)
  4. Isolasi terminal & binarisasi produksi
- Visualisasi hierarki Chomsky (Tipe 0–3)
- Klasifikasi heuristik tipe grammar yang dimasukkan pengguna

## Tech Stack

- **Frontend:** HTML5, CSS3 (custom, tanpa framework), JavaScript (vanilla, ES6+)
- **Visualisasi:** SVG native (diagram state, pohon penurunan, hierarki Chomsky)
- Tidak ada dependency backend — seluruh logika (parsing, simulasi, konversi) berjalan di sisi klien (client-side)


## Format Input

Setiap modul memiliki panel "Format & contoh" langsung di dalam aplikasi. Ringkasannya:

**FSA / Moore / Mealy**
```
states: q0,q1,q2
alphabet: 0,1
start: q0
final: q2
transitions:
q0,0,q0
q0,1,q1
```

**Regular Expression**
```
a(b|c)*d
```

**CFG (PDA & Chomsky/CNF)**
```
S -> a S b | ε
```

## Penggunaan Alat Bantu AI Generatif

> Wajib diisi sebelum pengumpulan sesuai Ketentuan Akademik dokumen tugas.

- **Tools yang digunakan:** [mis. Claude / ChatGPT / GitHub Copilot]
- **Bagian yang dibantu AI:** [mis. kerangka awal engine automata, styling CSS, draf dokumentasi]
- **Bagaimana dipahami & dimodifikasi:** [jelaskan verifikasi/pengujian yang dilakukan secara mandiri, mis. unit test pada engine, penyesuaian logika derivasi CFG, dst.]

## Penulis

- Nama: Mochamad Azka Alfarizi
- NIM: 301240022
- Mata Kuliah: Teori Bahasa dan Otomata — Semester IV, Genap 2025/2026
