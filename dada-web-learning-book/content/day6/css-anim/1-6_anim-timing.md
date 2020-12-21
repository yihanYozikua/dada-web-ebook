# Animation-timing-function-function

* ``` animation-timing-function ```就是**動畫加速函式**（類似過場效果）
* 有以下幾種
  * 連續系列：每個關鍵影格之間，程式會自動演算出中間沒設定的部分
    * ``` linear ```
    * ``` ease ```
    * ``` ease-in ```
    * ``` ease-out ```
    * ``` ease-in-out ```
  * 分段系列：基本上只會呈現出有設定的部分，看起來會有段落感
    * ``` step-start ```：會略過第一格
    * ``` step-end ```：會略過最後一格
    * ``` steps(int, start|end) ```
    ```scss
    steps( 每個%的設定之間要插入幾格影格, 略過第一格|略過最後一格)
    ```

### 連續系列
#### linear
![](https://i.imgur.com/qoGFZHZ.png)

#### ease
![](https://i.imgur.com/9aNXvw4.png)

#### ease-in
![](https://i.imgur.com/NbTuL5K.png)

#### ease-out
![](https://i.imgur.com/wqhoZGs.png)

#### ease-in-out
![](https://i.imgur.com/TL7WqfT.png)

<br><br>

### 分段系列
#### steps(int, start|end)
```scss
steps( 每個%的設定之間要插入幾格影格, 略過第一格|略過最後一格)
```
* int被設定的數字越大，動畫看起來會越流暢
* steps(int, start)
  * 有被設定的影格與影格之間，插入 int 個影格；跳過第一格後開始播放
* steps(int, end)
  * 有被設定的影格與影格之間，插入 int 個影格；播放時跳過最後一格

```scss
.test{
  position: absolute;
  left: 0;
  background-color: aquamarine;
  width: 200px;
  height: 200px;
  animation-name:t-anim;
  animation-duration: 1s;
  animation-delay: 0s;
  animation-iteration-count: infinite;
  animation-timing-function: steps(10, start);
  // 有被設定的影格與影格之間，插入10個影格；跳過第一格後開始播放
}


@keyframes t-anim{
  0%{
    left: 0;
    background-color: red;
  }
  25%{
    left: 250px;
    background-color: orange;
  }
  50%{
    left: 500px;
    background-color: yellow;
  }
  75%{
    left: 700px;
    background-color: green;
  }
  100%{
    left: 900px;
    background-color: blue;
  }
}
```

#### step-start
* 相當於 ``` animation-timing-function: steps(1, start); ```

#### step-end
* 相當於 ``` animation-timing-function: steps(1, end); ```