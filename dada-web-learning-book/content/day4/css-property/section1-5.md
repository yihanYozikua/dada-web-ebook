# CSS Property - Float / Clear

* ``` float ``` / ``` clear ```：文繞圖，排版用
  * ``` float ```
    ```html
    <div>
      <div class="float-div-left"></div>
      文字繞著浮動的圖片、文字繞著浮動的圖片、文字繞著浮動的圖片、文字繞著浮動的圖片
    </div>
    ```
    ```scss
    .float-div-left{
      height: 150px;
      width: 150px;
      background-color: rgb(106, 172, 248);
      float: right;
    }
    ```

    ![](https://i.imgur.com/iS5y68y.png)
    效果像上面這樣
    

  * ``` clear ```：用來清除``` float ```屬性
    * ``` left ```：清除（前一個元素的）左邊``` float ```
    * ``` right ```：清除（前一個元素的）右邊``` float ```
    * ``` both ```：（前方有兩個元素的）兩邊``` float ```都清除
    ```html
    <div>
        <div class="float-div-left"></div>
        <div class="float-div-right"></div>
    </div>
    ```
    ```scss
    .float-div-left{
      height: 150px;
      width: 150px;
      background-color: rgb(106, 172, 248);
      float: left;
    }
    .float-div-right{
      height: 150px;
      width: 150px;
      background-color: rgb(248, 203, 106);
      float: left;
      clear: left
    }
    ```