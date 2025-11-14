# Stack #

1. Kode Program
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

2. Penjelasan
   A) # stack and stack operations
     stack = []
     > Baris ini digunakan untuk membuat sebuah stack kosong. Stack disimpan dalam bentuk list karena Python bisa memakai list untuk menampung data secara berurutan.
   B)# Push
      stack.append('A')
      stack.append('B')
      stack.append('C')
      print("Stack: ", stack)
     > Proses push, yaitu memasukkan data ke dalam stack. Fungsi append() menambahkan elemen di posisi paling akhir. Secara berturut-turut data A, B, dan C dimasukkan, Setelah ketiga perintah ini dijalankan, isi stack menjadi:
      ['A', 'B', 'C']
      Output:
      Stack:  ['A', 'B', 'C']
   C) # Pop
      element = stack.pop()
      print("pop: ", element)
     > Fungsi pop() yaitu untuk menghapus data paling atas sekaligus mengembalikan nilainya. Karena C adalah elemen  terakhir yang dimasukkan, maka C-lah yang akan dikeluarkan.
      Output:
      Pop: C
   D) # Peek
      topElement = stack[-1]
      print("peek: ", topElement)
     > Peek untuk melihat data teratas tanpa menghapus
     > stack[-1] digunakan untuk mengetahui elemen yang berada di bagian paling atas. Setelah C dihapus, elemen teratas berubah menjadi 'B'.
C) # isEmpty
        isEmpty = not bool(stack)
        print("isEmpty: ", isEmpty)
    >Kode ini mengecek apakah stack kosong atau tidak. Jika stack berisi elemen, bool(stack) akan menghasilkan True. Jika kosong maka False. Karena stack masih berisi dua elemen (A dan B), maka hasilnya False.
      Output:

      isEmpty:  False
D) # Size
      print("size: ", len(stack))
    >Baris terakhir menampilkan berapa banyak elemen yang masih ada di dalam stack dengan menggunakan fungsi len().Saat ini ada dua elemen, jadi ukuran stack adalah 2.
   Output:
    Size:  2

3. Hasil Eksekusi
  Queue:  ['A', 'B', 'C']
  Dequeue:  A
  Peek:  B
  isEmpty:  False
  Size:  2

4. Kesimpulan
    Stack adalah struktur data yang bekerja dengan konsep LIFO (Last In, First Out), di mana elemen terakhir yang dimasukkan akan menjadi elemen pertama yang dikeluarkan. Di Python, stack dapat dibuat menggunakan list dengan memanfaatkan operasi append() untuk menambah data dan pop() untuk mengambil data dari bagian atas. Stack juga memungkinkan pengecekan elemen teratas (peek), mengecek apakah kosong, serta mengetahui jumlah elemennya.
   
