---
title: "🌲 Rangkuman Singkat: Depth First Search (DFS)"
date: 2025-06-11 20:45:00 +0700
categories: [Algoritma, Graph Traversal]
tags: [dfs, graph, traversal, pencarian, algoritma dasar]
toc: true
---

## 🌐 Apa Itu DFS?

**Depth First Search (DFS)** adalah algoritma penelusuran pada **graf** atau **pohon** yang menjelajah dengan cara **sedalam mungkin ke satu arah**, baru kemudian mundur (backtrack) untuk menjelajah cabang lainnya.

---

## 📌 Karakteristik Utama

- Menggunakan **stack** (baik eksplisit maupun rekursi)
- Penelusuran menyelam sedalam mungkin sebelum beralih cabang
- Cocok untuk eksplorasi menyeluruh, pendeteksian siklus, atau topological sort

---

## 📋 Representasi Graf

Graf bisa direpresentasikan dalam:
- **Adjacency List** (paling umum)
- **Adjacency Matrix**

---

## 🔁 Cara Kerja DFS

1. Mulai dari node awal
2. Tandai sebagai dikunjungi
3. Untuk setiap tetangga yang belum dikunjungi:
   - Rekursif panggil DFS pada tetangga tersebut
4. Kembali jika tidak ada lagi tetangga

---

## 👨‍💻 Contoh Implementasi (Python, Rekursif)

```python
def dfs(graph, node, visited=None):
    if visited is None:
        visited = set()

    if node not in visited:
        print(node, end=' ')
        visited.add(node)
        for neighbor in graph[node]:
            dfs(graph, neighbor, visited)

# Contoh penggunaan
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}

dfs(graph, 'A')
