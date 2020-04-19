# adding content

Seperti yang telah kita lihat dalam pelajaran sebelumnya, metode html () dan teks () dapat digunakan untuk mendapatkan dan mengatur konten elemen yang dipilih. Namun, ketika metode ini digunakan untuk mengatur konten, konten yang ada hilang.
jQuery memiliki metode yang digunakan untuk menambahkan konten baru ke elemen yang dipilih tanpa menghapus konten yang ada:
append () menyisipkan konten di akhir elemen yang dipilih.
prepend () menyisipkan konten di awal elemen yang dipilih.
after () menyisipkan konten setelah elemen yang dipilih.
before () menyisipkan konten sebelum elemen yang dipilih.

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
   <p id="demo">hai </p>
   <p id="demo2"> hai</p>
   <p id="demo3"> hai namaku david</p>
   <p id="demo4"> hai namaku aldo</p>

  <script>
$(function() {
    $("#demo").append("David");
    $("#demo2").prepend("David");
    $( "#demo3" ).before( "<b>Hello</b>" );
    $("#demo4").after("<b>Hello</b>");
});
  </script>
</body>
</html>
```

Metode append (), prepend (), before () dan after () juga dapat digunakan untuk menambahkan elemen yang baru dibuat.
Cara termudah untuk membuat elemen HTML baru dengan jQuery adalah sebagai berikut:


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
    <p id="demo">Hello</p>

  <script>
$(function() {
    var txt = $("<p></p>").text("Hi");
    /*
    Kode di atas membuat elemen <p> baru, yang berisi teks Hai dan menetapkannya ke variabel yang disebut txt.
    Sekarang, kita dapat menggunakan variabel itu sebagai parameter dari metode yang disebutkan di atas untuk menambahkannya ke HTML kita
    */
    $("#demo").after(txt);
});
  </script>
</body>
</html>
```


Ini akan memasukkan elemen `<p>` yang baru dibuat setelah paragraf `#demo`.
Anda juga dapat menentukan beberapa elemen sebagai argumen untuk metode before (), after (), append (), prepend () dengan memisahkannya menggunakan koma: $ ("# demo"). Append (var1, var2, var3).

```
Sintaks yang disebutkan di atas untuk membuat elemen dapat digunakan untuk membuat elemen HTML baru, misalnya $ ("<div> </div>") membuat div baru.
```