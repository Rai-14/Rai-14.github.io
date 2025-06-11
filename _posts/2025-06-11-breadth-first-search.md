---
title: "🔍 Rangkuman Singkat: Breadth First Search (BFS)"
date: 2025-06-11 20:30:00 +0700
categories: [Algoritma, Graph Traversal]
tags: [bfs, graph, traversal, pencarian, algoritma dasar]
toc: true
---

## 🔄 Apa Itu BFS?

**Breadth First Search (BFS)** adalah algoritma pencarian atau penelusuran **graf** dan **pohon** yang bekerja dengan menjelajahi simpul secara **melebar (level demi level)** sebelum melangkah lebih dalam.

---

## 📌 Karakteristik Utama

- Menggunakan **queue (antrian)**
- Menjelajah tetangga dulu sebelum ke anak dari tetangga
- Cocok untuk mencari **jalur terpendek** dalam graf tak berbobot

---

## 🌐 Representasi Graf

Graf bisa direpresentasikan dalam bentuk:
- **Adjacency List** (umum)
- **Adjacency Matrix** (padat)

---

## 🧠 Cara Kerja BFS (Langkah-langkah)

1. Masukkan node awal ke dalam queue
2. Tandai node sebagai sudah dikunjungi
3. Selama queue tidak kosong:
   - Ambil node dari depan queue
   - Kunjungi semua tetangganya yang belum dikunjungi
   - Tambahkan mereka ke queue dan tandai sebagai dikunjungi

---

## 👨‍💻 Contoh Implementasi (Python)

```python
from collections import deque

def bfs(graph, start):
    visited = set()
    queue = deque([start])

    while queue:
        node = queue.popleft()
        if node not in visited:
            print(node, end=' ')
            visited.add(node)
            for neighbor in graph[node]:
                if neighbor not in visited:
                    queue.append(neighbor)

# Contoh penggunaan
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}

bfs(graph, 'A')
