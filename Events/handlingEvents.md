# Handling Events

JQuery menyediakan cara yang efisien untuk menangani acara. Peristiwa terjadi ketika pengguna melakukan tindakan, seperti mengklik elemen, menggerakkan mouse, atau mengirimkan formulir.
Ketika suatu peristiwa terjadi pada elemen target, fungsi handler dieksekusi.
Sebagai contoh, katakanlah kita ingin menangani acara klik pada elemen dengan id = "demo" dan menampilkan tanggal saat ini ketika tombol diklik. Menggunakan JavaScript murni, kodenya terlihat seperti:

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

    <div id="demo">Click Me</div>

    <script>
    window.onload = function() {
        var x = document.getElementById("demo");
        x.onclick = function () {
            document.body.innerHTML = Date();
        }
    };
    
    </script>
</body>
</html>
```

Acara yang sama dapat ditangani menggunakan jQuery dengan kode berikut:

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

    <div id="demo">Click Me</div>

    <script>
    $(function() {
        $("#demo").click(function() {
            $("body").html(Date());
        });
    });
    </script>
</body>
</html>
```


Seperti yang Anda lihat, kode jQuery lebih pendek dan lebih mudah dibaca dan ditulis.
Perhatikan, bahwa nama acara disediakan tanpa awalan "on" (mis., Klik di JavaScript adalah klik di jQuery).

> Fungsi yang dieksekusi ketika suatu peristiwa dipecat disebut event handler.

### Common Events
> lihat gamvar 1.png
Berikut ini adalah acara yang paling sering digunakan:
Acara Mouse:
klik terjadi ketika suatu elemen diklik.
dblklik terjadi ketika sebuah elemen diklik dua kali.
mouseenter terjadi ketika pointer mouse lebih (memasuki) elemen yang dipilih.
mouseleave terjadi ketika pointer mouse meninggalkan elemen yang dipilih.
mouseover terjadi ketika pointer mouse berada di atas elemen yang dipilih.

Acara Keyboard:
keydown terjadi ketika tombol keyboard ditekan.
keyup terjadi ketika tombol keyboard dilepaskan.

Bentuk Acara:
kirim terjadi ketika formulir dikirimkan.
perubahan terjadi ketika nilai elemen telah diubah.
fokus terjadi ketika suatu elemen mendapat fokus.
blur terjadi ketika suatu elemen kehilangan fokus.

Dokumen Acara:
ready terjadi ketika DOM telah dimuat.
perubahan ukuran terjadi ketika jendela browser berubah ukuran.
gulir terjadi ketika pengguna menggulir di elemen yang ditentukan.

Sebagai contoh, mari kita ubah konten div ketika pengguna mengetik di bidang input. Untuk melakukan itu, kita perlu menangani peristiwa keydown, yang terjadi ketika tombol pada keyboard ditekan:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
#msg {
    color: blue;
    font-size: 16pt;
    font-weight: bold;
}
    </style>
</head>
<body>

    <input type="text" id="name" />
    <div id="msg"></div>

    <script>
$(function() {
    $("#name").keydown(function() {
        $("#msg").html($("#name").val());
    });
});
    </script>
</body>
</html>
```

Kode di atas menangani event keydown untuk elemen dengan id = "name" dan menetapkan konten div dengan id = "msg" nilai bidang input.

> Nama acara cukup jelas, jadi cukup bereksperimen untuk melihatnya beraksi.

```js
$("p").click(function() {
  alert("Clicked!");
});
```
Cara lain untuk menangani acara di jQuery adalah dengan menggunakan metode on ().
Metode on () digunakan untuk melampirkan peristiwa ke elemen yang dipilih. Sebagai contoh:

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

    <p>Click Me</p>

    <script>
$(function() {
    $( "p" ).on( "click", function() {
        alert("clicked");
    });
});
    </script>
</body>
</html>
```


Seperti yang Anda lihat, nama acara dilewatkan sebagai argumen pertama ke metode on (). Argumen kedua adalah fungsi handler

```
Metode on () berguna untuk mengikat fungsi handler yang sama ke beberapa peristiwa. Anda dapat memberikan beberapa nama acara yang dipisahkan oleh spasi sebagai argumen pertama. Misalnya, Anda bisa menggunakan pengendali acara yang sama untuk acara klik dan dblklik.
```

### off

Anda dapat menghapus event handler menggunakan metode off ().
Sebagai contoh:

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

    <div>Click Me</div>

    <script>
$(function() {
    $("div").on("click", function() { 
        alert('Hi there!'); 
    }); 
    $("div").off("click");
});
    </script>
</body>
</html>
```
> Argumen metode off () adalah nama acara yang ingin Anda hapus handlernya.