# Web Develop周邊基礎知識
* Server / Client
    * server side render
        * 前後端無法分開
        * 如果有一天server掛了，user就會直接無法造訪這個網頁 (Ex: 404 Not Found)
        * render的過程是放在server上
        * 前端工程師基本上負責view這個資料夾底下的所有東西
        * 前端工程師Debug的時候要把整個專案run起來，才能知道畫面輸出的結果，所以前端工程師會需要摸到後端的東西
        ![](https://i.imgur.com/HVSpPJ8.jpg)

    * client side render
        * 前後端可以完美切開 (分開工作/分開部署)
        * 前端工程師可以利用ajax從後端拿資料，再用JS動態產生內容就好
        * 如果有一天server掛了，user依舊可以造訪網頁，只是看不到資料而已
        * 前端工程師 / 後端工程師都可以愛用甚麼語言用甚麼語言，只要送出的資料格式固定就可以了
        ![](https://i.imgur.com/c2hQ0by.jpg)



* MVC : 一種開發模式(架構)，把各種功能(概念)分開來各自寫，前端/後端都可以遵循這種模式
    * 把所有本來都一起寫在html裡面的東西分開來
        * **M**odel : 放 "**資料**"
        * **V**iew : 放 "**跟畫面顯示有關的東西**"
        * **C**ontroller : 放 "**連接Model, View的code**"
        ![](https://i.imgur.com/tdBIoeG.jpg)
        Controller去Model裡面拿資料，再把資料塞入View裡面以顯示
        
        ![](https://i.imgur.com/tTDQD7f.png)
        上圖：全部東西混在一起的code（php/html寫在一起）//Ref: [跟著小明一起搞懂技術名詞](https://hulitw.medium.com/introduction-mvc-spa-and-ssr-545c941669e9)
    
        ![](https://i.imgur.com/bRCXbq7.png)
        下圖：php/html檔案分開 //Ref: [跟著小明一起搞懂技術名詞](https://hulitw.medium.com/introduction-mvc-spa-and-ssr-545c941669e9)



* SPA / MPA
    * SPA (Single Page Application)，單頁式應用
        * 在頁面上點擊按鈕以後，頁面會出現相對應變化，但不會有全白畫面出現
        * 例如 : Gmail / 音樂播放網站
        * 不同頁面輸出**相同**結果（.html）
        ![](https://i.imgur.com/MuXqJvE.jpg)

    * MPA（Multiple Page Application）
        * 不同頁面輸出**不同**結果（.html / .php）
        ![](https://i.imgur.com/9a2wc3w.jpg)