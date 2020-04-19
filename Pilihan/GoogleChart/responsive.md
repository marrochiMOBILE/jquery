# responsive frgafik / goole chart

anda bisa menggunakan fungsi resize
```javascript
$(function (){
 $(window).resize(function(){
        drawChart();
        });
});
```

atau bisa jugha seperti ini

```javascript
$(document).ready(function(){
 $(window).resize(function(){
        drawChart();
        });
});
```