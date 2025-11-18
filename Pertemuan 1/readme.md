# **Implementasi Stack dan Queue pada Python**


# **Stack**

## **1. Penjelasan**

### **A) Membuat Stack Kosong**

Stack dimulai dari kondisi kosong. Dalam Python, struktur ini biasanya dibuat menggunakan *list* karena mudah digunakan untuk menyimpan data secara berurutan.

### **B) Push (Menambahkan Elemen ke Stack)**

Operasi *push* menambahkan elemen baru ke bagian paling atas. Setelah memasukkan A, B, dan C, stack akan berisi:

```
['A', 'B', 'C']
```

Elemen C berada di posisi teratas karena dimasukkan terakhir.

### **C) Pop (Menghapus Elemen Teratas)**

Operasi *pop* menghapus sekaligus mengambil elemen teratas. Karena C adalah elemen yang terakhir masuk, maka C yang akan keluar terlebih dahulu.

### **D) Peek (Melihat Elemen Teratas Tanpa Menghapus)**

*Peek* digunakan untuk melihat elemen teratas tanpa menghilangkannya.
Setelah C dihapus, elemen paling atas berubah menjadi **B**.

### **E) isEmpty (Mengecek Apakah Stack Kosong)**

Pengecekan dilakukan untuk mengetahui apakah stack masih berisi elemen.
Jika masih ada data, hasil pengecekan adalah **False**.

### **F) Size (Menampilkan Jumlah Elemen)**

Jumlah elemen dihitung berdasarkan isi stack. Setelah satu elemen dihapus, tersisa dua elemen: **A dan B**.


## **2. Hasil Eksekusi**

```
Stack:  ['A', 'B', 'C']
Pop:  C
Peek:  B
isEmpty:  False
Size:  2
```


## **3. Kesimpulan**

Stack adalah struktur data yang menerapkan prinsip **LIFO (Last In, First Out)**, di mana elemen yang terakhir masuk akan menjadi elemen pertama yang keluar.
Di Python, stack dapat diimplementasikan menggunakan *list* dengan operasi seperti:

* menambah elemen (*push*)
* menghapus elemen teratas (*pop*)
* melihat elemen teratas (*peek*)
* mengecek apakah stack kosong
* menghitung jumlah elemen dalam stack


# **Queue**

## **1. Penjelasan**

### **A) Membuat Queue Kosong**

Queue dimulai dari kondisi kosong. Dalam Python, queue dapat dibangun menggunakan *list* karena mendukung penambahan di belakang dan penghapusan di depan.

### **B) Enqueue (Menambahkan Elemen ke Queue)**

Operasi *enqueue* menambahkan elemen ke bagian paling belakang. Setelah memasukkan A, B, dan C, queue berisi:

```
['A', 'B', 'C']
```

### **C) Dequeue (Menghapus Elemen dari Depan)**

*Dequeue* digunakan untuk mengambil elemen paling depan.
Karena A adalah elemen pertama yang masuk, maka A juga yang keluar terlebih dahulu.

### **D) Peek (Melihat Elemen Depan Tanpa Menghapus)**

*Peek* digunakan untuk melihat elemen yang berada di bagian depan.
Setelah A dihapus, elemen terdepan berubah menjadi **B**.

### **E) isEmpty (Memeriksa Apakah Queue Kosong)**

Jika queue masih berisi elemen, hasil pengecekan adalah **False**, yang berarti queue tidak kosong.

### **F) Size (Menampilkan Jumlah Elemen dalam Queue)**

Setelah satu elemen keluar, jumlah elemen yang tersisa adalah **2**, yaitu B dan C.


## **2. Hasil Eksekusi**

```
Queue:  ['A', 'B', 'C']
Dequeue:  A
peek:  B
isEmpty:  False
size:  2
```


## **3. Kesimpulan**

Queue adalah struktur data yang menggunakan prinsip **FIFO (First In, First Out)**, yaitu elemen yang pertama masuk akan menjadi elemen pertama yang keluar.
Dalam Python, queue dapat dibangun menggunakan *list* dengan operasi seperti:

* menambah elemen ke belakang (*enqueue*)
* menghapus elemen dari depan (*dequeue*)
* melihat elemen terdepan (*peek*)
* memeriksa kondisi kosong
* mengetahui jumlah elemen yang tersisa
  
