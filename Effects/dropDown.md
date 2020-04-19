# create Drop Down Menu

Mari kita buat menu drop-down sederhana yang akan terbuka setelah mengklik pada item menu.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="jquery.js"></script>
    <style>
#item {
    background-color: #4CAF50;
    color: white;
    padding: 16px;
    font-size: 16px;
    border: none;
    cursor: pointer;
}
#item:hover, #item:focus {
    background-color: #3e8e41;
}
.menu {
    position: relative;
    display: inline-block;
}
#submenu {
    display: none;
    position: absolute;
    background-color: #3e8e41;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
}
#submenu a {
    color: white;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}
#submenu a:hover {
    background-color: #4CAF50
}
    </style>
</head>
<body>

    
    <div class="menu">
        <div id="item">Dropdown</div>
        <div id="submenu">
          <a href="#">Link 1</a>
          <a href="#">Link 2</a>
          <a href="#">Link 3</a>
        </div>
      </div>
    
    <script>
$(function() {
    $("#item").click(function() {
        $("#submenu").slideToggle(500);
    });
}); 
    </script>
</body>
</html>
```

Kode di atas menangani event klik elemen id = "item" dan membuka / menutup submenu dalam 500 milidetik.
```
Jalankan kode untuk melihatnya beraksi. Anda juga dapat melihat CSS yang digunakan untuk menata item.
```
