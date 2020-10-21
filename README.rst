Makefile
=================================================================================

.. contents:: **Daftar Isi**

Manual Book
---------------------------------------------------------------------------------

- `GNU Make (PDF) <https://www.gnu.org/software/make/manual/make.pdf>`_
- `GNU Make (Web) <https://www.gnu.org/software/make/manual/make.html>`_

Install Make
---------------------------------------------------------------------------------

**Windows**

- `Download and Install Make <http://gnuwin32.sourceforge.net/packages/make.htm>`_
- add Make to path

Syntax Dasar
---------------------------------------------------------------------------------

Syntax dasar adalah:

::

   target: prerequisities
   <TAB> recipe

*target* adalah nama fungsi dan *prerequisities* adalah yang mengikuti *target*. 
*Command*-nya disebut *recipe*. *Recipe* menggunakan *prerequisites* untuk membuat 
*target*. *target*, *prerequisites*, dan *recipe* membentuk sebuah *rule*. 

Contoh Penggunaan
---------------------------------------------------------------------------------

Single Command
*********************************************************************************

Sebagai contoh, buatlah sebuah file tanpa *extension* dengan nama Makefile. 

::

   say_hello:
        echo "Hello World"

Jalankan di terminal dengan perintah *make*, hasilnya:

::

   $ make
   echo "Hello Wolrd"
   Hello World

Hasil di atas menampilkan *command* dan hasilnya. *Command* dapat disembunyikan dengan 
menambahkan **@** di depan **echo**. 

::

   say_hello:
      @echo "Hello World"

Hasilnya adalah:

::

   $ make
   Hello World

Lebih dari Satu Commands
*********************************************************************************

Apabila terdapat lebih dari 1 *target*, dengan menggunakan *syntax* di bawah ini 
maka hanya *target* yang ditulis pertama kali yang akan dijalankan. 

::

    cmd01:
        @echo "command ke-1"

    cmd02:
        @echo "command ke-2"

Agar semua *command* dijalankan maka perlu ditambah *all* sebagai berikut:

::

    all: cmd01 cmd02

    cmd01:
        @echo "command ke-1"

    cmd02:
        @echo "command ke-2"


Tambahkan juga spesial *phony target* untuk mendefinisikan bahwa semua *target*
adalah bukan *files*. Ini agar tidak membuat bingung *make* dalam menjalankan
*target*-nya. Berikut ini adalah contoh penulisan *phony*:

::

    .PHONY: all cmd01 cmd02

    all: cmd01 cmd02

    cmd01:
        @echo "command ke-1"

    cmd02:
        @echo "command ke-2"

**Referensi**

- `Opensource: what is a Makefile and how does it work? <https://opensource.com/article/18/8/what-how-makefile>`_
