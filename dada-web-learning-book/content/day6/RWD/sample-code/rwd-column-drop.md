# Column Drop
> 寫法參考

[回到 RWD設計模式 總列表](../section2-4.md)

```html
<div class="container">
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
</div>
```

```scss
/* Ref: https://developers.google.com/web/fundamentals/design-and-ux/responsive/patterns?hl=zh-tw
 */

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

.c1, .c2, .c3 {
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

/* media query */
@media (min-width: 600px) {
  .c1 {
    width: 60%;
    order: 2;
  }

  .c2 {
    width: 40%;
    order: 1;
  }

  .c3 {
    width: 100%;
    order: 3;
  }
}


@media (min-width: 800px) {
  .c2 {
    width: 20%;
  }

  .c3 {
    width: 20%;
  }
}
```

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

.c1, .c2, .c3 {
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

/* media query */
@include md{
  .c1 {
    width: 60%;
    order: 2;
  }

  .c2 {
    width: 40%;
    order: 1;
  }

  .c3 {
    width: 100%;
    order: 3;
  }
}


@include lg{
  .c2 {
    width: 20%;
  }

  .c3 {
    width: 20%;
  }
}
```

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


.c1 {
  background-color: #1D4587;
  @include xs{
    width: 100%;
  }
  @include sm{
    width: 100%;
  }
  @include md{
    width: 60%;
    order: 2;
  }
  @include lg{

  }
}

.c2 {
  background-color: #3C77D8;
  @include xs{
    width: 100%;

  }
  @include sm{
    width: 100%;
  }
  @include md{
    width: 40%;
    order: 1;
  }
  @include lg{
    width: 20%;
  }
}

.c3 {
  background-color: #C9DAF8;
  @include xs{
    width: 100%;
  }
  @include sm{
    width: 100%;
  }
  @include md{
    width: 100%;
    order: 3;
  }
  @include lg{
    width: 20%;
  }
}
```

[回到 RWD設計模式 總列表](../section2-4.md)