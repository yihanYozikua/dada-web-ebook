# CSS Property - Box Model - Margin / Padding / Border / Box-sizing
> Margin / Padding / Border / Box-sizing

![](https://i.imgur.com/C3eD5IG.jpg)
        
* 設定順序：margin => padding => border => box-sizing

#### Margin
* ``` margin ```：跟其他物件的距離（外框距離）
  * 有四個方向：上 右 下 左
  * 顏色是透明的
  * 如果同時設定``` display: inline; ```，則``` margin-top ``` ``` margin-bottom ```的設定會沒有效果
  * 值可以是負的
  * 有 ``` auto ``` 這個性質

  ```scss
  /*簡潔寫法*/
  margin: 10em 5em 20em 3em; /*上 右 下 左*/
  margin: 10em 5em; /*上下 左右*/
  margin: 10em 5em 7em; /*上 左右 下*/
            
  /*auto: 表示「剩下的可用空間」*/
  margin: 0 auto; /*讓「區塊本身」水平置中*/
  margin-left: auto; /*剩下的可用空間都給左邊，所以會靠右對齊*/
            
  /*四個方向分開寫*/
  margin-left: 2em;
  margin-right: 3em;
  margin-top: 5em;
  margin-bottom: 7em;
  ```

#### Padding
* ``` padding ```：物件跟邊界的距離，類似出血（內部留白）
  * 有四個方向：上 右 下 左
  * ``` padding ```區塊的顏色就是 ``` background-color ``` 的設定值
  * 會被 ``` box-sizing ``` 影響
  * 值不能是負的
  * 沒有 ``` auto ``` 這個性質
  
  ```scss
  /*簡潔寫法*/
  padding: 10em 5em 20em 3em; /*上 右 下 左*/
  padding: 10em 5em; /*上下 左右*/
  padding: 10em 5em 7em; /*上 左右 下*/
            
  /*四個方向分開寫*/
  padding-left: 2em;
  padding-right: 3em;
  padding-top: 5em;
  padding-bottom: 7em;
  ```


#### Border
* ``` border ```：邊框
  * 樣式（長相）
    * ``` solid ```，實線
    * ``` dashed ```，虛線
    * ``` double ```，雙線
    * ``` dotted ```，點點線
    * ``` groove ```，凹槽
    * ``` ridge ```，凸起
    * ``` inset ```
    * ``` outset ```，巧克力感
    ```scss
    /*單純設定邊框粗細*/
    border: 10em;
            
    /* 同時設定 尺寸 樣式 顏色 */
    border: 10em solid blue;
    ```

#### Box-Sizing
* ``` box-sizing ```：用來調整區塊的內距與邊框計算方式
    ```scss
    /* <div>設定的寬度 = 內容寬度，不包含padding和border */
    box-sizing: content-box;
            
    /* <div>設定的寬度 = 內容寬度 + padding + border*/
    box-sizing: border-box;
            
    /* 繼承外層的box-sizing設定值 */
    box-sizing: inherit;/*跟“親”一樣*/
    ```

    ![](https://i.imgur.com/xtiD6He.jpg)

#### Width / Height
* ``` width ```  ``` height ```：設定物件的長寬
  ```scss
  width: 7em
  height: 7em;
  ```