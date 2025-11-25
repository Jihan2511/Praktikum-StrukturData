# Implementasi Linked List pada Python


Kode ini berisi implementasi struktur data Linked List sederhana menggunakan Python. Setiap elemen disimpan dalam sebuah node yang terdiri dari data dan penunjuk ke node berikutnya. Struktur ini memungkinkan penambahan dan penghapusan elemen secara dinamis tanpa harus menggeser keseluruhan data seperti pada array.

## Fitur

* Menambah data di awal list (`insert_at_first`)
* Menambah data di akhir list (`insert_at_last`)
* Menyisipkan data di posisi tertentu (`insert_at`)
* Menghapus elemen pertama (`remove_first`)
* Menghapus elemen terakhir (`remove_last`)
* Menghapus elemen berdasarkan index (`remove_at`)
* Menampilkan seluruh isi list (`print`)
* Menghitung jumlah elemen (`length`)


## Penjelasan Class pada Python

### Pengertian Class

Class adalah kerangka untuk membuat objek. Di dalamnya terdapat atribut yang menyimpan data dan method yang berisi perilaku. Dengan class, objek dapat dibuat berulang dengan struktur dan fungsi yang sama.


## Penjelasan Persintaks

### Class Node

```python
class Node:
    def __init__(self, data=None, pointer=None):
        self.data = data
        self.next = pointer
```

`Node` merupakan unit dasar dalam linked list.
Bagian `data` menyimpan nilai, sedangkan `next` menunjuk ke node berikutnya.


### Class LinkedList

```python
class LinkedList:
    def __init__(self):
        self.head = None
```

`LinkedList` bertindak sebagai wadah utama.
Variabel `head` menyimpan node pertama dan bernilai None ketika list masih kosong.


### Fungsi `insert_at_first`

```python
def insert_at_first(self, data):
    node = Node(data, self.head)
    self.head = node
```

Menambah elemen di awal list.
Node baru diarahkan ke head lama, lalu head dipindahkan ke node tersebut.


### Fungsi `insert_at_last`

```python
def insert_at_last(self, data):
    if self.head is None:
        self.head = Node(data)
    else:
        node_sekarang = self.head
        while node_sekarang.next:
            node_sekarang = node_sekarang.next

        node = Node(data)
        node_sekarang.next = node
```

Menambah elemen di akhir.
Jika list kosong, nilai baru langsung menjadi head.
Jika tidak, dilakukan penelusuran hingga node terakhir sebelum menambahkan node baru.


### Fungsi `insert_at`

```python
def insert_at(self, index, data):
    if index < 0 or index > self.length() - 1:
        print("index tidak valid!")
    elif index == 0:
        self.insert_at_first(data)
    else:
        urutan = 0
        node_sekarang = self.head
        
        while urutan < (index - 1):
            urutan += 1
            node_sekarang = node_sekarang.next

        node = Node(data, node_sekarang.next)
        node_sekarang.next = node
```

Menyisipkan elemen pada posisi tertentu.
Jika index nol, prosesnya sama seperti menambah di awal.
Jika index valid, pencarian dilakukan sampai node sebelum posisi yang ditentukan, lalu node baru ditempatkan di tengah.


### Fungsi `remove_first`

```python
def remove_first(self):
    if self.head is None:
        print("tidak ada data yang bisa dihapus")
    else:
        self.head = self.head.next
```

Menghapus elemen pertama dengan memindahkan head ke node berikutnya.


### Fungsi `remove_last`

```python
def remove_last(self):
    if self.head is None:
        print("tidak ada data yang bisa dihapus")
    elif self.head.next is None:
        self.head = None
    else:
        node_sebelumnya = None
        node_sekarang = self.head

        while node_sekarang.next:
            node_sebelumnya = node_sekarang
            node_sekarang = node_sekarang.next

        node_sebelumnya.next = None
```

Jika hanya ada satu elemen, head langsung dikosongkan.
Jika lebih dari satu, penelusuran dilakukan sampai node terakhir, lalu koneksi ke node sebelumnya diputus.


### Fungsi `remove_at`

```python
def remove_at(self, index):
    if index < 0 or index >= self.length():
        print("index invalid!")
    elif index == 0:
        self.remove_first()
    else:
        urutan = 0
        node_sekarang = self.head

        while urutan < index - 1:
            node_sekarang = node_sekarang.next
            urutan += 1

        node_sekarang.next = node_sekarang.next.next
```

Menghapus elemen berdasarkan index tertentu.
Untuk index nol, sama seperti menghapus elemen pertama.
Jika index valid, pointer node sebelumnya diarahkan ke node sesudah node yang dihapus.


### Fungsi `print`

```python
def print(self):
    if self.head is None:
        print("data kosong")
    else:
        text_print = ''
        node_sekarang = self.head

        while node_sekarang:
            text_print += str(node_sekarang.data) + " -> "
            node_sekarang = node_sekarang.next

        print(text_print)
```

Menampilkan isi linked list dari awal hingga akhir.
Jika kosong, muncul pesan bahwa tidak ada data.


### Fungsi `length`

```python
def length(self):
    urutan = 0
    data_sekarang = self.head

    while data_sekarang:
        data_sekarang = data_sekarang.next
        urutan += 1
    return urutan
```

Menghitung jumlah elemen dengan menelusuri node satu per satu dari head.


## Eksekusi Program

```python
LL = LinkedList()

# insert
LL.insert_at_first("jeruk")
LL.insert_at_first("mangga")
LL.insert_at_first("manggis")
LL.insert_at_last("apel")
LL.insert_at(2, "anggur")

# remove
LL.remove_first()
LL.remove_last()
LL.remove_at(1)
LL.remove_at(1)

LL.print()
print(LL.length())
```


## Alur Proses

1. Linked list dibuat dalam keadaan kosong.
2. Data dimasukkan menggunakan fungsi insert, dengan beberapa ditempatkan di depan, di belakang, dan pada posisi tertentu.
3. Operasi penghapusan dilakukan untuk menghapus elemen pertama, terakhir, serta elemen pada index tertentu.
4. Setelah seluruh operasi, hanya satu elemen yang tersisa dalam list.


## Output Program

```
mangga -> 
1
```

Baris pertama merupakan hasil dari fungsi `print()`
Baris kedua adalah jumlah elemen yang dihitung melalui fungsi `length()`.

