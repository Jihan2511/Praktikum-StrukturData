#  **Implementasi Linked List Pada Python**

## **1. Kelas Node**

```python
class Node:
    def __init__(self, data=None, pointer=None):
        self.data = data
        self.next = pointer
```

### **Penjelasan Sintaks**

* `class Node:`
  Mendefinisikan struktur dasar sebuah node. Setiap node menyimpan data dan alamat node berikutnya.

* `def __init__(self, data=None, pointer=None):`
  Konstruktor yang dipanggil setiap kali membuat objek Node baru.

* `self.data = data`
  Menyimpan nilai yang diberikan ke node.

* `self.next = pointer`
  Menyimpan referensi menuju node berikutnya. Default-nya `None`.


## **2. Kelas LinkedList**

```python
class LinkedList:
    def __init__(self):
        self.head = None
```

### **Penjelasan Sintaks**

* `class LinkedList:`
  Sebuah struktur data yang terdiri dari rangkaian node.

* `self.head = None`
  Menentukan bahwa linked list dimulai dari posisi kosong, karena belum ada node pertama.


## **3. insert_at_first()**

```python
def insert_at_first(self, data):
    node = Node(data, self.head)
    self.head = node
```

### **Penjelasan Sintaks**

* `node = Node(data, self.head)`
  Membuat node baru yang langsung menunjuk ke node yang sebelumnya menjadi head.

* `self.head = node`
  Menjadikan node baru sebagai elemen paling depan.


## **4. insert_at_last()**

```python
def insert_at_last(self, data):
    if self.head is None:
        self.head = Node(data)
    else:
        node_sekarang = self.head
        while node_sekarang.next:
            node_sekarang = node_sekarang.next
        node_sekarang.next = Node(data)
```

### **Penjelasan Sintaks**

* `if self.head is None:`
  Mengecek apakah list masih kosong.

* `self.head = Node(data)`
  Jika kosong, data langsung menjadi elemen pertama.

* `node_sekarang = self.head`
  Jika tidak kosong, traversal dimulai dari head.

* `while node_sekarang.next:`
  Berulang sampai mencapai node terakhir.

* `node_sekarang.next = Node(data)`
  Menyambungkan node baru di bagian paling akhir.


## **5. insert_at(index, data)**

```python
def insert_at(self, index, data):
    if index < 0 or index > self.length():
        print("indeks tidak valid")
        return
    
    if index == 0:
        self.insert_at_first(data)
        return
    
    urutan = 0
    node_sekarang = self.head
    while urutan < index - 1 and node_sekarang:
        node_sekarang = node_sekarang.next
        urutan += 1

    node_baru = Node(data, node_sekarang.next)
    node_sekarang.next = node_baru
```

### **Penjelasan Sintaks**

* `if index < 0 or index > self.length():`
  Menolak index yang tidak masuk akal.

* `if index == 0:`
  Jika indeks 0, proses sama seperti insert di awal.

* `while urutan < index - 1:`
  Traversal dilakukan sampai posisi tepat sebelum index yang dituju.

* `node_baru = Node(data, node_sekarang.next)`
  Node baru menunjuk ke node yang sebelumnya berada di posisi tersebut.

* `node_sekarang.next = node_baru`
  Node sebelum index kini menunjuk ke node baru.


## **6. remove_first()**

```python
def remove_first(self):
    if self.head is None:
        print("tidak ada data yang bisa dihapus")
    else:
        self.head = self.head.next
```

### **Penjelasan Sintaks**

* `self.head = self.head.next`
  Head lama dilewati, sehingga elemen pertama terhapus secara otomatis.


## **7. remove_last()**

```python
def remove_last(self):
    if self.head is None:
        print("tidak ada data yang bisa dihapus")
        return
    
    if self.head.next is None:
        self.head = None
        return

    node_sekarang = self.head
    
    while node_sekarang.next.next:
        node_sekarang = node_sekarang.next
    
    node_sekarang.next = None
```

### **Penjelasan Sintaks**

* `if self.head.next is None:`
  Kasus khusus: hanya satu data → langsung hapus.

* `while node_sekarang.next.next:`
  Berhenti di node sebelum node terakhir.

* `node_sekarang.next = None`
  Node terakhir dilepas dari rantai.


## **8. remove_at(index)**

```python
def remove_at(self, index):
    if index < 0 or index >= self.length():
        print("index invalid")
        return
    
    if index == 0:
        self.remove_first()
        return
    
    urutan = 0
    node_sekarang = self.head
    
    while urutan < index - 1:
        node_sekarang = node_sekarang.next
        urutan += 1
    
    if node_sekarang.next:
        node_sekarang.next = node_sekarang.next.next
```

### **Penjelasan Sintaks**

* Validasi batas indeks.

* Jika index = 0 → hapus elemen pertama.

* Traversal hingga node sebelum index.

* `node_sekarang.next = node_sekarang.next.next`
  Node pada index dilewati sehingga terhapus.


## **9. print()**

```python
def print(self):
    if self.head is None:
        print("data kosong")
    else:
        hasil = ""
        node = self.head
        while node:
            hasil += str(node.data) + " → "
            node = node.next
        print(hasil)
```

### **Penjelasan Sintaks**

* Traversal dari head.
* Setiap data ditambahkan ke string.
* Ditampilkan dalam satu baris.

---

## **10. length()**

```python
def length(self):
    count = 0
    node = self.head
    while node:
        count += 1
        node = node.next
    return count
```

### **Penjelasan Sintaks**

* Menghitung jumlah node dengan melakukan traversal sampai habis.


## **11. Bagian Pengujian Program**

```python
ll = LinkedList()

ll.insert_at_first("jeruk")
ll.insert_at_first("mangga")
ll.insert_at_first("manggis")
ll.insert_at_last("apel")
ll.insert_at(2, "anggur")

ll.remove_first()
ll.remove_last()
ll.remove_at(1)
ll.remove_at(1)

ll.print()
print(ll.length())
```

### **Penjelasan Sintaks**

* Membuat objek LinkedList.
* Melakukan beberapa operasi insert dan delete.
* Bagian akhir menampilkan isi list dan jumlah elemen.

