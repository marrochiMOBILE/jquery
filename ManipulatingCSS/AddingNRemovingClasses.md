# Adding & Removing Classes

jQuery memiliki beberapa metode untuk manipulasi CSS.
Metode addClass () menambahkan satu atau lebih kelas ke elemen yang dipilih.
Sebagai contoh:
HTML:

### addClass
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
       .header {
    color: blue;
    font-size:x-large;
    }
    .red {
        color: red;
        font-weight: bold;
    }
    </style>
</head>
<body>
    
   <div class="header red">Some text</div>

  <script>
$(function() {
    $("div").addClass("header ");
});
  </script>
</body>
</html>
```

Kode di atas memberikan elemen div "header" kelas.
```
Untuk menentukan beberapa kelas dalam metode addClass (), pisahkan saja menggunakan spasi. Misalnya, $ ("div"). AddClass ("class1 class2 class3").
```

### removeClass
Metode removeClass () menghapus satu atau lebih nama kelas dari elemen yang dipilih.
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
       .header {
    color: blue;
    font-size:x-large;
    }
    .red {
        color: red;
        font-weight: bold;
    }
    </style>
</head>
<body>

  <div class="header red">Some text</div>
  <script>
      $(function() {
            $("div").removeClass("red");
        });
  </script>
</body>
</html>
```

### toggleClass()
Metode toggleClass () beralih antara menambahkan / menghapus kelas dari elemen yang dipilih, yang berarti bahwa jika kelas yang ditentukan ada untuk elemen, itu dihapus, dan jika tidak ada, ditambahkan.
Untuk mendemonstrasikan ini dalam tindakan, kami akan menangani acara klik tombol untuk beralih kelas. Kita akan belajar lebih banyak tentang peristiwa dan sintaksisnya dalam modul yang akan datang

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
    .red { 
    color:red; 
    font-weight: bold;
    }
    </style>
</head>
<body>

   <p>Some text</p>
   <button>Toggle Class</button>

    
  <script>
     $(function() {
  $("button").click(function() {
    $("p").toggleClass("red");
  });
});
  </script>
</body>
</html>
```