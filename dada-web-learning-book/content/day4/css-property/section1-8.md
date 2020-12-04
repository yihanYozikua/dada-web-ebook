# CSS Property - Text-decoration

* ``` text-decoration ```：底線、刪除線
  * underline
  * line-through
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
    text-decoration: underline;
  }
  ```
  * 寫法 #2
  ```html
  <div class="text-decorate">
    <p>我是示範區</p>
    <p>我是示範區</p>
    <p>我是示範區</p>
  </div>
  ```
  ```scss
  .text-decorate{
    text-decoration: underline red;
  }
  ```