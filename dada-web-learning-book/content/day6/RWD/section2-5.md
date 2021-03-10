# RWD實作時間
> 所以在我們的專案裡面會怎麼處理這件事呢？

![](https://i.imgur.com/caXXSOK.jpg)
* 先在 **scss** 資料夾裡面，創建一個 **vars.scss** 檔案
* 此後，只要每次開一個新的 .scss 檔案，就要在 .scss檔案最上方引入 **vars.scss** 這個檔案
```scss
@import "./vars.scss";
// 開始寫跟media query有關的東西...
```
* 以下示範 **vars.scss** 怎麼寫

```scss
$sm-width: 576px; // 6寸左右的手機
$md-width: 768px; // 一般iPad直式大小
$lg-width: 992px; // 一般iPad橫式大小、iPad pro直式大小
$xl-width: 1200px; // 一般電腦螢幕大小

@mixin xs() {
    @media all and(max-width: $sm-width) {
      @content;
    }
}
@mixin sm() {
  @media all and(min-width: $sm-width) {
    @content;
  }
}
@mixin md() {
  @media all and(min-width: $md-width) {
    @content;
  }
}
@mixin lg() {
  @media all and(min-width: $lg-width) {
    @content;
  }
}
@mixin xl() {
  @media all and(min-width: $xl-width) {
    @content;
  }
}
```
* 在其他引用 vars.scss的檔案中則是這樣寫...

```scss
#某個id{
  .某個class{
    @include sm(){
      // 在這個格式之下，版面要怎麼定義
    }

    @include md(){
      // 在這個格式之下，版面要怎麼定義
    }
    
    @include lg(){
      // 在這個格式之下，版面要怎麼定義
    }

    @include xl(){
      // 在這個格式之下，版面要怎麼定義
    }
  }
}
```