# Bootstrap 4 (Grid / Utility)（*這一段是實作*）
[Bootstrap Doc](https://getbootstrap.com/docs/4.4/getting-started/introduction/)

* 引入 : 引入才能開始使用
    ```html
    <!-- 跟CSS有關 -->
    <!-- 把下面這行貼在<head>裡面的最前面 --> 
    <!-- 也可以直接寫在 topImport.ejs 裡面 -->
    <!-- Sample code "topImport.ejs #23" -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    
    <!-- 跟JS有關 -->
    <!-- 把下面這三行貼在</body>之前 --> 
    <!-- 也可以直接寫在 bottomImport.ejs 裡面 -->
    <!-- Sample code "bottomImport.ejs #1" -->
    <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>
    
    <!-- 這個跟行動裝置的顯示有關 -->
    <!-- 把下面這行貼在<head>裡面 -->
    <!-- 也可以直接寫在 topImport.ejs 裡面 -->
    <!-- Sample code "topImport.ejs #3" -->
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    ```
* Grid (跟RWD有關)
    * 斷點代碼 (以螢幕尺寸為分界的定義方式)
        * ___ : extra small, 6吋以下手機
        * sm : small, 6吋以上的手機
        * md : medium, iPad直式
        * lg : large, iPad橫式 / iPad Pro直式
        * xl : extra large, 電腦螢幕
    ```html
    col-斷點代碼-格數
    ```
    |                     | Extra Small | Small    | Medium   | large    | Extra Large |
    | ------------------- | ----------- | -------- | -------- | -------- | ----------- |
    |    裝置畫面寬度       | <576px      | >=576px  | >=768px  | >=992px  | >=1200px    |
    | max container width | None(auto)  | 540px    | 720px    | 960px    | 1140px      |
    | Class Prefix        | col-       | col-sm- | col-md- | col-lg- | col-xl-    |
    | Total columns       |     12      |   12     |  12      |    12    |      12     |

    * 特別說明 : 如果要讓欄位寬度平均分配，則不要寫格數就好
    ```
    col-sm  #裝置畫面寬度在 >= 576px時，不寫格數，bootstrap會自動幫你分配格數
    ```

* HTML / CSS基本
    * 在HTML的每一個tag中，class可以同時設定好幾個，可以是你寫的、也可以是引用別人寫的，但要注意**後面的class通常會覆蓋前面class的屬性**（但如果你發現有例外狀況，那就表示本來寫這個class的人有針對不同的class設定優先權）
    * clearfix
        ![](https://i.imgur.com/b6v9IfJ.png)