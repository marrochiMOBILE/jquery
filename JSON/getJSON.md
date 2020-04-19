# getJSON
mengambil data jason 

## 1

#### coba2.json
```json
[
    {
        "nama" : "marrochi",
        "umur" : 22,
        "lulus" : true,
        "hoby"  : ["gamers","bultang"],
        "pembimbing" : {
            "pembmbing1" : "eko mulyono",
            "pembimbing2" : "vairus sal sabila"
        }
    },
    {
        "nama" : "malia",
        "umur" : 20,
        "lulus" : false,
        "hoby"  : ["berenang"],
        "pembimbing" : {
            "pembmbing1" : "ajis bambang",
            "pembimbing2" : "sania"
        }
    }
]
```


#### file HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script src="../jquery.js"></script>
    <script>
        $.getJSON('coba2.json', function(bebas){
        //   console.log(bebas)
         console.log(bebas[0]['pembimbing']['pembimbing2']) // vairus sal sabila
       })
    </script>
</body>
</html>
```