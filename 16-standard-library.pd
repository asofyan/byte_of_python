# Pustaka Standar 

Pustaka Standar Python berisi banyak sekali modul-modul yang bermanfaat dan merupakan bagian baku instalasi standar Python. Sangat penting bagi Anda untuk membiasakan diri dengan pustaka standar Python, mengingat banyak permasalahan yang bisa diselesaikan dengan cepat jika Anda sudah terbiasa dengan hal-hal yang bisa dilakukan oleh pustaka standar Python. 

Kita akan menjelajahi beberapa penggunaan modul yang umum dalam pustaka ini. Anda dapat memperoleh informasi lengkap dari modul-modul Pustaka Standar Python di dokumentasi yang dibundel bersama instalasi Python Anda di [ bagian 'Referensi Pustaka'](http://docs.python.org/py3k/library/index.html).

Mari kita lihat beberapa modul yang bermanfaat

Catatan

:   Jika Anda temukan topik di bab ini perlu pemahaman tingkat lanjut, Anda bisa abaikan bab ini. Bagaimanapun juga, saya rekomendasikan Anda untuk kembali ke bab ini jika Anda sudah merasa nyaman melakukan pemrograman dengan Python.

## modul sys 

Modul sys berisi fungsi-fungsi yang spesifik berkaitan dengan sistem. Kita telah melihat sebelumnya daftar `sys.argv` berisi argumen baris perintah.

Anggap kita ingin mengecek versi Python yang sedang kita gunakan, misalnya, untuk memastikan kita menggunakan paling tidak versi 3. Modul `sys` akan memberikan fungsi tersebut.

~~~
$ python3
>>> import sys
>>> sys.version_info
sys.version_info(major=3, minor=3, micro=0, releaselevel='final', serial=0)
>>> sys.version_info.major >= 3
True
~~~

Bagaimana Cara Kerjanya:

Modul `sys` memiliki tuple `version_info` yang memberikan informasi tentang versi yang digunakan. Isian pertama berisi versi besar (_major version_). Kita dapat mengecek ini, sebagai contoh, untuk memastikan program hanya berjalan di bawah Python versi 3.0.

Simpan dengan nama `versioncheck.py`:

~~~python
import sys, warnings
if sys.version_info.major < 3:
    warnings.warn("Butuh Python 3.0 untuk menjalankan program ini",
        RuntimeWarning)
else:
    print('Program dijalankan secara normal')
~~~

Keluaran:

~~~
$ python2.7 versioncheck.py
versioncheck.py:6: RuntimeWarning: Butuh Python 3.0 untuk menjalankan program ini
  RuntimeWarning)

$ python3 versioncheck.py
Program dijalankan secara normal
~~~

Bagaimana Cara Kerjanya:

Kita menggunakan modul dari pustaka standar dengan nama `warnings` yang digunakan untuk menampilkan pesan kesalahan kepada pengguna. Jika versi Python yang digunakan kurang dari 3, kita akan tampilkan pesan kesalahan terkait. 

## Modul penyimpan pesan (_logging_) 

Bagaimana jika Anda ingin menyimpan pesan _debugging_ atau pesan penting dari program dan ingin disimpan di suatu tempat sehingga Anda dapat mengecek apakah program berjalan sebagaimana yang Anda harapkan? Bagaimana "menyimpan pesan-pesan ini di suatu tempat"? Ini dapat dicapai dengan menggunakan modul _logging_.

Simpan sebagai `gunakan_logging.py`:

~~~python
import os, platform, logging

if platform.platform().startswith('Windows'):
    berkas_logging = os.path.join(os.getenv('HOMEDRIVE'), os.getenv('HOMEPATH'), 'test.log')
else:
    berkas_logging = os.path.join(os.getenv('HOME'), 'test.log')

print("Logging ke", berkas_logging)

logging.basicConfig(
    level=logging.DEBUG,
    format='%(asctime)s : %(levelname)s : %(message)s',
    filename = logging_file,
    filemode = 'w',
)

logging.debug("Memulai program")
logging.info("Mengerjakan sesuatu")
logging.warning("Matikan sekarang")
~~~

Keluaran:

~~~
$ python3 gunakan_logging.py
Logging ke C:\Users\swaroop\test.log
~~~

Jika kita memeriksa isi dari `test.log`, akan terlihat seperti ini:

~~~
2012-10-26 16:52:41,339 : DEBUG : Memulai program 
2012-10-26 16:52:41,339 : INFO : Mengerjakan sesuatu
2012-10-26 16:52:41,339 : WARNING : Matikan sekarang
~~~

Bagaimana Cara Kerjanya:

Kita menggunakan tiga modul dari pustaka standar - modul `os` untuk interaksi dengan sistem operasi, modul `platform` untuk mencari informasi tentang platform - sistem operasi dan modul `logging` untuk menyimpan pesan dan informasi.

Pertama, kita cek sistem operasi apa yang kita gunakan dengan mencatat string kembalian dari fungsi `platform.platform()` (untuk informasi lebih lanjut, jalankan `import platforml help(platform)). Jika Windows, kita cari tahu _drive_ (bagian dari _harddisk_ yang digunakan), mencari folder rumah dan nama berkas tempat kita menyimpan informasi. Dengan menyatukan ketiga informasi tersebut bersama-sama, kita akan mendapatkan lokasi lengkap dari berkas. Untuk platform lain, kita hanya perlu tahu folder rumah dari pengguna yang bersangkutan, dan kita akan mendapatkan lokasi lengkap dari berkas yang dituju.

Kita gunakan fungsi `os.path.join()` untuk menyatukan ketiga hal di atas bersamaan. Alasan penggunaan fungsi khusus untuk menyatukan string tersebut bersama-sama, sebab fungsi ini akan memastikan lokasi lengkapnya (separator/pemisah antar folder) sesuai dengan format yang diharapkan oleh sistem operasi. 

Kita konfigurasikan modul `logging` untuk menuliskan seluruh pesan dalam format khusus yang telah kita tentukan sebelumnya.

Terakhir, kita dapat menuliskan pesan hanya untuk debugging, informasi atau pesan kesalahan, bahkan pesan kesalahan yang bersifat kritis. Sekali program berjalan, kita dapat melihat berkas ini dan kita tahu apa yang terjadi di dalam program, meskipun tidak ada informasi yang ditampilkan di depan pengguna langsung.

## Seri Modul Mingguan 

Ada lebih banyak pustaka standar yang bisa dieksplorasi seperti [debugging](http://docs.python.org/py3k/library/pdb.html), [penanganan pilihan baris perintah](http://docs.python.org/py3k/library/argparse.html), [ekspresi reguler](http://docs.python.org/py3k/library/re.html) dan lain-lain.

Cara terbaik untuk mengeksplorasi pustaka standar lebih lanjut adalah dengan membaca seri terbaik dari Doug Hellmann [Modul Mingguan Python](http://www.doughellmann.com/projects/PyMOTW/) atau langsung membaca [Dokumentasi Python](http://docs.python.org/py3k/).

## Ringkasan 

Kita telah menjelajahi beberapa fungsi dari banyak modul yang ada dalam Pustaka Standar Python. Sangat dianjurkan untuk menelusuri lebih lanjut lewat [Pustaka Standar Python](http://docs.python.org/py3k/library/index.html) untuk mengetahui modul-modul apa yang tersedia. 

Berikutnya, kita akan membahas berbagai macam aspek dari Python yang akan membuat tur Python kita lebih *lengkap*.
