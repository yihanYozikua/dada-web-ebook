# Tiny Tweaks
> 寫法參考

[回到 RWD設計模式 總列表](../section2-4.md)

### HTML
```html
  <div class="c1">
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大
      好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛
      大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大
      好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大
      好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛
      大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大
      好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
    <p>大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大
      好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛
      大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大
      好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛大大好正好可愛</p>
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

.c1 {
  color: #ddd;
  background-color: #003476;
}

.c1 {
  padding: 10px;
  width: 100%;
}

@media (min-width: 500px) {
  .c1 {
    padding: 20px;
    font-size: 1.5em;
  }
}

@media (min-width: 800px) {
  .c1 {
    padding: 40px;
    font-size: 2em;
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