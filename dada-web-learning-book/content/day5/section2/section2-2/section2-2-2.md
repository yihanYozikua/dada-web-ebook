# 目標
``` :target ```

* 用來指定被指到的目標該長啥樣

```html
<ul>
  <li><a href="#p1">第一個</a></li>
  <li><a href="#p2">第二個</a></li>
  <li><a href="#p3">第三個</a></li>
</ul>
  
<p id="p1">
  這裡是第一段文字這裡是第一段文字這裡是第一段文字這裡是第一段文字這裡是第一段文字這裡是第一段文字
</p>
    
<p id="p2">
  這裡是第二段文字這裡是第二段文字這裡是第二段文字這裡是第二段文字這裡是第二段文字這裡是第二段文字
</p>

<p id="p3">
  這裡是第三段文字這裡是第三段文字這裡是第三段文字這裡是第三段文字這裡是第三段文字這裡是第三段文字
</p>
```

```scss
p:target{
  background-color: gold;
}
```
![](https://i.imgur.com/6tV6Z9j.png)
<br>

```scss
p:target::before {
  font: 70% sans-serif;
  content: "( ´ ▽ ` )ﾉ";
  color: rgb(119, 115, 101);
  margin-right: .25em;
}
```
![](https://i.imgur.com/lzbebfn.png)