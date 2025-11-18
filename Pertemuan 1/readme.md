# *Stack*


## *1. Penjelasan*

### *A) Membuat Stack Kosong*

python
stack = []


> Baris ini membuat sebuah stack kosong. Stack disimpan dalam bentuk list karena list dapat digunakan untuk menampung data secara berurutan.


### *B) Push (Menambahkan Elemen ke Stack)*

python
stack.append('A')
stack.append('B')
stack.append('C')
print("Stack: ", stack)


> Operasi push menambahkan elemen ke posisi paling akhir. Data A, B, dan C dimasukkan secara berurutan sehingga isi stack menjadi:
>
> ['A', 'B', 'C']
>
> *Output:*
> Stack: ['A', 'B', 'C']


### *C) Pop (Menghapus Elemen Teratas)*

python
element = stack.pop()
print("pop: ", element)


> Fungsi pop() digunakan untuk menghapus dan mengambil elemen paling atas. Karena C adalah elemen yang terakhir masuk, maka C yang akan dikeluarkan.
>
> *Output:*
> Pop: C


### *D) Peek (Melihat Elemen Teratas Tanpa Menghapus)*

python
topElement = stack[-1]
print("peek: ", topElement)


> Peek digunakan untuk melihat elemen paling atas tanpa mengubah isi stack.
> Setelah C terhapus, elemen teratas menjadi 'B'.


### *E) isEmpty (Mengecek Apakah Stack Kosong)*

python
isEmpty = not bool(stack)
print("isEmpty: ", isEmpty)


> Kode ini memeriksa apakah stack kosong.
> bool(stack) bernilai *True* jika stack berisi data, dan *False* jika kosong.
> Karena stack masih berisi A dan B, maka hasilnya *False*.
>
> *Output:*
> isEmpty: False


### *F) Size (Menampilkan Jumlah Elemen)*

python
print("size: ", len(stack))


> Baris ini menampilkan ukuran stack dengan len().
> Saat ini masih ada dua elemen, yaitu A dan B.
>
> *Output:*
> Size: 2


## *2. Hasil Eksekusi*


Stack:  ['A', 'B', 'C']
Pop:  C
Peek:  B
isEmpty:  False
Size:  2



## *3. Kesimpulan*

Stack merupakan struktur data yang menggunakan metode *LIFO (Last In, First Out)*, yaitu elemen yang paling terakhir dimasukkan menjadi elemen pertama yang dikeluarkan. Pada Python, struktur stack dapat dibangun menggunakan list dengan bantuan fungsi append() untuk melakukan push dan pop() untuk melakukan penghapusan data. Stack juga memungkinkan pengguna melakukan pengecekan elemen teratas (peek), memeriksa apakah stack kosong, serta mengetahui jumlah elemen yang tersimpan.




# *Queue*


## *1. Penjelasan*

### *A) Membuat Queue Kosong*

python
queue = []


> Baris ini digunakan untuk membuat sebuah queue kosong. Queue disimpan dalam bentuk list karena Python dapat menampung data secara berurutan dan memudahkan penambahan elemen di belakang serta penghapusan di depan.


### *B) Enqueue (Menambahkan Elemen ke Queue)*

python
queue.append('A')
queue.append('B')
queue.append('C')
print("Queue: ", queue)


> Operasi enqueue menambahkan elemen ke bagian belakang antrian. Setelah memasukkan A, B, dan C, queue akan berisi:
>
> ['A', 'B', 'C']
>
> *Output:*
> Queue: ['A', 'B', 'C']


### *C) Dequeue (Menghapus Elemen dari Depan)*

python
element = queue.pop(0)
print("Dequeue: ", element)


> Fungsi pop(0) digunakan untuk menghapus elemen dari urutan paling depan. Karena A masuk pertama, maka A yang pertama dikeluarkan.
>
> *Output:*
> Dequeue: A


### *D) Peek (Melihat Elemen Depan Tanpa Menghapus)*

python
frontElement = queue[0]
print("peek: ", frontElement)


> Peek digunakan untuk melihat elemen paling depan tanpa menghapusnya. Setelah A dihapus, posisi terdepan diisi oleh B.
>
> *Output:*
> peek: B


### *E) isEmpty (Memeriksa Apakah Queue Kosong)*

python
isEmpty = not bool(queue)
print("isEmpty: ", isEmpty)


> bool(queue) akan bernilai True jika masih ada elemen. Karena queue masih berisi dua elemen (B dan C), maka hasilnya False.
>
> *Output:*
> isEmpty: False


### *F) Size (Menampilkan Jumlah Elemen dalam Queue)*

python
print("size: ", len(queue))


> Fungsi len() menghitung jumlah elemen dalam queue. Setelah dequeue, tersisa dua elemen yaitu B dan C.
>
> *Output:*
> size: 2


## *2. Hasil Eksekusi*


Queue:  ['A', 'B', 'C']
Dequeue:  A
peek:  B
isEmpty:  False
size:  2



## *3. Kesimpulan*

Queue adalah struktur data yang bekerja menggunakan prinsip *FIFO (First In, First Out)*, yaitu elemen yang pertama masuk akan menjadi elemen pertama yang dikeluarkan. Pada Python, queue dapat dibuat menggunakan list dengan memanfaatkan append() untuk memasukkan data ke bagian belakang dan pop(0) untuk mengeluarkan elemen dari bagian depan. Selain itu, queue mendukung pengecekan elemen terdepan (peek), memeriksa kondisi kosong, serta mengetahui jumlah elemen yang tersisa.
