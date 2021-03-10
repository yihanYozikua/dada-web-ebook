# 提問時間

### flex


#### flex-grow
* 當空間有剩餘時，這個屬性用來決定元素要怎麼分配剩餘空間
* 例如：雙側欄排版
```html
<div class="container">
  <div class="sidebar">sidebar</div>
  <div class="content">content</div>
  <div class="content">content</div>
  <div class="sidebar">sidebar</div>
</div>
```

```scss
.container {
  display: flex;
  height: 100vh;
}

.sidebar, .content {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  padding: 0 10px;
}

.sidebar {
  background: gray;
}

.content {
  flex-grow: 1; // "1" => 扣除其他元素（沒有設定這個class的元素）以後，剩下的空間平均分配給有設定這個class的元素
  background: lightblue;
}
```


#### flex-shrink
* 當空間不夠時，這個屬性用來決定元素的壓縮比例
* 計算方式：（每個 item 的 ``` flex-shrink ``` / 全部 item 的 ``` flex-shrink ``` 總和） x （item 寬/高）
```html
<div class="container">
  <div class="sidebar">sidebar</div>
  <div class="content">content</div>
</div>
```

```scss
.container {
  display: flex;
  height: 100vh;
}

.sidebar, .content {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  padding: 0 10px;
}

.sidebar {
  background: gray;
  flex-basis: 200px;
}

.content {
  flex-basis: 300px;
  flex-grow: 1;
  flex-shrink: 1;
  background: lightblue;
}
```


#### flex-basis
* Q: ``` flex-basis ``` 和 ``` width/height ```哪裡不一樣？
* A:
  * 當 ``` flex-direction: row; ``` 時， ``` flex-basis ``` 會決定 ``` width ```
  * 當 ``` flex-direction: column ``` 時， ``` flex-basis ``` 會決定 ``` height ```
* 例如：
```html
<div class="container">
  <div class="item red">20px</div>
  <div class="item blue">50px</div>
  <div class="item green">100px</div>
</div>
```

```scss
.container {
  display: flex;
  flex-direction: column;
}

.item {
  height: 50px;
  margin: 10px;
  padding: 10px;
  text-align: center;

  &.red {
    background: rgba(255, 0, 0, 0.7);
    flex-basis: 20px;
  }

  &.blue {
    background: rgba(0, 255, 0, 0.7);
    flex-basis: 50px;
  }

  &.green {
    background: rgba(0, 0, 255, 0.7);
    flex-basis: 100px;
  }
}
```


#### 參考連結
[flex空間分配](https://ithelp.ithome.com.tw/articles/10208741)
