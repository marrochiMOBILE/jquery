# Attributes and Content Get & Set Attribute Values
Kami dapat memanipulasi atribut yang ditetapkan ke elemen HTML dengan mudah melalui jQuery.
href, src, id, class, style adalah semua contoh atribut HTML.

Metode attr () juga memungkinkan kita untuk menetapkan nilai atribut dengan menetapkannya sebagai parameter kedua.
Sebagai contoh:

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
    <a href="https://www.facebook.com/">SELECTOR</a>

    <a href="https://twitter.com/" id="ml" target="_blank">ID</a> 

    <a href="https://google.com/" class="kelas1" target="_blank">CLASS 1</a> 
    <a href="https://google.com/" class="kelas2" target="_blank">CLASS 2</a> 
    <a href="https://google.com/" class="kelas3" target="_blank">CLASS 3</a> 


    <div>
        <div>
            <a href="https://google.com/" class="coba1">array 1</a>
            <a href="https://google.com/" class="coba2">array 2 </a>
        </div>
    </div>

    <div>
        <div>
            <a href="https://google.com/" class="jajal1">function</a>
        </div>
    </div>
    
    <p>
            <a href="https://google.com/" class="a1">Array Of Object 1 </a>
            <a href="ksalkanlnslan" class="a1">Array Of Object 2 </a>
    </p>


    <script>
   $(function() {
    $("a").attr("href", "http://www.jquery.com");
    let bo = $("a#ml").attr("href", "https://xwayzet.000webhostapp.com/");

    // object
    const lt = {
                kelas1 :  $("a.kelas1").attr("href", "https://xwayzet.000webhostapp.com/"),
                kelas2 :  $("a.kelas2").attr("href", "https://xwayzet.000webhostapp.com/"),
                kelas3 :  $("a.kelas3").attr("href", "https://xwayzet.000webhostapp.com/")
    };
   

    // array
    var st = [ $("div .coba1").attr("href", "https://xwayzet.000webhostapp.com/"),  $("div .coba2").attr("href", "https://xwayzet.000webhostapp.com/"),]

    //function
    function fc(){
        $("div > div > .jajal1").attr("href", "https://xwayzet.000webhostapp.com/");
    }
    fc()

    // array Object
   let endGame = [{
        nama :  $("p > .a1").attr("href", "https://xwayzet.000webhostapp.com/")
   },{
        nama2:  $("p .a1").attr("href", "https://xwayzet.000webhostapp.com/")
   }];
 

    //end jquery 
    });
    </script>
</body>
</html>
```