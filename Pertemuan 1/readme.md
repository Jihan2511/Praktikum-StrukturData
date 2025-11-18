# **Stack**

## **1. Penjelasan**

### **A) Membuat Stack Kosong**

Baris ini membuat sebuah stack kosong. Stack disimpan dalam bentuk list karena list dapat digunakan untuk menampung data secara berurutan.

### **B) Push (Menambahkan Elemen ke Stack)**

Operasi push menambahkan elemen ke posisi paling akhir. Data A, B, dan C dimasukkan secara berurutan sehingga isi stack menjadi:

```
['A', 'B', 'C']
```

*Output:*
`Stack: ['A', 'B', 'C']`

### **C) Pop (Menghapus Elemen Teratas)**

Fungsi pop() digunakan untuk menghapus dan mengambil elemen paling atas. Karena C adalah elemen yang terakhir masuk, maka C yang akan dikeluarkan.

*Output:*
`Pop: C`

### **D) Peek (Melihat Elemen Teratas Tanpa Menghapus)**

Peek digunakan untuk melihat elemen paling atas tanpa mengubah isi stack.
Setelah C terhapus, elemen teratas menjadi **'B'**.

### **E) isEmpty (Mengecek Apakah Stack Kosong)**

Kode ini memeriksa apakah stack kosong.
`bool(stack)` bernilai *True* jika stack berisi data, dan *False* jika kosong.
Karena stack masih berisi A dan B, maka hasilnya **False**.

*Output:*
`isEmpty: False`

### **F) Size (Menampilkan Jumlah Elemen)**

Baris ini menampilkan ukuran stack dengan `len()`.
Saat ini masih ada dua elemen, yaitu A dan B.

*Output:*
`Size: 2`


## **2. Hasil Eksekusi**

```
Stack:  ['A', 'B', 'C']
Pop:  C
Peek:  B
isEmpty:  False
Size:  2
```


## **3. Kesimpulan**

Stack merupakan struktur data yang menggunakan metode **LIFO (Last In, First Out)**, yaitu elemen yang paling terakhir dimasukkan menjadi elemen pertama yang dikeluarkan.
Pada Python, struktur stack dapat dibangun menggunakan list dengan operasi seperti:

* menambah elemen (push)
* menghapus elemen teratas (pop)
* melihat elemen teratas (peek)
* memeriksa apakah stack kosong
* mengetahui jumlah elemen yang tersimpan


# **Queue**

## **1. Penjelasan**

### **A) Membuat Queue Kosong**

Baris ini digunakan untuk membuat sebuah queue kosong. Queue disimpan dalam bentuk list karena Python dapat menampung data secara berurutan dan memudahkan penambahan elemen di belakang serta penghapusan di depan.

### **B) Enqueue (Menambahkan Elemen ke Queue)**

Operasi enqueue menambahkan elemen ke bagian belakang antrian. Setelah memasukkan A, B, dan C, queue akan berisi:

```
['A', 'B', 'C']
```

*Output:*
`Queue: ['A', 'B', 'C']`

### **C) Dequeue (Menghapus Elemen dari Depan)**

Fungsi `pop(0)` digunakan untuk menghapus elemen dari urutan paling depan. Karena A masuk pertama, maka A yang pertama dikeluarkan.

*Output:*
`Dequeue: A`

### **D) Peek (Melihat Elemen Depan Tanpa Menghapus)**

Peek digunakan untuk melihat elemen paling depan tanpa menghapusnya. Setelah A dihapus, posisi terdepan diisi oleh **B**.

*Output:*
`peek: B`

### **E) isEmpty (Memeriksa Apakah Queue Kosong)**

`bool(queue)` akan bernilai *True* jika masih ada elemen. Karena queue masih berisi dua elemen (B dan C), maka hasilnya **False**.

*Output:*
`isEmpty: False`

### **F) Size (Menampilkan Jumlah Elemen dalam Queue)**

Fungsi `len()` menghitung jumlah elemen dalam queue. Setelah dequeue, tersisa dua elemen yaitu B dan C.

*Output:*
`size: 2`


## **2. Hasil Eksekusi**

```
Queue:  ['A', 'B', 'C']
Dequeue:  A
peek:  B
isEmpty:  False
size:  2
```


## **3. Kesimpulan**

Queue adalah struktur data yang bekerja menggunakan prinsip **FIFO (First In, First Out)**, yaitu elemen yang pertama masuk akan menjadi elemen pertama yang dikeluarkan.
Pada Python, queue dapat dibuat menggunakan list dengan operasi seperti:

* menambah elemen ke belakang (*enqueue*)
* menghapus elemen dari depan (*dequeue*)
* melihat elemen terdepan (*peek*)
* memeriksa kondisi kosong
* mengetahui jumlah elemen yang tersisa

!
