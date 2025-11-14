# **Stack**

## **1. Kode Program**

```python
# stack and stack operations
stack = []

# Push
stack.append('A')
stack.append('B')
stack.append('C')
print("Stack: ", stack)

# Pop
element = stack.pop()
print("pop: ", element)

# Peek
topElement = stack[-1]
print("peek: ", topElement)

# isEmpty
isEmpty = not bool(stack)
print("isEmpty: ", isEmpty)

# Size
print("size: ", len(stack))
```

---

## **2. Penjelasan**

### **A) Membuat Stack Kosong**

```python
stack = []
```

> Baris ini membuat sebuah stack kosong. Stack disimpan dalam bentuk list karena list dapat digunakan untuk menampung data secara berurutan.

---

### **B) Push (Menambahkan Elemen ke Stack)**

```python
stack.append('A')
stack.append('B')
stack.append('C')
print("Stack: ", stack)
```

> Operasi *push* menambahkan elemen ke posisi paling akhir. Data A, B, dan C dimasukkan secara berurutan sehingga isi stack menjadi:
>
> `['A', 'B', 'C']`
>
> **Output:**
> `Stack: ['A', 'B', 'C']`

---

### **C) Pop (Menghapus Elemen Teratas)**

```python
element = stack.pop()
print("pop: ", element)
```

> Fungsi `pop()` digunakan untuk menghapus dan mengambil elemen paling atas. Karena C adalah elemen yang terakhir masuk, maka C yang akan dikeluarkan.
>
> **Output:**
> `Pop: C`

---

### **D) Peek (Melihat Elemen Teratas Tanpa Menghapus)**

```python
topElement = stack[-1]
print("peek: ", topElement)
```

> *Peek* digunakan untuk melihat elemen paling atas tanpa mengubah isi stack.
> Setelah C terhapus, elemen teratas menjadi `'B'`.

---

### **E) isEmpty (Mengecek Apakah Stack Kosong)**

```python
isEmpty = not bool(stack)
print("isEmpty: ", isEmpty)
```

> Kode ini memeriksa apakah stack kosong.
> `bool(stack)` bernilai **True** jika stack berisi data, dan **False** jika kosong.
> Karena stack masih berisi A dan B, maka hasilnya **False**.
>
> **Output:**
> `isEmpty: False`

---

### **F) Size (Menampilkan Jumlah Elemen)**

```python
print("size: ", len(stack))
```

> Baris ini menampilkan ukuran stack dengan `len()`.
> Saat ini masih ada dua elemen, yaitu A dan B.
>
> **Output:**
> `Size: 2`

---

## **3. Hasil Eksekusi**

```
Stack:  ['A', 'B', 'C']
Pop:  C
Peek:  B
isEmpty:  False
Size:  2
```

---

## **4. Kesimpulan**

Stack merupakan struktur data yang menggunakan metode **LIFO (Last In, First Out)**, yaitu elemen yang paling terakhir dimasukkan menjadi elemen pertama yang dikeluarkan. Pada Python, struktur stack dapat dibangun menggunakan list dengan bantuan fungsi `append()` untuk melakukan push dan `pop()` untuk melakukan penghapusan data. Stack juga memungkinkan pengguna melakukan pengecekan elemen teratas (*peek*), memeriksa apakah stack kosong, serta mengetahui jumlah elemen yang tersimpan.


   
