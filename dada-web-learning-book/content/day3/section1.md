# Loading頁面怎麼寫
[別人寫好的Loading Page參考](https://codepen.io/search/pens?q=loading&page=1&order=popularity&depth=everything&show_forks=false)


#### HTML
```html
<!-- html -->
<body onload="你設定的function名稱()">
    <div class="你設定的class名稱()">
        開始寫你的Loading效果
    </div>
</body>
```
```html
<!-- html -->
<body onload="loading_page()">
    <div class="load" style="background-color: teal;" >
      <p class="text">載入中...</p>
    </div>
</body>
```


#### CSS
```css
/*css*/
.你設定的class名稱{
    /*CSS property設定*/
}
``` 
```css
/*css*/
.load {
  position: fixed;
  background: lightblue;
  width: 100%;
  height: 100vh;
  z-index: 99999;
  top: 0;
  left: 0;
}

.load p {
  text-align: center;
  position: relative;
  top: 50%;
}
```


#### JS
```js
//js
function 你設定的function名稱(){
    $("你設定的class名稱").fadeOut(3000); //指定3000毫秒後，Loading頁面會消失
}
```
```js
//js
function loading_page(){
  $(".loader").fadeOut(3000);
}
```