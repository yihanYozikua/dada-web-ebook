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
  overflow-x: hidden;
}

.container {
  display: block;
  margin: 0;
  padding: 0;
  width: 100%;
  color: white;
}

.container div {
  box-sizing: border-box;
  min-height: 150px;
  min-width: 150px;
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

.c5 {
  background-color: #dfe1e5;
}


.c1, .c3 {
  position: absolute;
  width: 250px;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden; 

  -webkit-transition: -webkit-transform 0.4s ease-out;
  transition: transform 0.4s ease-out;
  
  z-index: 1;
}

.c1 {
  -webkit-transform: translate(-250px,0);
  transform: translate(-250px,0);
}

.c1.open {
  -webkit-transform: translate(0,0);
  transform: translate(0,0);
}

.c2 {
  width: 100%;
  position: absolute;
}

.c3 {
  left: 100%;
}

.c3.open {
  -webkit-transform: translate(-250px,0);
  transform: translate(-250px,0);
}

@media (max-width: 500px) {
  /* If the screen is wider then 500px, use Flexbox */
  .container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-flow: row nowrap;
    flex-flow: row nowrap;
  }
  .c1 {
    position: relative;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
  .c2 {
    position: static;
  }
}

@media (min-width: 500px) {
  /* If the screen is wider then 500px, use Flexbox */
  .container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-flow: row nowrap;
    flex-flow: row nowrap;
  }
  .c1 {
    position: relative;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
  .c2 {
    position: static;
  }
}

@media (min-width: 800px) {
  body {
    overflow-x: auto;
  }
  .c3 {
    position: relative;
    left: auto;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
}
```

### CSS/SCSS寫法（二）
```scss
@import "./vars.scss";

body {
  margin: 0;
  overflow-x: hidden;
}

.container {
  display: block;
  margin: 0;
  padding: 0;
  width: 100%;
  color: white;
}

.container div {
  box-sizing: border-box;
  min-height: 150px;
  min-width: 150px;
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

.c5 {
  background-color: #dfe1e5;
}


.c1, .c3 {
  position: absolute;
  width: 250px;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden; 

  -webkit-transition: -webkit-transform 0.4s ease-out;
  transition: transform 0.4s ease-out;
  
  z-index: 1;
}

.c1 {
  -webkit-transform: translate(-250px,0);
  transform: translate(-250px,0);
}

.c1.open {
  -webkit-transform: translate(0,0);
  transform: translate(0,0);
}

.c2 {
  width: 100%;
  position: absolute;
}

.c3 {
  left: 100%;
}

.c3.open {
  -webkit-transform: translate(-250px,0);
  transform: translate(-250px,0);
}

@include xs{
  .container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-flow: row nowrap;
    flex-flow: row nowrap;
  }
  .c1 {
    position: relative;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
  .c2 {
    position: static;
  }
}

@include sm{
  /* If the screen is wider then 500px, use Flexbox */
  .container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-flow: row nowrap;
    flex-flow: row nowrap;
  }
  .c1 {
    position: relative;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
  .c2 {
    position: static;
  }
}

@include lg{
  body {
    overflow-x: auto;
  }
  .c3 {
    position: relative;
    left: auto;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
}
```

### CSS/SCSS寫法（三）
```scss
@import "./vars.scss";

body {
  margin: 0;
  overflow-x: hidden;

  @include lg{
    overflow-x: auto;
  }
}

.container {
  display: block;
  margin: 0;
  padding: 0;
  width: 100%;
  color: white;

  @include xs{
    display: -webkit-flex;
    display: flex;
    -webkit-flex-flow: row nowrap;
    flex-flow: row nowrap;
  }
  @include sm{
    display: -webkit-flex;
    display: flex;
    -webkit-flex-flow: row nowrap;
    flex-flow: row nowrap;
  }
}

.container div {
  box-sizing: border-box;
  min-height: 150px;
  min-width: 150px;
}

.c1 {
  background-color: #003476;
  position: absolute;
  width: 250px;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden; 

  -webkit-transition: -webkit-transform 0.4s ease-out;
  transition: transform 0.4s ease-out;
  
  z-index: 1;

  -webkit-transform: translate(-250px,0);
  transform: translate(-250px,0);

  @include xs{
    position: relative;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
  @include sm{
    position: relative;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
}
.c1.open {
  -webkit-transform: translate(0,0);
  transform: translate(0,0);
}

.c2 {
  background-color: #0062d2;
  width: 100%;
  position: absolute;

  @include xs{
    position: static;
  }
  @include sm{
    position: static;
  }
}

.c3 {
  background-color: #b4d2f7;
  position: absolute;
  width: 250px;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden; 

  -webkit-transition: -webkit-transform 0.4s ease-out;
  transition: transform 0.4s ease-out;
  
  z-index: 1;

  left: 100%;

  @include lg{
    position: relative;
    left: auto;
    -webkit-transition: none 0s ease-out;
    transition: none 0s ease-out;
    -webkit-transform: translate(0,0);
    transform: translate(0,0);
  }
}
.c3.open {
  -webkit-transform: translate(-250px,0);
  transform: translate(-250px,0);
}

.c4 {
  background-color: #d5dfef;
}

.c5 {
  background-color: #dfe1e5;
}
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