# CSS Property - Font

* ``` font ```
  * ``` font-size ```：大小
  * ``` font-weight ```：粗細
  * ``` color ```
  * ``` font-family ```
  
  ```scss
  font-weight: normal;
  font-weight: bold;
  font-weight: bolder;
  font-weight: lighter;
  font-weight: 400; /*400 = normal, 700 = bold*/
    
  font-family: "Arial", "Noto Sans TC", "Microsoft JhengHei", sans-serif;
  ```
  * 引入外部字體
    * 先去下載字體
    * 需要以下格式，通常是先下載一種然後拿去轉檔
    [可用轉檔連結](https://www.font-converter.net/en)
      * .eot
      * .otf
      * .svg
      * .ttf
      * .woff
    * 轉好檔案後，把這些檔案加入你的project中
    * 在css中撰寫以下的code
    ```scss
    @font-face {
      font-family: "Nagurigaki-Crayon"; /*這就是你的字體名稱，會用在font-family上*/
      src: url("./fonts/crayon.eot"); /* IE9 Compat Modes */
      src: url("./fonts/crayon.eot?#iefix") format("embedded-opentype"), /* IE6-IE8 */
        url("./fonts/crayon.otf") format("opentype"), /* Open Type Font */
        url("./fonts/crayon.svg") format("svg"), /* Legacy iOS */
        url("./fonts/crayon.ttf") format("truetype"), /* Safari, Android, iOS */
        url("./fonts/crayon.woff") format("woff"), /* Modern Browsers */
        url("./fonts/crayon.woff2") format("woff2"); /* Modern Browsers */
      font-weight: normal;
      font-style: normal;
    }
    body{
      font-family: "Nagurigaki-Crayon";
    }
    ```