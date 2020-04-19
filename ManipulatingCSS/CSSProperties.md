# CSS Properties

Mirip dengan metode html (), metode css () dapat digunakan untuk mendapatkan dan menetapkan nilai properti CSS.
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
   p {
        background-color:red;
        color: white;
    }
    </style>
</head>
<body>

   <p>Some text</p>
  

    
  <script>
$(function() {
    alert($("p").css("background-color"));
    $("p").css("background-color", "blue");
});

  </script>
</body>
</html>
```

### Multiple Properties


Untuk mengatur beberapa properti CSS, metode css () menggunakan sintaks JSON, yaitu:

> css({"property":"value","property":"value",...});

Seperti yang Anda lihat, sintaks terdiri dari pasangan "properti": "nilai", yang dipisahkan koma dan dilampirkan dalam kurung keriting {}.
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

   <p>Some text</p>
  

    
  <script>
$(function() {
    $("p").css({"background-color": "red", "font-size": "200%"});
});


  </script>
</body>
</html>
```

### dimensions

Metode width () dan height () dapat digunakan untuk mendapatkan dan mengatur lebar dan tinggi elemen HTML.

Mari atur lebar dan tinggi div ke 100px, serta atur warna latar untuknya:

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

    <div></div>
  

    
  <script>
$(function() {
    $("div").css("background-color", "red");
    $("div").width(100);
    $("div").height(100);
});

  </script>
</body>
</html>
```

Metode lebar () dan tinggi () mendapatkan dan mengatur dimensi tanpa bantalan, batas, dan margin.
Metode innerWidth () dan innerHeight () juga termasuk padding.
Metode outerWidth () dan outerHeight () termasuk padding dan borders.
Lihat gambar ini untuk memahami cara kerjanya

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
    width: 300px;
    height: 100px;
    padding: 10px;
    margin: 20px;
    border: 3px solid blue;
    background-color: red;
    color: white;
}
    </style>
</head>
<body>

    <div></div>
  

    
  <script>
$(function() {
    var txt = "";
    txt += "width: " + $("div").width() + " ";
    txt += "height: " + $("div").height() + "<br/>";
    txt += "innerWidth: " + $("div").innerWidth() + " ";
    txt += "innerHeight: " + $("div").innerHeight() + "<br/>";
    txt += "outerWidth: " + $("div").outerWidth() + " ";
    txt += "outerHeight: " + $("div").outerHeight();
    
    $("div").html(txt);
});


  </script>
</body>
</html>
```