# the dom
Saat Anda membuka halaman web di browser, HTML halaman dimuat dan ditampilkan secara visual di layar.
Untuk mencapai hal ini, browser membangun Document Object Model (DOM) dari halaman itu, yang merupakan model berorientasi objek dari struktur logisnya.
DOM dokumen HTML dapat direpresentasikan sebagai kumpulan kotak:

> lihat gambar 1.png

DOM mewakili dokumen sebagai struktur pohon tempat elemen HTML saling terkait di dalam pohon.
Node dapat memiliki node anak. Node pada tingkat pohon yang sama disebut saudara.
jQuery traversing adalah istilah yang digunakan untuk menggambarkan proses bergerak melalui DOM dan menemukan (memilih) elemen HTML berdasarkan hubungannya dengan elemen lainnya.

## DOM Traversal

Misalnya, pertimbangkan HTML yang diwakili oleh struktur berikut:

> lihat gambar 2.png

Elemen <html> adalah induk dari <body> dan leluhur dari semua yang ada di bawahnya.
Elemen <body> adalah induk dari elemen <h1> dan <a>.
Elemen <h1> dan <a> adalah elemen turunan dari elemen <body> dan turunan dari <html>.
Elemen <h1> dan <a> adalah saudara kandung (mereka berbagi orang tua yang sama).

```
Ringkasan
Seorang leluhur adalah orangtua, kakek nenek, kakek buyut, dan sebagainya.
Keturunan adalah anak, cucu, cicit, dan sebagainya.
Saudara kandung memiliki orangtua yang sama
```
> Memahami hubungan antara elemen-elemen DOM adalah penting untuk dapat melintasi DOM dengan benar.