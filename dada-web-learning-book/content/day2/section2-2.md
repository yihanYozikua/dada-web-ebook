## JS (Vanilla.js)
* 名詞解釋
    * ES6：是指JS的語言版本
    * Vanilla JS（原生JS）：沒有用到別的library（別的library：React / jQuery），比如說我們以前修的進階程式設計
* 建議去複習[峻鋒的JS講義](https://drive.google.com/drive/folders/1uSsAgjKSDkTLMXu_J-bVmPAz40XCHkp1?usp=sharing)
* 怎麼從JS裡面取得HTML裡的元素
```html
<!-- 如果要讓js能夠控制html的話，要把下面這行加到 html </body>的上面 -->
<script src="js/檔名.min.js"></script>
```
```js
document.getElementById('id名稱').innerHTML = "希望取得的元素變成怎樣";" //innerHTML取得「內文」
document.getElementById('id名稱').style.CSS屬性 = "希望取得的元素變成怎樣";" //style.CSS屬性取得「屬性」（property）
```
```js
//當然，也可以把document.getElementById參數化
var text = document.getElementById('text').innerHTML;
//接下來針對 text 操作就好
.
.
.
```