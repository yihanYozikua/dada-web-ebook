# 提問時間

#### Viewport
  * 語法：如何在小螢幕（手機）之內，調整適合使用者的閱讀解析度
    * ``` width=device-width ```
        * 手機品牌太多ㄌ，這個是用來設定「自動符合所有不同手機螢幕」的預設最佳解析度
    * ``` initial-scale=1.0 ```
        * 設定手機螢幕畫面的預設縮放比例 = 100%
    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```
    * ``` shrink-to-fit=no ```
      * Safari 9.0 的特定語法
      * 如果元素的大小實際上超過裝置尺寸時，如：手機576px / 圖片750px
      * 不允許瀏覽器自動縮放元素至fit螢幕尺寸
      ```html
      <meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no">
      ```
      ![](https://i.imgur.com/fvPPwUb.jpg)
    
#### Common.js
  * 單純代表 ``` require ``` ``` export ```這兩個語法
  * 重要性：讓「引用library」這件事變得簡單
  * [大大學網頁Day2 前端關鍵字/引入Library的機制, ES6](https://hackmd.io/@YsV3H6xcTLyIarrux1RSmA/r1kHBQsuv)

#### 文件開頭
  * 定義這份html的主要語言
  ```html
  <html class="" lang="jp"> </html>
  <html class="" lang="en"> </html>
  ```