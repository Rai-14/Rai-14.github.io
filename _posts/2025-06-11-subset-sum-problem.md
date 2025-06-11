---
title: "🧮 Rangkuman Singkat: Subset Sum Problem"
date: 2025-06-11 19:30:00 +0700
categories: [Algoritma, Dynamic Programming]
tags: [subset sum, dynamic programming, backtracking, problem solving]
toc: true
---

## 📌 Apa Itu Subset Sum Problem?

**Subset Sum Problem** adalah salah satu masalah klasik dalam **teori himpunan dan algoritma kombinatorik**, yang menanyakan apakah ada **subset dari elemen-elemen dalam array** yang jumlahnya sama dengan sebuah nilai target tertentu.

---

## 🎯 Deskripsi Masalah

### Diberikan:
- Array bilangan bulat: `S = [s₁, s₂, ..., sₙ]`
- Nilai target: `T`

### Tujuan:
Apakah mungkin ada subset dari `S` sedemikian sehingga jumlah elemen-elemen dalam subset tersebut = `T`?

---

## 📋 Contoh

```text
S = [3, 34, 4, 12, 5, 2]
T = 9

Output: True
Penjelasan: Subset [4, 5] memiliki jumlah 9.
