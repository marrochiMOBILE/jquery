# the event object

> lihat gambar 2.png

Setiap fungsi penanganan acara dapat menerima objek acara, yang berisi properti dan metode yang terkait dengan acara:
pageX, pageY posisi mouse (koordinat X & Y) pada saat peristiwa itu terjadi, relatif ke kiri atas halaman.
ketik jenis acara (mis. "klik").
dimana tombol atau tombol yang ditekan.
data data apa pun yang dilewatkan saat acara terikat.
menargetkan elemen DOM yang memprakarsai acara.
preventDefault () mencegah aksi default acara (mis., mengikuti tautan).
stopPropagation () Hentikan acara agar tidak menggelembung ke elemen lain.

> Anda dapat melihat kursus JavaScript kami untuk informasi lebih lanjut tentang properti acara.


Misalnya, mari kita menangani acara klik pada elemen <a> dan mencegahnya mengikuti tautan yang disediakan dalam atribut href:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
    </style>
</head>
<body>

    <a href="https://www.twitter.com">Click me</a>
    
    <script>
$(function() {
    $( "a" ).click(function(event) {
        alert(event.pageX);
        event.preventDefault();
    });
});
    </script>
</body>
</html>
```
Kode di atas mengingatkan posisi mouse pada saat klik dan mencegah mengikuti tautan.
> Seperti yang Anda lihat, objek acara dilewatkan ke fungsi event handler sebagai argumen.

## Trigger Events

Kami juga dapat memicu acara secara terprogram menggunakan metode trigger (). Misalnya, Anda dapat memicu acara klik tanpa pengguna benar-benar mengklik elemen:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
    </style>
</head>
<body>

    <div>Click me</div>
    
    <script>
$(function() {
    $("div").click(function () {
        alert("Clicked!");
    });
    $("div").trigger("click");
});
    </script>
</body>
</html>
```

Kode ini memicu acara klik untuk elemen yang dipilih


> Metode trigger () tidak dapat digunakan untuk meniru acara browser asli, seperti mengklik kotak input file atau tag anchor. Hanya acara dalam sistem acara jQuery yang dapat ditangani.
