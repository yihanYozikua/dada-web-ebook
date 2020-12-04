# CSS Property - Box Model - Flexbox
> Flexbox：是其中一種box model

  ![](https://i.imgur.com/IdMERjU.jpg)

  * 有以下css屬性
    * ``` display ```：跟顯示方式有關的設定

    ```scss
    display: inline; /*內容多長空間就有多大，不強迫換行*/
    display: block; /*佔一整行，強迫換行*/
    display: flex; /*可以設定長寬，強迫換行*/
    display: inline-block; /*可以設定長寬，不強迫換行*/
    display: inline-flex; /*可以設定長寬，不強迫換行*/
    /* inline-＿＿ 可以想成是inline裡面包＿＿ */
    display: none; /*不顯示*/
    ```
    
    ![](https://i.imgur.com/2d0WnGg.jpg)

  **注意**
  **以下所有屬性都要記得先在CSS中設定 ```display: flex;```或```display: inline-flex;``` 才能發揮作用**
  
  * ``` flex-direction ```：元素排列方向

  ```html
  <div class="flex">
  <div class="text" style="background-color: thistle;">第一行</div>
  <div class="text" style="background-color: teal;">第二行</div>
  <div class="text" style="background-color: wheat;">第三行</div>
  </div>
  ```

  ``` flex-direction ``` 寫在外框，不是寫在元素上

  ```scss
  .flex{
      display: flex;
      flex-direction: row; /*全部子元素排成一列*/
      flex-direction: row-reverse; /*全部子元素排成一列，而且排列方向跟html裡面寫的顛倒*/
      flex-direction: column; /*全部子元素排成一行*/
      flex-direction: column-reverse; /*全部子元素排成一行，而且排列方向跟html裡面寫的顛倒*/
  }
  ```

  * ``` justify-content ```：「內容」與整個flexbox的「水平對齊」位置
  
  ```html
  <div class="flex">
      <div class="text" style="background-color: thistle;">第一行</div>
      <div class="text" style="background-color: teal;">第二行</div>
      <div class="text" style="background-color: wheat;">第三行</div>
  </div>
  ```
  
  ```scss
  /*練習的時候，記得要設定height才看得出來差別*/
  .flex{
      display: flex;
      height: 30em;
      justify-content:flex-start; /* 預設值，對齊最左邊main start */
      justify-content:flex-end; /* 對齊最右邊main end */
      justify-content:center; /* 水平置中 */
      justify-content:space-between; /* 平均分配內容元素，左右元素將會與 main start 和 main end 貼齊，最左的靠最左、最右的靠最右 */
      justify-content:space-around; /* 元素的左右邊留白不一樣，平均分配內容元素，間距也是平均分配 */
  }         
  ```
  
  * ``` align-items ```：「內容」與整個flexbox的「垂直對齊」位置
  
  ```html
  <div class="flex">
      <div class="text" style="background-color: thistle;">第一行</div>
      <div class="text" style="background-color: teal;">第二行</div>
      <div class="text" style="background-color: wheat;">第三行</div>
  </div>
  ```

  ```scss
  .flex{
      display: flex;
      align-items: flex-start; /*置頂對齊*/
      align-items: flex-end; /*置底對齊*/
      align-items: center; /*置直置中*/
      align-items: stretch; /*元素的高度拉長到與flexbox相同，在沒有設定元素高度時，把元素拉到與空間上下滿版*/
      align-items: baseline; /*以元素裡面的值（如：字）的基線（元素本身的最底部）作為對齊標準*/
  }
  ```

  * ``` align-self ```：用來覆寫（覆蓋）``` align-items ``` 的設定，通常直接針對子元素設定

  ```scss
  align-self: flex-start; /*置頂對齊*/
  align-self: flex-end; /*置底對齊*/
  align-self: center; /*置直置中*/
  align-self: stretch; /*元素的高度拉長到與flexbox相同*/
  align-self: baseline; /*以元素的基線（元素本身的最底部）作為對齊標準*/
  ```

  * ``` align-content ```：延續上述，上面那個是針對「單行」元素進行調整，這個則是針對「多行」元素進行調整
  ```scss
  align-content: flex-start; /*對齊最上面的cross start*/
  align-content: flex-end; /*對齊最下面的cross end*/
  align-content: center; /*垂直置中*/
  align-content: space-between; /*將第一行與最後一行分別對齊最上方與最下方*/
  align-content: space-around; /*每行平均分配間距*/
  align-content: stretch; /*預設值，內容元素全部撐開*/
  ```
  
  * ``` flex-wrap ```：讓內容元素換行
  
  ```scss
  flex-wrap: nowrap; /*預設值，不會換行，內容元素寬度會隨著視窗做調整*/
  flex-wrap: wrap; /*根據元素本身寬度、與視窗的寬度，決定是否要換行*/
  flex-wrap: wrap-reverse; /*根據元素本身寬度、與視窗的寬度，決定是否要換行，而且一但換行，元素的排列順序會與原來顛倒*/
  ```
  
  * ``` order ```：直接指定元素的排列順序
  
  ```html
  <div class="flex">
      <div class="obj1">第一個</div>
      <div class="obj2">第二個</div>
      <div class="obj3">第三個</div>
  </div>
  ```
  
  ```scss
  .obj1{
      order: 3;
  }
  .obj2{
      order: 1;
  }
  .obj3{
      order: 2;
  }
  ```

  * ``` flex ```
    * **flexbox裡面最重要（也最難）的屬性！**
    * 概念理解
      * 子元素與父元素比較，比size誰大誰小
        * 子 < 父（子比較小），則採用 ``` flex-grow ``` 的比例，伸展比例（也就是說「要伸展多少」）
        * 子 > 父（子比較大），則採用 ``` flex-shrink ``` 的比例，壓縮比例（也就是說「要壓縮多少」）
                        
        * 由3種屬性組合而成
          * ``` flex-grow ```：當子元素的 flex-basis 長度「小」於它自己在父元素分配到的長度，按照數字做相對應的「伸展」比例分配
            * 數字，無單位（數字代表的是比例）
            * 預設值為 0
            * 不可為負值
            * 設定為 1 則會進行彈性變化
          * ``` flex-shrink ```：當子元素的 flex-basis 長度「大」於它自己在父元素分配到的長度，按照數字做相對應的「壓縮」比例分配
            * 數字，無單位
            * 預設值為 1
            * 不可為負值
            * 設為 0 的話會沒反應
          * ``` flex-basis ```：子元素的基本大小，作為父元素的大小比較基準
            * 預設值為 0
            * 因為預設值為 0，所以如果沒有設定此屬性的話，會以直接採用 flex-grow 屬性（也就是說會直接按比例分配長度）
            * 也可以設為``` auto ```
          
          ```html
          <div class="flex">
              <div class="obj1">第一個</div>
              <div class="obj2">第二個</div>
              <div class="obj3">第三個</div>
          </div>
          ```
        ```scss
            .flex{
              display: flex;
            }
            .obj1{
              flex: 2 2 200px;
            }
            .obj2{
              flex: 5 5 200px;
            }
            .obj3{
              flex: 3 3 200px;
            }
        ```