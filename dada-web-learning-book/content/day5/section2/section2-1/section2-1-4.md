# JS 操控偽元素
> 因為CSS偽元素並不存在於html文件中，所以如果要使用JS控制的話，無法以正規的DOM方式來操控

### 如何以JS取得偽元素？
* ``` getComputedStyle ```
  * 使用方法：``` window.getComputedStyle('元素', '偽元素') ```
  * 可以取得當前元素「所有使用到的CSS property值」
  * 讀取後，return一個Object CSSStyleDeclaration，而這個物件是唯讀的，無法進行修改

```html
<div id="test-div">
  我是div
</div>
<span id="test-span">
</span>
```

```scss
#test-div::before{
  content: '偽元素的content';
  color: bisque;
}
```

```JS
var d = document.getElementById( 'test-div' );
var s = document.getElementById( 'test-span' );
var b = window.getComputedStyle( d, '::before' );
s.innerHTML = b.content + '<br>' + b.color ;
```

* 加上JS之前<br>
![](https://i.imgur.com/tPna3pP.png)

* 加上JS之後<br>
![](https://i.imgur.com/TPo3kv9.png)

---

### 如何以JS修改偽元素屬性？
* ``` insertRule ```
  * 先在 ```  <head> ``` 加上 ``` <style> ```
  * 再在JS中加上 ``` .sheet ```
  * 才可以使用 ``` .insertRule ``` 修改屬性

```html
<head>
  .
  .
  .
  <style id="css"></style>
</head>
<body>
  <div id="test-div">
    我是div
  </div>
  <span id="test-span">
  </span>
</body>
```

```scss
#test-div::before{
  content: '偽元素的content';
  color: bisque;
}
```

```JS
var css = document.getElementById( 'css' );
var d = document.getElementById( 'test-div' );
var modified = css.sheet;
modified.insertRule( "#test-div#test-div::before{color: red;}", 0 );
```

* 經過JS修改<br>
![](https://i.imgur.com/2rdnmwY.png)