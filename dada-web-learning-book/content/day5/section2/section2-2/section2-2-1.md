# 動態
``` :link ```  ``` :visited ```  ``` :hover ```  ``` :active ```  ``` :focus ```

* 通常使用在超連結上
* ``` :link ```：還沒造訪過的連結
* ``` :visited ```：點過的連結
* ``` :hover ```：滑鼠滑過的時候的效果
* ``` :active ```：點下去的瞬間

```html
<a href="https://dada-web-ebook-yihanyozikua.gitbook.io/dada-web-learning-ebook/" target="_blank">大大學網頁EBook</a>
```

```scss
a:link{
  color: black;
}
a:visited{
  color: lightblue;
}
a:hover{
  color: gold;
}
a:active{
  color: green;
}
```

* 通常使用在填表單的時候
* ``` :focus ```：標示目前正在填哪一格

```html
<form>
  回政大午餐要吃什麼：<input type="text" name="lunch" placeholder="阿里郎"><br>
  最想要的唇膏色號：<input type="text" name="color" placeholder="那個我其實也不知道色號會怎麼寫">
</form>
```

```scss
input:focus{
  background-color: gold;
}
```

![](https://i.imgur.com/qZDXMrw.png)