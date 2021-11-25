# Command-Line

## Membuat File
Command Line adalah tool yang penting untuk pengembangan software.
Dengan menggunakan command, Kalian dapat menjalankan banyak program pada komputer kalian.
Mari mempelajari command UNIX yang fundamental yang diperlukan untuk pengembangan pada pelajaran ini!


Command Line adalah tool untuk berinteraksi dengan komputer dengan hanya menggunakan text (juga dikenal sebagai text interface) daripada metode lain seperti klik dan scrolling. Mari kita pelajari karena ini sangat berguna untuk mengembangkan website dan aplikasi! Command UNIX adalah tipe command yang digunakan dalam Linux dan macOS.

Seperti pada gambar di bawah, kalian dapat memberikan instruksi pada komputer dengan mengetik command ke terminal.
Mari kita lihat jenis-jenis command pada slide berikutnya.
Tidak perlu menulis $ karena itu merupakan simbol untuk menandakan dimana kalian bisa mulai mengetik command.

Pertama-tama, mari kita lihat command untuk membuat file baru, command touch. Kalian dapat membuat file kosong dengan mengetik touch file_name dan menjalankannya.

```bash
$ touch beginner.txt
```

Kalian dapat menjalankan sebuah command dengan menekan tombol Enter setelah mengetiknya.

## Menampilkan Sebuah File

Untuk menampilkan konten dari sebuah file, gunakan command cat. Untuk menggunakan command cat, ketik cat file_name.

Jika kalian menentukan sebuah file yang tidak ada menggunakan command cat, maka akan mendapat sebuah error, karena command tidak sah.

Command line juga memiliki fitur completion (penyelesaian) yang berguna untuk mempersingkat pengetikan. Jika kalian menekan tombol Tab saat mengetik nama file atau nama folder, kepanjangan nama tersebut akan terisi otomatis. Dengan menggunakan tombol tab, maka tidak hanya dapat meningkatkan efisiensi namun juga mencegah salah ketik.

## Membuat Sebuah Direktori

Kalian dapat membuat direktori baru menggunakan command.
Sebuah direktori dikenal juga dengan istilah folder.
Untuk membuat sebuah direktori, gunakan command mkdir sebagai berikut: mkdir directory_name.

## Berpindah Antar Direktori

Saat menggunakan command line, penting untuk mengenal struktur file. Pada contoh struktur di bawah, kita mempunyai banyak cabang. Contohnya, direktori home berisi file-file seperti about.txt dan direktori lainnya seperti direktori html.

home
  |-- html
  |     |-- index.html
  |
  |-- about.txt
  |-- readme.md
  
 
Pada command line, direktori dimana kalian bekerja disebut direktori saat ini. Contohnya, touch file.txt akan membuat file yang bernama file.txt di dalam direktori saat ini.
Jika kalian ingin membuat file baru di dalam direktori html, kalian dapat melakukannya dengan mengganti direktori saat ini menjadi direktori html.

Kalian dapat menggunakan command cd untuk berpindah ke direktori lain. Dengan mengetik cd directory_name, maka dapat berpindah ke suatu direktori spesifik.

```bash
$ cd html
html $ 
```

Direktori saat ini ditampilkan di sebelah kiri $.

Kalian akan mendapat error jika menentukan direktori yang tidak ada dengan command cd. Selain itu, perlu diingat bahwa kalian hanya bisa menentukan nama direktori, bukan nama file.

## Memeriksa Direktori Saat Ini

Pada struktur file komputer, ada direktori root pada bagian atas. Direktori root direpresentasikan dengan /. 

Pada command line, sangat penting untuk mengetahui direktori dimana Anda bekerja. Ada command yang disebut pwd untuk mengecek itu.
Saat Anda menjalankan command pwd seperti pada gambar di bawah, semua direktori dari direktori root sampai direktori saat ini akan ditampilkan.

## Menampilkan Daftar File - File

Saat berpindah diantara direktori, akan lebih mudah jika kita dapat melihat daftar file dan direktori di dalam direktori saat ini.
Untuk melakukannya, maka kalian dapat menggunakan command ls seperti contoh di bawah.

```bash
$ ls
```

Perlu dicatat bahwa command ls hanya akan menampilkan direktori dan file yang merupakan anak langsung dari direktori saat ini.

## Direktori Induk

Kita sudah belajar bagaimana menggunakan command cd, namun kita belum tahu bagaimana cara berpindah ke direktori induk.
Jika kalian ingin berpindah ke direktori induk, maka dapat menggunakan simbol khusus .., seperti cd ...

## Direktory Awal

Jika kalian menjalankan cd tanpa menetapkan sebuah direktori, maka kalian dapat berpindah ke apa yang disebut direktori awal (home).

Direktori awal merujuk pada direktori dasar untuk pengguna. Karena hal ini penting, berpindah ke direktori awal dibuat mudah. /home adalah direktori awal untuk pelajaran ini.

home
  |-- html
  |     |-- index.html
  |
  |-- about.txt
  |-- readme.md
  
## Memindahkan File dan Direktori (mv -> move)

Dari sini, kita akan mempelajari bagaimana menjalankan berbagai operasi seperti memindahkan, menyalin, dan menghapus file dengan command.

Mari kita mulai dengan command untuk memindahkan sebuah file.
Untuk melakukan ini, kita gunakan command mv.
Dengan mengetik mv file_yang_dipindahkan direktori_tujuan, kalian dapat memindahkan sebuah file ke direktori yang dispesifikasikan.

```bash
$ mv about.txt html
```
home
  |-- html
  |     |-- index.html
  |     |-- about.txt
  |
  |-- readme.md
  
Dengan command mv, Anda juga dapat memindahkan direktori, bukan hanya file.
Dengan mengetik mv direktori_yang_dipindahkan direktori_tujuan, Anda dapat memindahkan semua file dan direktori di bawah direktori tersebut.


## Mengubah Nama File dan Direktori

Command mv, yang kita gunakan untuk memindahkan file dan direktori sebelumnya, dapat juga digunakan untuk menamai ulang sebuah file.
Anda dapat menamai ulang sebuah file dengan mengetik mv nama_file_lama nama_file_baru.

```bash
$ cd html
html $ mv index.html home.html
```

home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |
  |-- readme.md

## Menyalin File dan Direktori (cp -> copy)

Selanjutnya, mari kita lihat bagaimana menyalin file-file.
Untuk melakukannya, kita dapat menggunakan command cp.
Kalian dapat menyalin sebuah file dengan mengetik cp file_yang_disalin nama_file_baru.

```bash
$ cd html
html $ cp about.txt readme.txt
```

home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |     |-- readme.txt
  |
  |-- readme.md

Dengan command cp, Anda juga dapat menyalin direktori dengan menambahkan pilihan -r (Recursive copy), seperti cp -r directory_yang_disalin nama_directori_baru.

Jika Anda mencoba untuk menyalin sebuah direktori tanpa menambahkan pilihan -r, Anda akan mendapat sebuah error dan command tidak akan dijalankan.

```bash
$ cp html php
```

home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |     |-- readme.txt
  |
  |-- php
  |     |-- home.html
  |     |-- about.txt
  |     |-- readme.txt
  |
  |-- readme.md
  
## Menghapus File dan Direktori (rm -> remove)
  
Selanjutnya, mari kita lihat bagaimana menghapus sebuah file.
Untuk melakukannya, kita dapat menggunakan command rm, seperti rm file_yang_dihapus.

```bash
$ cd html
html $ rm readme.txt
```

home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |
  |-- php
  |     |-- home.html
  |     |-- about.txt
  |     |-- readme.txt
  |
  |-- readme.md

Anda juga dapat menghapus sebuah direktori dengan menambahkan pilihan -r ke command rm, seperti rm -r direktori_yang_dihapus.
Seperti command cp, Anda akan mendapat error jika lupa menambahkan -r.

```bash
$ rm -r php
```

home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |
  |-- readme.md









