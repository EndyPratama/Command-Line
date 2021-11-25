# Command-Line

## Create Files
The Command Line is an important tool for software development.
By using the command, you can run many programs on your computer.
Let's learn the fundamental UNIX commands required for development in this lesson!


The Command Line is a tool for interacting with a computer using only text (also known as a text interface) rather than other methods such as clicking and scrolling. Let's because this is very useful for developing websites and applications! The UNIX command is a type of command used on Linux and macOS.

As in the image below, you can give instructions to the computer by typing commands into the terminal.
Let's look at the types of commands on the next slide.
There is no need to write $ because it is a symbol to indicate you can start typing commands.

First, let's look at the command to create a new file, the touch command. You can create an empty file by typing touch file_name and running it.

``` bash
$ touch upstart.txt
```

You can run a command by pressing the Enter key after typing it.

## A File

To display the contents of a file, use the cat command. To use the cat command, type cat file_name.

If you specify a non-existent file using the cat command, it will get an error, because the command is invalid.

The command line also has a completion feature that is useful for shortening typing. If you press the Tab key while typing a file name or folder name, the extension of the name will be filled in automatically. By using the tab key, it can not only increase efficiency but also prevent typos.

## Create a Directory

You can create a new directory using the command.
A directory also known as a folder.
To create a directory, use the mkdir command as follows: mkdir directory_name.

## Switch Between Directors

When using the command line, it is important to be familiar with the file structure. In the example structure below, we have many branches. For example, the home directory contains files such as about.txt and other directories such as the html directory.
```
House
  |-- html
  |     |-- index.html
  |
  |-- about.txt
  |-- readme.md
```
On the command line, the directory you are working in is the current directory. For example, touch file.txt will create a file named file.txt in the current directory.
If you want to create a new file in the html directory, you can do so by changing the current directory to the html directory.

You can use the cd command to move to another directory. By typing cd directory_name, it can move to a specific directory.

``` bash
$cd html
html $
```

The current directory is shown to the left of $.

You will get an error if the directory doesn't exist with the cd command. Also, keep in mind that you can only specify directory names, not file names.

## Checking Current Directory

In the computer file structure, there is a root directory at the top. The root directory is represented by /.

On the command line, it is very important to know the directory in which you are working. There is a command called pwd to check that.
When you run the pwd command as shown below, all directories from the root directory to the current directory will be displayed.

## Displays List of Files

When moving between directories, it will be easier if we can see a list of files and directories in the current directory.
To do this, you can use the ls command as in the example below.

``` bash
$ ls
```

Note that the ls command will only display directories and files that are direct children of the current directory.

## Parent Directory

We've learned how to use the cd command, but we don't know how to move to the parent directory.
If you want to move to the parent directory, you can use special symbols .., like cd ...

## Initial Directory

If you run cd without specifying a directory, then you can move to what is called the home directory.

The starting directory refers to the base directory for the user. Because this is important, moving to the starting directory is made easy. /home is the starting directory for this lesson.
```
home
  |-- html
  |     |-- index.html
  |
  |-- about.txt
  |-- readme.md
```
## Move Files and Directories (mv -> move)

From here, we will learn how to perform various operations such as moving, copying, and deleting files with commands.

Let's start with the command to move a file.
To do this, we use the mv command.
By typing mv file_destination_moved_directory, you can move a file to the specified directory.

``` bash
$ mv about.txt html
```
```
home
  |-- html
  |     |-- index.html
  |     |-- about.txt
  |
  |-- readme.md
```
With the mv command, you can also move directories, not just files.
By typing mv directory_which_the_destination_directory was moved to, you can move all files and directories under that directory.


## Rename Files and Directories

The mv command, which we used to move previous files and directories, can also be used to rename a file.
You can rename a file by typing mv old_filename new_filename.

``` bash
$ cd html
html $ mv index.html home.html
```
```
home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |
  |-- readme.md
```
## Copy Files and Directories (cp -> copy)

Next, let's see how to copy files.
To do this, we can use the cp command.
You can copy a file by typing cp file_the_copied_new_file_name.

``` bash
$ cd html
html $ cp about.txt readme.txt
```
```
home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |     |-- readme.txt
  |
  |-- readme.md
```
With the cp command, you can also copy directories by adding the -r (Recursive copy) option, such as cp -r directory_the_new_directory_name copied.

If you try to copy a directory without adding the -r option, you will get an error and the command will not be executed.

``` bash
$ cp html php
```
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
```
## Delete Files and Directories (rm -> remove)
  
Next, let's see how to delete a file.
To do this, we can use the rm command, such as rm file_deleted.

``` bash
$ cd html
html $ rm readme.txt
```
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
```
You can also delete a directory by adding the -r option to the rm command, such as rm -r deleted_directory.
Like the cp command, you will get an error if you forget to add -r.

``` bash
$ rm -r php
```
```
home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |
  |-- readme.md
```
[Indonesia]

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
```
home
  |-- html
  |     |-- index.html
  |
  |-- about.txt
  |-- readme.md
``` 
 
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
```
home
  |-- html
  |     |-- index.html
  |
  |-- about.txt
  |-- readme.md
```
## Memindahkan File dan Direktori (mv -> move)

Dari sini, kita akan mempelajari bagaimana menjalankan berbagai operasi seperti memindahkan, menyalin, dan menghapus file dengan command.

Mari kita mulai dengan command untuk memindahkan sebuah file.
Untuk melakukan ini, kita gunakan command mv.
Dengan mengetik mv file_yang_dipindahkan direktori_tujuan, kalian dapat memindahkan sebuah file ke direktori yang dispesifikasikan.

```bash
$ mv about.txt html
```
```
home
  |-- html
  |     |-- index.html
  |     |-- about.txt
  |
  |-- readme.md
```
Dengan command mv, Anda juga dapat memindahkan direktori, bukan hanya file.
Dengan mengetik mv direktori_yang_dipindahkan direktori_tujuan, Anda dapat memindahkan semua file dan direktori di bawah direktori tersebut.


## Mengubah Nama File dan Direktori

Command mv, yang kita gunakan untuk memindahkan file dan direktori sebelumnya, dapat juga digunakan untuk menamai ulang sebuah file.
Anda dapat menamai ulang sebuah file dengan mengetik mv nama_file_lama nama_file_baru.

```bash
$ cd html
html $ mv index.html home.html
```
```
home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |
  |-- readme.md
```
## Menyalin File dan Direktori (cp -> copy)

Selanjutnya, mari kita lihat bagaimana menyalin file-file.
Untuk melakukannya, kita dapat menggunakan command cp.
Kalian dapat menyalin sebuah file dengan mengetik cp file_yang_disalin nama_file_baru.

```bash
$ cd html
html $ cp about.txt readme.txt
```
```
home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |     |-- readme.txt
  |
  |-- readme.md
```
Dengan command cp, Anda juga dapat menyalin direktori dengan menambahkan pilihan -r (Recursive copy), seperti cp -r directory_yang_disalin nama_directori_baru.

Jika Anda mencoba untuk menyalin sebuah direktori tanpa menambahkan pilihan -r, Anda akan mendapat sebuah error dan command tidak akan dijalankan.

```bash
$ cp html php
```
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
```
## Menghapus File dan Direktori (rm -> remove)
  
Selanjutnya, mari kita lihat bagaimana menghapus sebuah file.
Untuk melakukannya, kita dapat menggunakan command rm, seperti rm file_yang_dihapus.

```bash
$ cd html
html $ rm readme.txt
```
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
```
Anda juga dapat menghapus sebuah direktori dengan menambahkan pilihan -r ke command rm, seperti rm -r direktori_yang_dihapus.
Seperti command cp, Anda akan mendapat error jika lupa menambahkan -r.

```bash
$ rm -r php
```
```
home
  |-- html
  |     |-- home.html
  |     |-- about.txt
  |
  |-- readme.md
```







