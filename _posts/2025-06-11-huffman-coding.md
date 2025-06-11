---
title: "🧬 Rangkuman Singkat: Huffman Coding"
date: 2025-06-11 16:00:00 +0700
categories: [Algoritma, Struktur Data]
tags: [huffman coding, greedy, compression, algoritma, tree]
toc: true
---

## 🔍 Apa Itu Huffman Coding?

**Huffman Coding** adalah algoritma kompresi data berbasis **Greedy Algorithm** yang digunakan untuk **mengurangi ukuran file atau pesan** tanpa kehilangan informasi (lossless compression).

Algoritma ini membuat **kode biner optimal** untuk setiap karakter berdasarkan **frekuensi kemunculannya** — karakter yang sering muncul mendapat kode lebih pendek, sedangkan yang jarang muncul mendapat kode lebih panjang.

---

## 🎯 Tujuan

Menyusun **kode prefix** (kode yang tidak saling menjadi awalan satu sama lain) sehingga **total panjang encoding** untuk seluruh pesan menjadi **sekecil mungkin**.

---

## 🧩 Deskripsi Masalah

### Diberikan:
- Sekumpulan simbol/karakter beserta frekuensi/kemunculannya.

### Tujuan:
- Bangun *binary tree* Huffman.
- Gunakan tree tersebut untuk menghasilkan *bit encoding* untuk setiap karakter.

---

## ⚙️ Langkah-Langkah Algoritma Huffman

1. Buat node untuk setiap karakter dan masukkan ke **priority queue** (berdasarkan frekuensi).
2. Ulangi hingga hanya ada satu node dalam queue:
   - Ambil dua node dengan frekuensi terkecil.
   - Buat node baru dengan frekuensi gabungan dari dua node tersebut.
   - Node baru menjadi parent, yang lama menjadi child (kiri dan kanan).
   - Masukkan node baru ke queue.
3. Setelah tree terbentuk, lakukan *traversal*:
   - Ke kiri → tambahkan `0`
   - Ke kanan → tambahkan `1`
   - Kode untuk karakter ditemukan di daun (leaf node)

---

## 📊 Contoh

### Input:

```text
Karakter   Frekuensi
   A           5
   B           9
   C           12
   D           13
   E           16
   F           45
