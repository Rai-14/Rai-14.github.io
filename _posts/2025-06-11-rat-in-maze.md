---
title: "🐭 Rangkuman Singkat: Rat in a Maze Problem"
date: 2025-06-11 20:00:00 +0700
categories: [Algoritma, Backtracking]
tags: [backtracking, maze, pathfinding, rat in maze, algoritma]
toc: true
---

## 🧩 Apa Itu Rat in a Maze Problem?

**Rat in a Maze** adalah masalah klasik dalam algoritma **backtracking**, di mana seekor tikus berada di posisi awal (biasanya kiri atas) dari sebuah **maze** (labirin) dan ingin mencapai posisi akhir (biasanya kanan bawah), hanya bisa bergerak ke **arah tertentu** (biasanya: bawah dan kanan atau keempat arah), dan hanya melalui **jalur yang aman (nilai 1)**.

---

## 🎯 Tujuan

Temukan **semua jalur yang memungkinkan** dari titik awal ke titik tujuan dengan **menghindari rintangan** dan **tanpa melewati sel yang sama lebih dari sekali**.

---

## 📋 Representasi Maze

Maze diwakili oleh matriks `N × N`, berisi:
- `1` → sel yang bisa dilewati
- `0` → rintangan atau dinding

Contoh maze:

```text
1 0 0 0
1 1 0 1
0 1 0 0
1 1 1 1
