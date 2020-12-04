# CSS Property - Background

* ``` background ```
  * [background-color](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)：背景顏色
  * [background-image](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image)：背景圖片
  * [background-attachment](https://developer.mozilla.org/zh-TW/docs/Web/CSS/background-attachment)：背景圖片是否固定
  * [background-position](https://developer.mozilla.org/zh-TW/docs/Web/CSS/background-position)：位置（座標）
  * [background-repeat](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat)：是否重複
  

  ```scss
  background-color: blue;
        
  background-image: none; /*沒背景圖片*/
  background-image: url("test.jpg");
  background-image: url("這裡可以放網路圖片url");
        
        
  background-attachment: fixed; /*不管視窗如何捲動，bg-img永遠停在可見範圍的左上角*/
  background-attachment: scroll; /*背景圖會隨著視窗滾動而移動*/
        
  background-position: 137px 119px; /*(x, y)*/ /*長度+單位*/
  background-position: center center; /*上下左右置中對齊*/
    
        
  background-repeat: repeat; /*重複*/
  background-repeat: repeat-x; /*水平重複*/
  background-repeat: repeat-y; /*垂直重複*/
  background-repeat: no-repeat; /*不重複*/
  background-size: auto;
  ```