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
  color: #ddd;
  background-color: #003476;
}

.c2 {
  color: #ddd;
  background-color: #0062d2;
}

.c3 {
  color: #333;
  background-color: #b4d2f7;
}

.c4 {
  color: #333;
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

```

### CSS/SCSS寫法（三）
```scss

```

[回到 RWD設計模式 總列表](../section2-4.md)