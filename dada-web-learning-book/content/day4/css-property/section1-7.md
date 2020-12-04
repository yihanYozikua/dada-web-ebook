# CSS Propety - Text

* ``` text ```
  * ``` text-align ```：文字對齊方式
    * ``` left ```
    * ``` right ```
    * ``` center ```
    * 寫法 #1
    ```html
    <div>
      <p>我是示範區</p>
      <p>我是示範區</p>
      <p>我是示範區</p>
    </div>
    ```
    ```scss
    p{
      text-align: center;
    }
    ```
    * 寫法 #2
    ```html
    <div class="text-alignment">
      <p>我是示範區</p>
      <p>我是示範區</p>
      <p>我是示範區</p>
    </div>
    ```
    ```scss
    .text-alignment{
      text-align: center;
    }
    ```
    * ``` line-height ```：行高
    ```scss
    line-height: normal;
    line-height: 1.6;
    line-height: 80%;
    line-height: 4vh;
    ```
    * 寫法 #1
    ```html
    <div>
      <p>我是示範區</p>
      <p>我是示範區</p>
      <p>我是示範區</p>
    </div>
    ```
    ```scss
    p{
      line-height: 2vh;
    }
    ```
    * 寫法 #2
    ```html
    <div class="text-line-height">
      <p>我是示範區</p>
      <p>我是示範區</p>
      <p>我是示範區</p>
    </div>
    ```
    ```scss
    .text-line-height{
      line-height: 2vh;
    }
    ```