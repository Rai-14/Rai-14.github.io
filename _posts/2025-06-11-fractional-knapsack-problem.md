---
title: "🎒 Rangkuman Singkat: Fractional Knapsack Problem"
date: 2025-06-11 14:00:00 +0700
categories: [Algoritma, Greedy]
tags: [greedy, knapsack, fractional, algoritma, problem solving]
toc: true
---

## 🎯 Apa Itu Fractional Knapsack Problem?

**Fractional Knapsack Problem** adalah varian dari masalah klasik *Knapsack*, dan merupakan salah satu contoh aplikasi **Greedy Algorithm**.

Berbeda dari **0/1 Knapsack** yang membatasi item hanya bisa diambil seluruhnya atau tidak sama sekali, dalam **Fractional Knapsack**, kita **boleh mengambil sebagian** dari suatu item — sesuai fraksinya.

---

## 🧩 Deskripsi Masalah

### Diberikan:
- `n` item, masing-masing memiliki:
  - berat `w[i]`
  - nilai `v[i]`
- Kapasitas maksimum knapsack: `W`

### Tujuan:
Memilih item (atau bagiannya) agar total nilai maksimal, **tanpa melebihi kapasitas** `W`.

---

## ⚙️ Strategi Penyelesaian (Greedy)

Langkah-langkah utama:

1. Hitung rasio nilai per berat dari setiap item: `value/weight`.
2. Urutkan item berdasarkan rasio tersebut secara **menurun**.
3. Ambil sebanyak mungkin dari item dengan rasio tertinggi:
   - Jika masih muat → ambil seluruhnya
   - Jika tidak → ambil sebagian sesuai sisa kapasitas

---

## 📊 Contoh

```text
Item:     1   2   3
Value:   60 100 120
Weight:  10  20  30
Kapasitas W = 50
