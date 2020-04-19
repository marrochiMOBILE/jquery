# DOM Traversal


jQuery memiliki banyak metode yang berguna untuk traversal DOM.
Metode parent () mengembalikan elemen induk langsung dari elemen yang dipilih. Sebagai contoh:
HTML:

```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
        div {
            padding: 10px;
        }
        p {
            border: 1px solid black;
            padding: 5px;
        }
    </style>
</head>
<body>

    <div> div element
        <p>paragraph</p> 
    </div>

    <div>
    
    <span>
        border parent
         <p>
                paragft
        </p>
    </span>    
  

    
  <script>
$(function() {
    var e = $("p").parent();
    e.css("border", "2px solid red");
});
  </script>
</body>
</html>
```


Kode di atas memilih elemen induk paragraf dan menetapkan batas merah untuknya.

> Run the code to see it in action.


Metode parent() hanya dapat melintasi satu tingkat di atas pohon DOM.
Untuk mendapatkan semua leluhur dari elemen yang dipilih, Anda dapat menggunakan metode parents(). Sebagai contoh:
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
    body, div, ul, li {
        padding: 5px;
        margin: 15px;
        }
    p {
        border: 1px solid black;
        padding: 5px;
    }
    </style>
</head>
<body>

    <div style="width:300px;">div
        <ul>ul
            <li>li
                <p>paragraph</p>
            </li>
        </ul>   
    </div>
    
  <script>
$(function() {
    var e = $("p").parents();
    e.css("border", "2px solid red");
});
  </script>
</body>
</html>
```

Kode di atas menetapkan batas merah untuk semua orang tua paragraf.

Beberapa metode traversal yang paling sering digunakan disajikan di bawah ini:

> lihat gambar 3.png

Metode eq() dapat digunakan untuk memilih elemen tertentu dari beberapa elemen yang dipilih.
Misalnya, jika halaman berisi beberapa elemen div dan kami ingin memilih yang ketiga:

> $("div").eq(2);

`Nomor indeks mulai dari 0, jadi elemen pertama akan memiliki nomor indeks 0.`


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

    <p>a</p>
    <p>b</p> <!-- tampil boosque-->
    <p>c</p>
    
    <script>
    alert($("p").eq(1).text());
    </script>

</body>
</html>
```
