# background-size

* 可以自訂圖片尺寸
```scss
body{
  background-image: url("https://i.imgur.com/o57A3gD.png");
  background-position: 100px 100px;
  background-repeat: repeat;
  background-size: 30vh;
}
```

* ``` contain ```
  * 讓寬度適應螢幕大小
  * 如果沒有特別設定圖片大小，則尺寸就以所在空間的短邊為主

```html
<div class="test"></div>
```

```scss
.test{
  width: 1000px;
  height: 1000px;
  background-color: gold;
  background-image: url("https://i.imgur.com/o57A3gD.png");
  background-size: contain;
}
```

* ``` cover ```
  * 使圖片不依靠repeat，也能佔滿整個版面
  * 但如果所在空間尺寸小於圖片本身，圖片本身會無法顯示

```scss
.test{
  width: 1000px;
  height: 1000px;
  background-color: gold;
  background-image: url("https://i.imgur.com/o57A3gD.png");
  background-size: cover;
}
```


* ``` 100% auto ```
  * width height
  * width 100%，height則隨圖片比例縮放

``` scss
.test{
  width: 1000px;
  height: 600px;
  background-color: gold;
  background-image: url("https://i.imgur.com/o57A3gD.png");
  background-size: 70% auto;
}
```