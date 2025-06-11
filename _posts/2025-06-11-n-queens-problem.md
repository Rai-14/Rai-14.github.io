---
title: "♛ Rangkuman Singkat: N-Queens Problem"
date: 2025-06-11 18:00:00 +0700
categories: [Algoritma, Backtracking]
tags: [backtracking, n-queens, algoritma, rekursif, dsa]
toc: true
---

## 🧩 Apa Itu N-Queens Problem?

**N-Queens Problem** adalah masalah klasik dalam algoritma dan teori permainan. Tujuannya adalah menempatkan **N buah ratu (queen)** di papan catur berukuran **N × N** sehingga **tidak ada dua ratu yang saling menyerang** satu sama lain.

---

## 🎯 Aturan Penempatan Ratu

Ratu bisa menyerang secara:
- **Vertikal (kolom yang sama)**
- **Horisontal (baris yang sama)**
- **Diagonal (kedua arah)**

Maka solusi yang valid harus memastikan:
- Hanya **satu ratu per baris**
- Hanya **satu ratu per kolom**
- Tidak ada dua ratu di **diagonal yang sama**

---

## 🔄 Strategi Penyelesaian: Backtracking

### Pendekatan Umum:

1. Tempatkan ratu di **baris pertama**, coba di setiap kolom.
2. Lanjut ke baris berikutnya:
   - Coba setiap kolom
   - **Cek apakah aman** menaruh ratu di kolom itu (tidak diserang ratu sebelumnya)
3. Jika aman, lanjut ke baris selanjutnya (rekursif).
4. Jika tidak bisa lanjut (dead end), **backtrack**: hapus ratu terakhir dan coba kolom lain.
5. Ulangi hingga semua ratu berhasil ditempatkan (baris ke-N).

---

## 🧠 Kenapa Backtracking?

Karena solusi lengkap tidak bisa dicari secara langsung — kita harus **membangun solusi bertahap**, mencoba semua kemungkinan, dan **mundur saat menemui konflik**.

---

## 👨‍💻 Contoh: 4-Queens Problem

Salah satu solusi valid:

