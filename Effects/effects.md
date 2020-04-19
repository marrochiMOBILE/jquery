# Effects

## Hide/Show
Query memiliki beberapa efek yang mudah diterapkan untuk membuat animasi.
Metode hide () dan show () digunakan untuk menyembunyikan dan menampilkan elemen yang dipilih.
Metode toggle () digunakan untuk beralih antara elemen bersembunyi dan menampilkan.
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
    background-color:grey;
    text-align:center;
    color:white;
    padding:5px;
    cursor:pointer;
}
div {
    background-color:grey;
    color:white;
}
    </style>
</head>
<body>

    
            <p>Click to toggle show/hide</p>
            <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            </div>
 
    
    <script>
$(function() {
    $("p").click(function() {
        $("div").toggle();
    });
});
    </script>
</body>
</html>
```
Metode hide / show / toggle dapat mengambil argumen opsional, kecepatan, yang menentukan kecepatan animasi dalam milidetik.
Misalnya, mari kita lewati 1000 milidetik sebagai argumen kecepatan ke metode toggle ()

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
    background-color:grey;
    text-align:center;
    color:white;
    padding:5px;
    cursor:pointer;
}
div {
    background-color:grey;
    color:white;
}
    </style>
</head>
<body>

    
            <p>Click to toggle show/hide</p>
            <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            </div>
  
    
    <script>
$(function() {
    $("p").click(function() {
        $("div").toggle(1000);
    });
});
    </script>
</body>
</html>
```

## Fade In/Out
Mirip dengan metode sembunyikan / tampilkan, jQuery menyediakan metode fadeIn / fadeOut, yang memudar elemen masuk dan keluar dari visibilitas.
Sama seperti metode toggle () yang beralih antara menyembunyikan dan menampilkan, metode fadeToggle () memudar masuk dan keluar.
Mari kita lihat aksi fadeToggle ():

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
    background-color:grey;
    text-align:center;
    color:white;
    padding:5px;
    cursor:pointer;
}
div {
    background-color:grey;
    color:white;
}
    </style>
</head>
<body>

  
            <p>Click to toggle show/hide</p>
            <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            </div>
  
    
    <script>
$(function() {
    $("p").click(function() {
        $("div").fadeToggle(1000);
    });
});
    </script>
</body>
</html>
```


Sama seperti toggle (), fadeToggle () membutuhkan dua parameter opsional: kecepatan dan panggilan balik.
> metode lain yang digunakan untuk fading adalah fadeTo (), yang memungkinkan fading ke opacity yang diberikan (nilai antara 0 dan 1). Misalnya: $ ("div"). FadeTo (1500, 0.7);

## Slide Up/Down

Metode slideUp () dan slideDown () digunakan untuk membuat efek geser pada elemen.
Sekali lagi, mirip dengan metode beralih sebelumnya, metode slideToggle () beralih antara efek geser dan dapat mengambil dua parameter opsional: kecepatan dan panggilan balik.

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
    background-color:grey;
    text-align:center;
    color:white;
    padding:5px;
    cursor:pointer;
}
div {
    background-color:grey;
    color:white;
}
    </style>
</head>
<body>

  
            <p>Click to toggle show/hide</p>
            <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            </div>

    
    <script>
$(function() {
    $("p").click(function() {
        $("div").slideToggle(500);
    });
});
    </script>
</body>
</html>
```