# Get Content

Ada beberapa metode untuk memanipulasi konten elemen HTML melalui jQuery.
Metode html () digunakan untuk mendapatkan konten dari elemen yang dipilih, termasuk markup HTML.

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
  <p>
     jquery is fun <b>:)</b>
  </p>

  <script>
      $(function() {
  var val = $("p").html();
  alert(val);
});
// alerts "JQuery is <b>fun</b>"
  </script>
</body>
</html>
```
Perhatikan, bahwa markup HTML (tag <b>) juga dikembalikan,
Jika Anda hanya membutuhkan konten teks, tanpa markup HTML, Anda dapat menggunakan metode text ():

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
  <p>
     jquery is fun <b>:)</b>
  </p>

  <span>cinta yang telah kita bina pahit, manis berdua, andaikan malam yang sepi dapat berbicara </span>

  <script>
 $(function() {
  var val = $("p").text();
  alert(val);
  console.log(val)


  let span = $("span").text();
  console.log(span)
});
// alerts "JQuery is fun"
  </script>
</body>
</html>
```

```html
<div id="test">
  <p>p</p>
</div>
<script>
  alert($("#test").text())
</script>
```


## value


Kita telah melihat dalam pelajaran sebelumnya bagaimana kita dapat memanipulasi konten elemen HTML menggunakan metode text () dan html ().
Metode lain yang bermanfaat adalah metode val (), yang memungkinkan kita untuk mendapatkan dan mengatur nilai bidang formulir, seperti kotak teks, dropdown, dan input serupa.
Sebagai contoh:
HTML:

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
    <input type="text" id="name" value="Your Name">

  <script>
    $(function() {
    alert($("#name").val());
    });
    //alerts "Your Name"
  </script>
</body>
</html>
```


Demikian pula, Anda bisa mengatur nilai untuk bidang dengan menyediakannya sebagai parameter ke metode val ()

```
Getting and setting form field values is very useful when you need to handle form events and validation. We will cover events later in the course.
```

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
    <input type="text" id="user" value="Your Name">
    <p id="demo"></p>

  <script>
$(function() {
  var t = $("#user").val();
  $("#demo").text(t);
});
  </script>
</body>
</html>
```

# Summary

Metode jQuery berikut tersedia untuk mendapatkan dan mengatur konten dan atribut elemen HTML yang dipilih:
1. text () mengatur atau mengembalikan konten teks dari elemen yang dipilih.
1. html () mengatur atau mengembalikan konten elemen yang dipilih (termasuk markup HTML).
1. val () menetapkan atau mengembalikan nilai bidang formulir.
1. attr () menetapkan atau mengembalikan nilai atribut.
1. removeAttr () menghapus atribut yang ditentukan.
