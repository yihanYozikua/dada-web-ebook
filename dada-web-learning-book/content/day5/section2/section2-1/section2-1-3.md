# content

* ``` content ```可以使用 ``` attr ```來直接取得html元素內容的屬性

```html
<a class="test" href="https://dada-web-ebook-yihanyozikua.gitbook.io/dada-web-learning-ebook/" target="_blank">DADA Web</a>
```

```scss
.test::before{
  content: attr(href);
  color: rosybrown;
}
.test::after{
  content: attr(target);
  color: lightblue;
}
```


* ``` content ```內容可以**相加**
  * 可以一次把好幾個內容寫在一起，放在 ``` content ```裡面
  * 每個內容以一個空白符號隔開

```scss
.test::before{
  content: "(" attr(href) attr(target) ")";
  color: rosybrown;
}
```


* 甚至可以用url放入圖片，再把這個url放進``` content ```裡面

```scss
.test::before{
  content: url("https://images-tw.girlstyle.com/wp-content/uploads/2019/05/21abbbb3cbf8e7f191335a5441bf77dc.jpg") attr(href) attr(target);
  color: rosybrown;
}
.test::after{
  content: "";
  color: lightblue;
}
```

---

### content搭配quote使用

* ``` quotes ```
  * 是一種css屬性，不太常用
  * 用來定義 **括號格式**

* ``` <q> ```
  * 是一種html tag
  * 如果一段文字被 ``` <q> ``` 包住，這段文字的前後就會出現我們自定義的括號
  
```html
<div class="test">
  最外層
  <q>
    第一層
    <q>
      第二層
      <q>
        最裡面
      </q>
    </q>
  </q>
</div>
```

```scss
.test q{
  quotes: '{' '>' ;
}
```
![](https://i.imgur.com/pprjBO7.png)

<br>
* 但其實我們也可以不使用 ``` <q> ```就達到自定義括號的效果
* 就是運用 ```  content ``` ``` ::before ``` ``` ::after ```
* 如此一來，前後括號的樣式也能分開寫ㄌ！

```html
<div class="test">
  最外層
  <span>
    第一層
    <span>
      第二層
      <span>
        最裡面
      </span>
    </span>
  </span>
</div>
```

```scss
.test span{
  quotes: '<' '>' 'da' 'da' 'yi' 'yi';
}
.test span::before{
  content: open-quote;
  color: bisque;
}
.test span::after{
  content: close-quote;
  color: lightblue;
}
```

![](https://i.imgur.com/buuqQAy.png)