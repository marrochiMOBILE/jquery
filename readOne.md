# What is jQuery ?


jQuery adalah pustaka JavaScript yang cepat, kecil, dan kaya fitur.
Itu membuat hal-hal seperti traversal dan manipulasi dokumen HTML, penanganan acara, dan animasi menjadi lebih mudah.

Semua kekuatan jQuery diakses melalui JavaScript, jadi memiliki pemahaman yang kuat tentang JavaScript sangat penting untuk memahami, menyusun, dan men-debug kode Anda.

> jquery = library.js


Pertama, mari kita lihat contoh manipulasi HTML dengan JavaScript.
Untuk mendapatkan elemen dengan id = "start" dan mengubah html menjadi "Go" kita perlu melakukan hal berikut:

```javascript
var el = document.getElementById("start");
el.innerHTML = "Go";
```


Untuk melakukan manipulasi yang sama dengan jQuery, kita hanya perlu satu baris kode:
```javascript
$("#start").html("Go");
```

Anda akan belajar tentang sintaks baru dalam pelajaran yang akan datang, tetapi seperti yang Anda lihat, kodenya jauh lebih pendek dan lebih mudah dipahami.

> Keuntungan besar lain dari jQuery adalah Anda tidak perlu khawatir tentang dukungan browser, kode Anda akan berjalan persis sama di semua browser utama, termasuk Internet Explorer 6!

## Getting Started

Anda dapat mengunduh salinan perpustakaan jQuery dari www.jquery.com, atau, sebagai alternatif, Anda dapat memasukkannya dari CDN (Content Delivery Network), seperti Google atau Microsoft.
Kami akan menggunakan CDN dari situs web jQuery resmi.
Untuk mulai menggunakan jQuery, pertama-tama kita harus menambahkannya ke kepala dokumen HTML menggunakan tag skrip:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
    </head>
    <body>
    </body>
</html>
```

> jQuery adalah perpustakaan JavaScript, sehingga memiliki ekstensi file .js

Ini adalah praktik yang baik untuk menunggu dokumen HTML dimuat sepenuhnya dan siap sebelum bekerja dengannya.
Untuk itu kami menggunakan acara siap dari objek dokumen:

```javascript
$(document).ready(function() {
   // jQuery code goes here
});
```

$ Digunakan untuk mengakses jQuery. Dari sini, kode mengakses objek dokumen dan menentukan fungsi yang akan dipanggil ketika acara siap dokumen dipecat.
Ini mencegah kode jQuery dari menjalankan sebelum dokumen selesai memuat.
Karena kode di atas digunakan di hampir semua kasus ketika menggunakan jQuery, ada jalan pintas yang berguna untuk menulisnya:

```javascript
$(function() {
   // jQuery code goes here
});
```

> Kode ini melakukan tugas yang sama dengan kode yang lebih panjang di atas.


Sekarang, dengan memiliki pustaka jQuery di bagian kepala kami dan telah menentukan acara siap dokumen, kita dapat memulai manipulasi jQuery pertama kami! Mari kita ubah konten elemen div.


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
</head>
<body>
    
        <div id="star">Hello Word</div>


    <script>
        $(function(){
            $('#star').html('go..!!');
        });
    </script>
</body>
</html>
```


jQuery digunakan untuk memilih (meminta) elemen HTML dan melakukan "aksi" padanya.
Sintaks dasarnya adalah: $ ("selector"). Action ()
- $ mengakses jQuery.
- (selector) menemukan elemen HTML.
- action () kemudian dilakukan pada elemen.


#### example
```js
$("p").hide()  // hides all <p> elements
$(".demo").hide()  // hides all elements with class="demo"
$("#demo").hide()  // hides the element with id="demo"
```

## selector
Mari kita lihat semua penyeleksi jQuery.
Seperti yang Anda lihat dalam pelajaran sebelumnya, pemilih jQuery mulai dengan tanda dolar dan tanda kurung: $ ().
Pemilih paling dasar adalah pemilih elemen, yang memilih semua elemen berdasarkan nama elemen.

```js
$("div")  // selects all <div> elements
```

Berikutnya adalah pemilih id dan kelas, yang memilih elemen dengan id dan nama kelas mereka:

```js
$("#test") // select the element with the id="test"
$(".menu") //selects all elements with class="menu"
```


Anda juga dapat menggunakan sintaks berikut untuk penyeleksi:

```js
$("div.menu")  // all <div> elements with class="menu"

$("p:first")  // the first <p> element

$("p:last")

$("h1, p") // all <h1> and all <p> elements

$("div p") // all <p> elements that are descendants of a <div> element

$("div > p")

$("*")  // all elements of the DOM
```

