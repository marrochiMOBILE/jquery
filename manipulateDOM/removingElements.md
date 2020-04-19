# remove elements

Kami menghapus elemen yang dipilih dari DOM menggunakan metode remove (). Sebagai contoh:
HTML:

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

    <p style="color:red">Red</p>
        <p style="color:green">Green</p> <!-- remove jadi ilang-->
        <p style="color:blue">Blue</p>



    <script>
$(function() {
    $("p").eq(1).remove();
});
    </script>
</body>
</html>
```

Ini menghilangkan Hijau, elemen paragraf kedua.
Anda juga dapat menggunakan metode remove () pada beberapa elemen yang dipilih, misalnya $ ("p"). Remove () menghapus semua paragraf.

> Metode jQuery remove () menghapus elemen yang dipilih, serta elemen turunannya.

## Removing Content


Metode kosong () digunakan untuk menghapus elemen turunan dari elemen yang dipilih. Sebagai contoh:
HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
    div {
        background-color: aqua;
        width: 300px;
        height: 200px;
    }
    </style>
</head>
<body>

    <div>
        <p style="color:red">Red</p>
        <p style="color:green">Green</p>
        <p style="color:blue">Blue</p>
     </div>

    <script>
$(function() {
    $("div").empty(); // bikin kosong ke hatiku
});
    </script>
</body>
</html>
```

