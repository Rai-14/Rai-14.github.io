---
title: "📊 Rangkuman Singkat: Kahn's Algorithm untuk Topological Sorting"
date: 2025-06-11 21:00:00 +0700
categories: [Algoritma, Graph]
tags: [kahn, topological-sort, graph, algoritma, sorting]
toc: true
---

## 🔄 Apa Itu Kahn's Algorithm?

**Kahn’s Algorithm** adalah metode untuk melakukan **topological sorting** pada graf berarah **acyclic** (DAG – Directed Acyclic Graph) menggunakan pendekatan berbasis **indegree**.

---

## 🎯 Tujuan Topological Sort

Menyusun urutan simpul dari graf sedemikian rupa sehingga **jika ada sisi dari A → B, maka A muncul sebelum B** dalam urutan.

---

## 📦 Konsep Dasar

- Topological Sort hanya berlaku untuk **graf berarah dan tanpa siklus (DAG)**
- Kahn’s Algorithm menggunakan **indegree (jumlah sisi masuk)** setiap simpul
- Proses utama: **hapus simpul dengan indegree 0**, lalu kurangi indegree simpul-simpul yang bergantung padanya

---

## 🔁 Langkah-Langkah Kahn’s Algorithm

1. Hitung **indegree** untuk semua simpul
2. Masukkan semua simpul dengan **indegree 0** ke dalam queue
3. Selama queue tidak kosong:
   - Ambil simpul dari depan queue
   - Tambahkan ke hasil topological sort
   - Kurangi indegree semua tetangganya
   - Jika indegree tetangga menjadi 0, masukkan ke queue
4. Jika jumlah simpul dalam hasil ≠ jumlah simpul dalam graf, berarti ada **siklus**

---

## 👨‍💻 Contoh Implementasi (Python)

```python
from collections import deque, defaultdict

def kahn_topological_sort(graph):
    indegree = defaultdict(int)
    for node in graph:
        for neighbor in graph[node]:
            indegree[neighbor] += 1

    queue = deque([node for node in graph if indegree[node] == 0])
    topo_order = []

    while queue:
        current = queue.popleft()
        topo_order.append(current)

        for neighbor in graph[current]:
            indegree[neighbor] -= 1
            if indegree[neighbor] == 0:
                queue.append(neighbor)

    if len(topo_order) != len(graph):
        print("Graf memiliki siklus. Topological sort tidak mungkin.")
    else:
        print("Topological Order:", topo_order)

# Contoh penggunaan
graph = {
    'A': ['C'],
    'B': ['C', 'D'],
    'C': ['E'],
    'D': ['F'],
    'E': ['H', 'F'],
    'F': ['G'],
    'G': [],
    'H': []
}

kahn_topological_sort(graph)
