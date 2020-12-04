# 專案結構看光光

> 一個網頁前端專案內部通常會有哪些東西


* // deploy //：真正要部署的時候，要放上去到網域上的東西都在裡面。yarn build完後產生此folder，可直接將folder內的所有東西上傳至ftp。不需編輯、不需進git 
* // dist //：每次處理過後的結果都在裡面，在一邊做測試的時候這裡會一直更新、刷新（示範給你看）放各個處理過的js, css, html檔案。不需編輯、不需進git
* // js //：放各個js原始碼，最佳化後會被放在/dist/js/
dada-learn-web
* .gitignore：用來列出哪些東西不用push到github，可以列資料夾、或是特定檔案
* gulpfile.js（這個你可以不用動到）：用來寫自動化的步驟，關於編譯sass, js的規則、開啟localhost的設定等
* README(.md)：用來寫關於專案的說明
* yarn.lock
* package.json


![](https://i.imgur.com/Q8J3kKJ.png)