# Layout Shifter
> 寫法參考

[回到 RWD設計模式 總列表](../section2-4.md)

### HTML
```html
  <div class="container" role="main">
    <div class="c1">
      <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
    </div>
    <div class="c4">
      <div class="c2">
        <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
      </div>
      <div class="c3">
        <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
      </div>
    </div>
  </div>
```

### CSS/SCSS寫法（一）
```scss
body {
  margin: 0;
  color: white !important;
}

.container {
  display: flex;
  flex-flow: row wrap; // flex-direction 和 flex-wrap的縮寫
}

.container div {
  box-sizing: border-box;
  min-height: 150px;
  min-width: 150px;
}

.c1, .c2, .c3, .c4 {
  width: 100%;
}

.c1 {
   background-color: #003476;
}

.c2 {
  background-color: #0062d2;
}

.c3 {
  background-color: #b4d2f7;
}

.c4 {
  background-color: #d5dfef;
}

@media (min-width: 762px) {
  .c1 {
    width: 25%;
  }

  .c4 {
    width: 75%;
  }

}

@media (min-width: 992px) {
  .container {
    width: 800px;
    margin-left: auto;
    margin-right: auto;
  }
}
```

### CSS/SCSS寫法（二）
```scss
@import "./vars.scss";

body {
  margin: 0;
  color: white !important;
}

.container {
  display: flex;
  flex-flow: row wrap; // flex-direction 和 flex-wrap的縮寫
}

.container div {
  box-sizing: border-box;
  min-height: 150px;
  min-width: 150px;
}

.c1, .c2, .c3, .c4 {
  width: 100%;
}

.c1 {
  background-color: #003476;
}

.c2 {
  background-color: #0062d2;
}

.c3 {
  background-color: #b4d2f7;
}

.c4 {
  background-color: #d5dfef;
}

@include md{
  .c1 {
    width: 25%;
  }

  .c4 {
    width: 75%;
  }

}

@include lg{
  .container {
    width: 800px;
    margin-left: auto;
    margin-right: auto;
  }
}
```

### CSS/SCSS寫法（三）
```scss
@import "./vars.scss";

body {
  margin: 0;
  color: white !important;
}

.container {
  display: flex;
  flex-flow: row wrap; // flex-direction 和 flex-wrap的縮寫

  @include lg{
    width: 800px;
    margin-left: auto;
    margin-right: auto;
  }
}

.container div {
  box-sizing: border-box;
  min-height: 150px;
  min-width: 150px;
}


.c1 {
   background-color: #003476;
   @include xs{
    width: 100%;
   }
   @include sm{
    width: 100%;
   }
   @include md{
    width: 25%;
   }
   @include lg{

   }
}

.c2 {
  background-color: #0062d2;
  @include xs{
    width: 100%;
  }
  @include sm{
    width: 100%;
  }
  @include md{

  }
  @include lg{
    
  }
}

.c3 {
  background-color: #b4d2f7;
  @include xs{
    width: 100%;
  }
  @include sm{
    width: 100%;
  }
  @include md{

  }
  @include lg{
    
  }
}

.c4 {
  background-color: #d5dfef;
  @include xs{
    width: 100%;
  }
  @include sm{
    width: 100%;
  }
  @include md{
    width: 75%;
  }
  @include lg{

  }
}
```

[回到 RWD設計模式 總列表](../section2-4.md)