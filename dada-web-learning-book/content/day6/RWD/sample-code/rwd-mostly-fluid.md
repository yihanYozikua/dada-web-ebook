# Mostly Fuild
> 寫法參考
[回到 RWD設計模式 總列表](../section2-4.md)

```html
<div class="container"> <!--這個 "container" 是bootstrap的語法喔-->
  <div class="c1">
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
  </div>

  <div class="c2">
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
  </div>

  <div class="c3">
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
  </div>

  <div class="c4">
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
  </div>

  <div class="c5">
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
  </div>
</div>
```

### css/scss 寫法（一）
```scss
/* Ref: https://developers.google.com/web/fundamentals/design-and-ux/responsive/patterns?hl=zh-tw*/

/* basic setting */

body {
  background: #FFF;
}

p {
  margin: 2vw;
  color: white;
}

.container {
  display: flex;
  flex-flow: row wrap; // flex-direction 和 flex-wrap的縮寫
}

.c1, .c2, .c3, .c4, .c5 { // 一般狀況，在這個例子裡面，一般情況指的是手機版
  width: 100%;
}

.c1 {
  background-color: #1D4587;
}

.c2 {
  background-color: #3C77D8;
}

.c3 {
  background-color: #C9DAF8;
}

.c4 {
  background-color: #D5DFEF;
}

.c5 {
  background-color: #DFE1E5;
}

/* media query */
@media (min-width: 768px) { // 當版面width介於768px ~ 992px之間時
  
  .c2, .c3, .c4, .c5 {
    width: 50%;
  }
}

@media (min-width: 992px) { // 當版面width大於992px時
  .c1 {
    width: 60%;
  }
  .c2 {
    width: 40%;
  }
  .c3, .c4 {
    width: 33%;
  }
  .c5 {
    width: 34%;
  }
}
```

### css/scss 寫法（二）
```scss
@import "./vars.scss";

body {
  background: #FFF;
}

p {
  margin: 2vw;
  color: white;
}

.container {
  display: flex;
  flex-flow: row wrap; // flex-direction 和 flex-wrap的縮寫
}


.c1, .c2, .c3, .c4, .c5 { // 一般狀況，在這個例子裡面，一般情況指的是手機版
  width: 100%;
}

.c1 {
  background-color: #1D4587;
}

.c2 {
  background-color: #3C77D8;
}

.c3 {
  background-color: #C9DAF8;
}

.c4 {
  background-color: #D5DFEF;
}

.c5 {
  background-color: #DFE1E5;
}

/* media query */
@include md{ // 當版面width介於768px ~ 992px之間時
  
  .c2, .c3, .c4, .c5 {
    width: 50%;
  }
}

@include lg{ // 當版面width大於992px時
  .c1 {
    width: 60%;
  }
  .c2 {
    width: 40%;
  }
  .c3, .c4 {
    width: 33%;
  }
  .c5 {
    width: 34%;
  }
}
```

### css/scss 寫法（三）
```scss
@import "./vars.scss";

body {
  background: #FFF;
}

p {
  margin: 20px;
  color: white;
}

.container {
  display: flex;
  flex-flow: row wrap; // flex-direction 和 flex-wrap的縮寫
}

.c1 {
  background-color: #1D4587;
  @include xs{
    width: 100%;
  }
  // @include sm{
  //   width: 100%;
  // }
  // @include md{

  // }
  @include lg{
    width: 60%;
  }
}

.c2 {
  background-color: #3C77D8;
  @include xs{
    width: 100%;
  }
  // @include sm{
  //   width: 100%;
  // }
  @include md{
    width: 50%;
  }
  @include lg{
    width: 40%;
  }
}

.c3 {
  background-color: #C9DAF8;
  @include xs{
    width: 100%;
  }
  // @include sm{
  //   width: 100%;
  // }
  @include md{
    width: 50%;
  }
  @include lg{
    width: 33%;
  }
}

.c4 {
  background-color: #D5DFEF;
  @include xs{
    width: 100%;
  }
  // @include sm{
  //   width: 100%;
  // }
  @include md{
    width: 50%;
  }
  @include lg{
    width: 33%;
  }
}

.c5 {
  background-color: #DFE1E5;
  @include xs{
    width: 100%;
  }
  // @include sm{
  //   width: 100%;
  // }
  @include md{
    width: 50%;
  }
  @include lg{
    width: 34%;
  }
}
```

[回到 RWD設計模式 總列表](../section2-4.md)