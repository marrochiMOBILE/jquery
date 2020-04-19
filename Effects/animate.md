# animate

Metode animate () memungkinkan Anda menganimasikan ke nilai yang ditetapkan, atau ke nilai relatif ke nilai saat ini.
Anda perlu mendefinisikan properti CSS yang akan dianimasikan sebagai parameternya dalam format JSON (pasangan "kunci": "nilai").
Parameter kedua menentukan kecepatan animasi.
Misalnya, kode berikut menjiwai properti lebar div dalam 1 detik ke nilai 250px:
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
    display:inline-block;
    padding:25px;
    background-color:grey;
    color:white;
    text-align:center;
    cursor:pointer;
}
    </style>
</head>
<body>

    <div>Click me</div>
    
    <script>
    $(function() {
        $("div").click(function() {
            $("div").animate({width: '250px'}, 1000);
        });
    });
    </script>
</body>
</html>
```
Perhatikan format JSON untuk menyediakan parameter CSS. Sintaks JSON juga digunakan dalam modul sebelumnya ketika memanipulasi properti CSS.

```
Anda dapat menganimasikan setiap properti CSS menggunakan sintaks yang disebutkan di atas, tetapi ada satu hal penting yang perlu diingat: semua nama properti harus dikunci unta saat digunakan dengan metode animate () (camelCase adalah praktik menulis kata atau frasa majemuk sehingga setiap kata atau singkatan dimulai dengan huruf kapital dengan kata pertama dalam huruf kecil).
Anda harus menulis paddingLeft alih-alih padding-kiri, marginRight, bukan margin-kanan, dan sebagainya.
```


Beberapa properti dapat dianimasikan secara bersamaan dengan memisahkannya dengan koma.
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
    display:inline-block;
    padding:25px;
    background-color:grey;
    color:white;
    text-align:center;
    cursor:pointer;
}
    </style>
</head>
<body>

    <div>Click me</div>
    
    <script>
   $(function() {
    $("div").click(function() {
        $("div").animate({
            width: '250px',
            height: '250px'
        }, 1000);
    });
});
    </script>
</body>
</html>
```
Dimungkinkan juga untuk menentukan nilai relatif (nilainya kemudian relatif terhadap nilai elemen saat ini). Ini dilakukan dengan meletakkan + = atau - = di depan nilai:

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
    display:inline-block;
    padding:25px;
    background-color:grey;
    color:white;
    text-align:center;
    cursor:pointer;
}
    </style>
</head>
<body>

    <div>Click me</div>
    
    <script>
$(function() {
    $("div").click(function() {
        $("div").animate({
            width: '+=250px',
            height: '+=250px'
        }, 1000);
    });
});
    </script>
</body>
</html>
```

## Animation Queue
Secara default, jQuery hadir dengan fungsi antrian untuk animasi.
Ini berarti bahwa jika Anda menulis beberapa panggilan animate () satu demi satu, jQuery membuat antrian "internal" untuk panggilan metode ini. Kemudian ia menjalankan panggilan satu per satu.
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
div {
    background:orange;
    height:80px;width:80px;
    position:absolute;
    border-radius: 50%;
    opacity: 0.5;
}
    </style>
</head>
<body>

    
   <div></div>
    
    <script>
$(function() {
    var div = $("div");
    div.animate({opacity: 1});
    div.animate({height: '+=100px', width: '+=100px', top: '+=100px'}, 500);
    div.animate({height: '-=100px', width: '-=100px', left: '+=100px'}, 500);
    div.animate({height: '+=100px', width: '+=100px', top: '-=100px'}, 500);
    div.animate({height: '-=100px', width: '-=100px', left: '-=100px'}, 500);
    div.animate({opacity: 0.5});
}); 
    </script>
</body>
</html>
```

Setiap panggilan metode animate () akan berjalan satu demi satu.
Ingat, untuk memanipulasi posisi elemen, Anda perlu mengatur properti posisi CSS elemen menjadi relatif, tetap, atau absolut.

```
Metode animate (), seperti metode hide / show / fade / slide, dapat menggunakan fungsi callback opsional sebagai parameternya, yang dieksekusi setelah efek saat ini selesai.
```