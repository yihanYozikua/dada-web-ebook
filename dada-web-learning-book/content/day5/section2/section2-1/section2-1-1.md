# ::before / ::after

* 以 ``` display: inline-block; ``` 的屬性存在
* ``` ::before ```：在原本的html元素**之前**加入內容
* ``` ::after ```：在原本的html元素**之後**加入內容

```html
<div>
  原本的HTML元素
</div>
```

```scss
div::before{
  content: '這裡是Before';
  color: rosybrown;
}
div::after{
  content: '這裡是After';
  color: lightblue;
}
```

```html
<div class="test">
  原本的HTML元素
</div>
```

```scss
.test::before{
  content: '這裡是Before';
  color: rosybrown;
}
.test::after{
  content: '這裡是After';
  color: lightblue;
}
```