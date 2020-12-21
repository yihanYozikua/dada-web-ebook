# CSS動畫
> 動畫大全
> 可以用css做出簡易動畫！

* CSS動畫property有以下這些
  * ``` animation-name ```：動畫名稱
  * ``` animation-duration ```：動畫持續時間
  * ``` animation-delay ```：動畫延遲播放時間
  * ``` animation-iteration-count ```：動畫播放次數
  * ``` animation-timing-function ```：動畫加速度函式（移動模式）
  * ``` animation-direction ```：動畫播放方向
  * ``` animation-fill-mode ```：動畫播放前後模式
  * ``` animation-play-state ```：動畫狀態（播放or暫停）
  * ``` animation ```：以上所有屬性可以用這個property一起設定
    ```scss
    animation: name | duration | timing-function | delay | iteration-count | direction | fill-mode | play-state;
    ```
  * 當然也可以用JS控制
  <br><br>


* 話不多說，先來個簡易示範
* 以下是個會左右移動、並漸漸變色的方框

```html
<div class="test"></div>
```

```scss
.test{
  position: absolute;
  left: 0;
  background-color: aquamarine;
  width: 200px;
  height: 200px;
  animation-name:t-anim;
  animation-duration: 1s;
}


@keyframes t-anim{
  0%{
    left: 0;
    background-color: blue;
  }
  50%{
    left: 100px;
    background-color: brown;
  }
  100%{
    left: 0;
    background-color: blue;
  }
}
```

* ``` keyframes ```：就相當於AE裡面的關鍵影格，不過這裡是以%來表示
* 注意事項
  * 如果沒有寫清楚開頭或結尾要做什麼，程式會自動幫我們演算出來（但是呈現效果就不見得會跟我們預期的一樣）
  * 不可單獨寫數字，一定要加上%
  * 如果寫了同樣的百分比數和同樣的屬性，則後面的屬性會覆蓋前面的
  * 可以一個元素套用多個動畫

```scss
.test{
  position: absolute;
  left: 0;
  background-color: aquamarine;
  width: 200px;
  height: 200px;
  animation-name:t-anim;
  animation-duration: 1s;
  animation: t-anim 1s ease-in infinite both, rotate 4s infinite both;
}

@keyframes t-anim{
  0%{
    left: 0;
    background-color: blue;
  }
  50%{
    left: 100px;
    background-color: brown;
  }
  100%{
    left: 0;
    background-color: blue;
  }
}

@keyframes rotate{
  0%{
    -webkit-transform: rotate(0deg);
  }
  50%{
    -webkit-transform: rotate(90deg);
  }
  100%{
    -webkit-transform: rotate(180deg);
  }
}
```