# Off Canvas
> 寫法參考

[回到 RWD設計模式 總列表](../section2-4.md)

### HTML
```html
  <div class="container" role="main">
    <div class="c1" id="leftDrawer">
    </div>
    <div class="c2" id="mainPanel">
      Click the <code>div</code>'s to change views
    </div>
    <div class="c3" id="rightDrawer">
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

### JS
```JS
var position = 0;
var mainPanel = document.getElementById("mainPanel");
var leftDrawer = document.getElementById("leftDrawer");
var rightDrawer = document.getElementById("rightDrawer");

function toggle(evt) {
  position++;
  if (position % 3 == 0) {
    leftDrawer.classList.remove("open");
    rightDrawer.classList.remove("open");
  } else if (position % 3 == 1) {
    leftDrawer.classList.add("open");
    rightDrawer.classList.remove("open");
  } else {
    leftDrawer.classList.remove("open");
    rightDrawer.classList.add("open");
  }
}

mainPanel.addEventListener("click", toggle);
leftDrawer.addEventListener("click", toggle);
rightDrawer.addEventListener("click", toggle);
```

[回到 RWD設計模式 總列表](../section2-4.md)