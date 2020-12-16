# UI元素狀態
``` :enabled ```  ``` :disabled ```  ``` :checked ``` ``` :unchecked ```

#### Enabled & Disabled
```html
<form>
  你的名字：<input type="text" placeholder="大大"><br>
  你的聖誕節禮物是：<input type="text" value="還不能說" disabled>
</form>
```

```scss
input:enabled{
  background-color: rgb(176, 204, 204);
  border-color: transparent;
  color: white;
}
input:disabled{
  background-color: gray;
}
```

#### Checked & Unchecked
```html
<form>
  以下的日子哪天要出去玩：<input type="checkbox" value="1212" unchecked disabled>12/12&nbsp;&nbsp;&nbsp;
  <input type="checkbox" value="1223" unchecked>12/23&nbsp;&nbsp;&nbsp;
  <input type="checkbox" value="1225" checked>12/25&nbsp;&nbsp;&nbsp;
  <input type="checkbox" value="1226" checked>12/26&nbsp;&nbsp;&nbsp;
  <br>>
  午餐吃甚麼好：<input type="checkbox" value="1" checked>拿玻里烤雞&nbsp;&nbsp;&nbsp;
  <input type="checkbox" value="2" unchecked>米粉湯&nbsp;&nbsp;&nbsp;
  <input type="checkbox" value="3">壽喜燒&nbsp;&nbsp;&nbsp;
  <input type="checkbox" value="4" disabled>以上都太狂了&nbsp;&nbsp;&nbsp;
</form>
```

```scss
input:checked{
  width: 100px;
  height: 100px;
}
```

![](https://i.imgur.com/cgebgib.png)