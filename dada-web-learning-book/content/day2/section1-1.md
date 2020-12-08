# Git / Github / SourceTree
> git就是一個版本控管工具，是很好的輔助！（常常也會是救星）

* git GUI工具推薦（這樣就不用開可怕的Terminal了）：[Sourcetree](https://www.sourcetreeapp.com/)
* Download & Install [Git](https://git-scm.com/download/mac)
    ```bash
    brew install git   # 記得先裝好Xcode
    ```
* git是程式碼的版本控管工具，[github](https://github.com/)則是用來存放這些歷代版本的遠端空間，同時供給所有github使用者交流平台
* Private / Public
* github io可以用來放靜態網頁！
* git 語法＆Sourcetree使用介紹
```bash
#初始化
git init  
```
```bash
#把github的空間連結到Local端的資料夾
git remote add origin https://github.com/yihanYozikua/hey-dada.git
```
```bash
#把要commit的檔案加入暫存
git add *
```
```bash
#紀錄當前的code狀態 
#這是記錄在你自己的電腦上喔
git commit -m "這裡打你對這次commit的註解"
```
```bash
#將當前的code狀態放到遠端空間中
#這是記錄在遠端空間上喔
git push
```
```bash
#可以利用git指令把github上面的專案下載下來
git clone github上面的某個專案連結
例如 : git clone https://github.com/yihanYozikua/14-days-sketch.git
```
```bash
#可以透過git clone，把別人放在gitjhub上面的專案下載下來
git clone <別人的專案連結>
git clone https://github.com/yihanYozikua/14-days-sketch.git
```
![](https://i.imgur.com/fE4T7Rm.png)