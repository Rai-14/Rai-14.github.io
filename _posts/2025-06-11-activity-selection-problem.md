---
title: "🧠 Rangkuman Singkat: Activity Selection Problem"
date: 2025-06-11 10:00:00 +0700
categories: [Algoritma, Greedy]
tags: [greedy, algoritma, activity selection, problem solving]
toc: true
---

## 🎯 Apa Itu Activity Selection Problem?

**Activity Selection Problem** adalah salah satu contoh klasik dari _Greedy Algorithm_ dalam dunia algoritma dan struktur data. Masalah ini berkaitan dengan memilih sejumlah kegiatan dari sekumpulan kegiatan yang diberikan, sehingga tidak ada dua kegiatan yang saling tumpang tindih waktunya, dan jumlah kegiatan yang dipilih **sebesar mungkin**.

---

## 🧩 Deskripsi Masalah

### Diberikan:
- `n` aktivitas, masing-masing memiliki:
  - waktu mulai (`start[i]`)
  - waktu selesai (`finish[i]`)

### Tujuan:
Memilih aktivitas sebanyak mungkin **tanpa ada yang saling tumpang tindih**, berdasarkan waktu mulai dan selesai masing-masing.

---

## ⚙️ Strategi Penyelesaian (Greedy)

Langkah-langkah utama:

1. **Urutkan** semua aktivitas berdasarkan waktu selesai (`finish[]`) secara menaik.
2. **Pilih** aktivitas pertama (yang selesai paling awal).
3. Untuk aktivitas selanjutnya, **pilih hanya jika** waktu mulai-nya ≥ waktu selesai aktivitas yang terakhir dipilih.
4. Ulangi hingga semua aktivitas telah diproses.

### Kenapa Greedy?
Strategi ini berhasil karena dengan selalu memilih aktivitas yang selesai lebih awal, kita menyisakan waktu sebanyak mungkin untuk aktivitas-aktivitas berikutnya.

---

## 📊 Contoh

```text
start[]  =  {1, 3, 0, 5, 8, 5}
finish[] =  {2, 4, 6, 7, 9, 9}
