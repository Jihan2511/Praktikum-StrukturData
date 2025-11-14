PERTEMUAN 1

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

  # Python

2. Penjelasan
   A) # stack and stack operations
     stack = []
     > Baris ini digunakan untuk membuat sebuah stack kosong. Stack disimpan dalam bentuk list karena Python bisa memakai         list untuk menampung data secara berurutan.
   B)# Push
      stack.append('A')
      stack.append('B')
      stack.append('C')
      print("Stack: ", stack)
     > Proses push, yaitu memasukkan data ke dalam stack. Fungsi append() menambahkan elemen di posisi paling akhir. Secara       berturut-turut data A, B, dan C dimasukkan, Setelah ketiga perintah ini dijalankan, isi stack menjadi:

      ['A', 'B', 'C']

      Output:

      Stack:  ['A', 'B', 'C']

   C) # Pop
      element = stack.pop()
      print("pop: ", element)
     > Fungsi pop() yaitu untuk menghapus data paling atas sekaligus mengembalikan nilainya. Karena C adalah elemen               terakhir yang dimasukkan, maka C-lah yang akan dikeluarkan.

   D) # Peek
      topElement = stack[-1]
      print("peek: ", topElement)
     > Peek untuk melihat data teratas tanpa menghapus
     > stack[-1] digunakan untuk mengetahui elemen yang berada di bagian paling atas. Setelah C dihapus, elemen teratas            berubah menjadi 'B'.
   





