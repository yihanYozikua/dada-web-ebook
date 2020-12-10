# CSS Property - Position

* ``` position ```：調整位置，元素的位置由 top、left、right、bottom 所決定
  * ``` static ```：由上而下、由左而右排列（Normal Flow）
  * ``` relative ```：相對位置
    * 相對於 **其它元素** 而定位 
  * ``` absolute ```：絕對位置
    * 當網頁往下拉時，元素也會跟著改變位置
    * 通常使用：元素需要重疊的狀況
  * ``` fixed ```：固定位置
    * 相對於 **瀏覽器** 而定位
    * 也就是說不管滑到哪裡，user看到他的位置永遠不變
    * 網頁被捲動的時候，被 ``` fixed ``` 的元素會固定不動
  * ``` sticky ```
    * 通常使用：頁面頂部的導覽列
    ```scss
    position: static; /*預設值，如果position設定成這個，top / left / bottom / right 會變得沒作用*/
    position: relative;
    position: absolute;
    position: fixed;
    position: sticky; 
    ```

      **使用sticky時，記得要再多設定元素位置唷**
      ```scss
      position: sticky;
      top: 0;
      ```
        
  * 上下左右位置（ ``` top ``` / ``` bottom ``` / ``` left ``` / ``` right ``` ）
    ```scss
    top: 20vh; /*上到下計算*/
    bottom: 10vh; /*下到上計算*/
    left: 10vw; /*左到右計算*/
    right: 20vw; /*右到左計算*/
    ```