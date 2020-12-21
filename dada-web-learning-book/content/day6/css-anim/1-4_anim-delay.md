# Animation-delay

* ``` animation-delay ```就是**延後多久才開始播放**
* 單位：s（秒） / ms（毫秒）
* 預設值：0s（就是沒有延遲的意思）
* 如果設定成**負值**，則會快轉
  * 假設一段動畫從頭到尾完整播完有5秒，而設定 ``` animation-delay: -2s; ```，則動畫會將前面的2秒快轉掉，從第3秒開始播，播完3秒後停止

```html
<div class="test"></div>
<div class="test2"></div>
<div class="test3"></div>
```

```scss
.test{
  position: absolute;
  left: 0;
  background-color: aquamarine;
  width: 200px;
  height: 200px;
  animation-name:t-anim;
  animation-duration: 5s;
  animation-delay: 0s; //從頭開始播放，沒有延遲、沒有快轉
}
.test2{
  position: absolute;
  left: 0;
  background-color: aquamarine;
  width: 200px;
  height: 200px;
  animation-name:t-anim;
  animation-duration: 5s;
  animation-delay: -2s; //快轉兩秒播放
}
.test3{
  position: absolute;
  left: 0;
  background-color: aquamarine;
  width: 200px;
  height: 200px;
  animation-name:t-anim;
  animation-duration: 5s;
  animation-delay: 2s; //延遲兩秒播放
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