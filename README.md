# A Byte of Python

## Instalasi 

Pastikan Python (&gt;= 2.7) telah terinstal.

Instal Pandoc dari <http://johnmacfarlane.net/pandoc/installing.html>

Instal `pdflatex` dari <http://www.tug.org/texlive/>.
Mohon dicatat bahwa pengguna Mac dapat menginstal `MacTex.pkg` dari <http://www.tug.org/mactex/2012/>.

Instal `pip` jika belum ada di komputer Anda:

    sudo sh -c "curl -k -O https://raw.github.com/pypa/pip/master/contrib/get-pip.py && python get-pip.py && rm get-pip.py"


Instal pustaka Python yang dibutuhkan:

    sudo pip install -r requirements.txt


Konversi berkas sumber ke dalam format HTML:

    fab html

Konversi berkas sumber ke dalam format PDF:

    fab pdf

Konversi berkas sumber ke dalam format EPUB (ebook):

    fab epub

## Mengedit

Jika Anda menggunakan editor VIM, Anda bisa instal plugin [vim-pandoc](https://github.com/vim-pandoc/vim-pandoc). Bagaimanapun juga ada kelemahannya - untuk bab yang panjang, plugin tersebut membuat vim menjadi pelan, jadi saya hanya mengeditnya dalam mode teks murni (`:set ft=`), tepi saat review saya menggunakan `pandoc` (`:set ft=pandoc`)

## Terjemahan

Terjemahan Bahasa Indonesia ini disusun oleh Ahmad Sofyan asofyan (a) gmail.com
