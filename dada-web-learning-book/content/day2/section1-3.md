# 前端關鍵字
> html / css / JS / jQuery / CSS Preprocessor / PostCSS / Browserify / Gulp / ES6 / Webpack

* **Web** = html + css + JS + 第三方工具
* **jQuery**：跨瀏覽器支援
* **CSS Preprocessor**：把CSS的Property參數化 / 跨瀏覽器支援
    * 非CSS語法 => 經過預處理後 => 變成.css
    * 把CSS的Property參數化

    ![](https://i.imgur.com/4kiGM2h.png)
    
    * @mixin：是一個用來把css設定包成一整包的工具
        ```
        // 在css檔案裡面
        @mixin 名稱(){
            這個@mixin要尬麻
        }
            .
            .
            .
        .some-css-class{
            @include 名稱;
        }
        ```
        * 例如：有些瀏覽器會要加上特定的prefix才能正常顯示，所以可以用 @mixin包起來，之後只要 @include即可（類似function）（取代掉那個位置）
            * [webkit官方文件](https://developer.mozilla.org/en-US/docs/Web/CSS/WebKit_Extensions)
                * -webkit：chrome / safari
                * -moz：firefox
                * -ms：IE (Edge)
        ![](https://i.imgur.com/KjT2exd.png)


* **PostCSS**：自動加上 prefix
    * PostCSS之中有很多plugins => 其中的Autoprefixer
    ![](https://i.imgur.com/FuwbB4m.jpg)


* 引入Library（以下簡稱lib）的機制
    * 問題：假設今天引入了兩個lib（A.js / B.js）各自都定義了叫做“VERSION”的參數 => 則有可能造成變數衝突，兩個lib互相干擾
    * 解法：**Browserify** [(LINK)](http://browserify.org/)
    
        ![](https://i.imgur.com/65lmXFc.png)
        * 過去的引入方式：直接在html中，下<script></script>的標籤
        
        ![](https://i.imgur.com/gX1Se9E.png)
        * 有了Browserify之後的引入方式：可直接在js中把lib個別require，且設成變數方便使用
        * 而且解決了相依性問題
        ![](https://i.imgur.com/Hws0pAq.jpg)


* **Gulp**
    * 統整一下目前為止的開發過程：都是透過一些工具，將我們寫的檔案變成browser可讀模式
        ![](https://i.imgur.com/xHQcUxx.jpg)

    * 上述的步驟，可以用gulp來管理workflow
    * 定義task / 執行task
    * 所以從此以後，只要拿到專案檔，看gulp file就可以知道這個專案要怎麼跑/怎麼打包
* **ES6**（新一代JS，ECMAScript）
    * 目前只要知道ES6是比較新一代的JS就可以了，細節以後慢慢說
    * 幾年前因為瀏覽器還沒有完全支援，所以需要透過一個轉譯器 **Babel** 把JS轉成瀏覽器可讀模式
        ![](https://i.imgur.com/fFWcLn0.jpg)

* **Webpack**（module bundler）
    * 自從這個東西出來，就越來越少人用Browserify了
    * 可以當成是Gulp裡面的一個task
    * 仔細定義資料傳入跟傳出的類型
    * 可以設定uglify