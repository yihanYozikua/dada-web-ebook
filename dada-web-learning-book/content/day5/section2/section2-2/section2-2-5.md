# 結構
> 這裡面可以分成 ``` -child ``` ``` - of-type ```兩類

``` :first-child ```  ``` :last-child ```  ``` :nth-child ```  ``` :nth-last-child ```  ``` :nth-of-type ```  ``` :nth-last-of-type ```  ``` :only-child ``` 
``` :first-of-type ```  ``` :last-of-type ``` ``` :nth-of-type ``` ``` :nth-last-of-type ``` ``` :only-of-type ```

### -child
* 用來指定 放在同一層內的所有元素中的第n個（全部人裡面的第幾個）
* 套在它外面的DOM就是他的父元素（親）
* 有以下幾種
  * ``` :first-child ```：第一個子元素
  * ``` :last-child ```：最後一個子元素
  * ``` :nth-child(數字) ```：第幾個子元素
  * ``` :nth-child(2n) ```：挑出偶數的元素(2的倍數)
  * ``` :nth-child(2n+1) ```：挑出奇數的元素
  * ``` :nth-last-child(數字) ```：從後面數來第幾個子元素
  * ``` :only-child ```：只有一個子元素時使用

#### :first-child
```html
<div>
  <ul class="text">
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
    <li>5</li>
    <li>6</li>
  </ul>
</div>
```

```scss
li{
  list-style:none;
  float:left;
  width:5vh;
  height:5vh;
  font-size: 3vh;
  background:burlywood;
  margin:5px;
}
li:first-child{
  color: red;
  background-color: gray;
}
```
![](https://i.imgur.com/vjvBByL.png)
<br>

#### :last-child
```scss
li:last-child{
  color: red;
  background-color: gray;
}
```
![](https://i.imgur.com/v3qt1xt.png)
<br>

#### :nth-child(數字)
```scss
li:nth-child(4){
  color: red;
  background-color: gray;
}
```

#### :nth-child(2n)
```scss
li:nth-child(2n){
  color: red;
  background-color: gray;
}
```
![](https://i.imgur.com/ZsX9Hjz.png)
<br>

#### :nth-child(2n+1)
```scss
li:nth-child(2n){
  color: red;
  background-color: gray;
}
```
![](https://i.imgur.com/ymkEsyF.png)
<br>

#### :nth-last-child(數字)
```scss
li:nth-last-child(3){
  color: red;
  background-color: gray;
}
```
![](https://i.imgur.com/jzRCuMI.png)
<br>

#### :only-child
```scss
li:only-child{
  color: red;
  background-color: gray;
}
```
![](https://i.imgur.com/L5AGYOB.png)
<br>

---

* 但有時候事情不會像上面那麼簡單，例如：
```html
<div id="test">
  <div>1</div>
  <span>2</span>
  <span>3</span>
  <section>4</section>
  <div>5</div>
  <section>6</section>
</div>
```
```scss
#test div, #test span, #test section {
  width:5vh;
  height:5vh;
  font-size: 3vh;
  display: inline-block;
  background:burlywood;
  margin:5px;
}
```
* 然後這時候，如果我們寫了
```scss
#test span:first-child{
  background: gray;
  color: red;
}
```
* ......就會發現完全沒反應，Why？
  * 因為 ``` -child ```指的是親之中的**所有**元素小孩。
  * 在上面的例子中，所有小孩中的第一個是 ``` <div> ```，可是因為我們指向 ``` <span> ```，所以這個CSS就不會被套用進去

* 所以，該怎麼解決呢？
  * 把 ``` -child ``` 改成 ``` -of-type ``` 就好啦

---

### -of-type
* 用來指定 放在同一層內的所有元素中的第n個（全部人裡面的第幾個）
* 有以下幾種
  * ``` :first-of-type ```：同一種元素的第一個
  * ``` :last-of-type ```：同一種元素的最後一個
  * ``` :nth-of-type ```：同一種元素裏頭的第幾個
  * ``` :nth-last-of-type ```：同一種元素從後面屬過來第幾個
  * ``` :only-of-type ```：只有這種元素

#### :first-of-type
```scss
#test span:first-of-type{
  background: gray;
  color: red;
}
```

#### :last-of-type
```scss
#test span:last-of-type{
  background: gray;
  color: red;
}
```

#### :nth-of-type()
```scss
#test span:nth-of-type(){
  background: gray;
  color: red;
}
```

#### :nth-last-of-type()
```scss
#test span:nth-last-of-type(){
  background: gray;
  color: red;
}
```

#### :only-of-type
* 只有孤身一人的時候才起作用

```html
<div id="test">
  <div>1</div>
  <span>2</span>
  <span>3</span>
  <div>5</div>
  <section>6</section>
</div>
```

```scss
#test section:only-of-type{
  background: gray;
  color: red;
}
```