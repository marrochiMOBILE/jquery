# Creating a To-Do List
Mari kita buat proyek daftar yang harus dilakukan menggunakan konsep yang telah kita pelajari.
Daftar yang Harus Dilakukan akan dapat menambahkan item baru ke daftar, serta menghapus item yang ada.
Pertama, kami membuat HTML:

```html
<h1>My To-Do List</h1>
<input type="text" placeholder="New item" />
<button id="add">Add</button>
<ol id="mylist"></ol>
```
> Mengklik tombol harus menambahkan nilai kolom input ke daftar <ol> kami.


Sekarang, setelah HTML siap, kita dapat mulai menulis kode jQuery kami.
Pertama, kami menangani acara klik untuk tombol:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
        h1 {
    color: #1abc9c;
}
.rem {
    margin-left: 5px;
    background-color: white;
    color: red;
    border: none;
    cursor: pointer;
}
    </style>
</head>
<body>

    <h1>My To-Do List</h1>
    <input type="text" placeholder="New item" />
    <button id="add">Add</button>
    <ol id="mylist"></ol>
    
    <script>
$(function() {
    $("#add").on("click", function() {
        var val = $("input").val();
        if(val !== '') {
            var elem = $("<li></li>").text(val);
            $(elem).append("<button class='rem'>X</button>");
            $("#mylist").append(elem);
            $("input").val("");
        }
    });
});
    </script>
</body>
</html>
```


Yang tersisa untuk dilakukan adalah menangani event klik pada tombol class = "rem" dan menghapus elemen <li> yang sesuai dari daftar

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
        h1 {
    color: #1abc9c;
}
.rem {
    margin-left: 5px;
    background-color: white;
    color: red;
    border: none;
    cursor: pointer;
}
    </style>
</head>
<body>

    <h1>My To-Do List</h1>
    <input type="text" placeholder="New item" />
    <button id="add">Add</button>
    <ol id="mylist"></ol>
    
    <script>
$(function() {
    $("#add").on("click", function() {
        var val = $("input").val();
        if(val !== '') {
            var elem = $("<li></li>").text(val);
            $(elem).append("<button class='rem'>X</button>");
            $("#mylist").append(elem);
            $("input").val("");
            $(".rem").on("click", function() {
                $(this).parent().remove();
            });
        }
    });
});
    </script>
</body>
</html>
```

To-Do List hanyalah demonstrasi singkat tentang cara menangani acara dan membangun proyek sederhana.

## cobalah 

```html
<div>1</div>
<script>
$("div").click(function() {
  $("div").text($("div").text()+1); // 111
});
</script>
```