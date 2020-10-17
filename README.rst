Makefile
=================================================================================

.. contents:: **Daftar Isi**

Syntax Dasar
---------------------------------------------------------------------------------

Syntax dasar adalah:

::

   target: prerequisities
   <TAB> recipe

*target* adalah nama fungsi dan *prerequisities* adalah yang mengikuti *target*. 
*Command*-nya disebut *recipe*. *Recipe* menggunakan *prerequisites* untuk membuat 
*target*. *target*, *prerequisites*, dan *recipe* membentuk sebuah *rule*. 

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

**Referensi**

- `Opensource: what is a Makefile and how does it work? <https://opensource.com/article/18/8/what-how-makefile>`_
