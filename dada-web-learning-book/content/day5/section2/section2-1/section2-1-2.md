# ::first-line / ::first-letter / ::selection

### ::first-line
* 指定「第一行文字」
* **不能**作用於 ``` display: inline; ```元素

> 如果照下面那樣寫，第一行文字就會呈現藍綠色

```html
<div>
  <p class="test">我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼我是大大幼稚鬼</p>
</div>
```

```scss
.test::first-line{
  color: burlywood;
}
```
![](https://i.imgur.com/5LOYDRb.png)
<br>

> 但如果在css中加入了以下code，則 ```  ::first-line ``` 就沒用ㄌ

```scss
.test{
  display: inline;
}
```
![](https://i.imgur.com/TElmc6B.png)

---

### ::first-letter
* 指定「第一個文字」
* 利用這個效果，可以做到文章首字放大、首字變色的效果

```scss
.test::first-letter{
  font-style: italic;
  font-size: 10vh;
}
```
![](https://i.imgur.com/9NAqtdH.png)

---

### ::selection
* 指定反白（選取）文字的格式

```scss
.test::selection{
  color: rgb(255, 255, 255);
  background-color: blue;
}
```

![](https://i.imgur.com/G7dvTDY.png)
<br>

![](https://i.imgur.com/LGasBCa.png)