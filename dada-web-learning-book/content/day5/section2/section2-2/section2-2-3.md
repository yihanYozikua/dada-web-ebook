# 語言
``` :lang ```

```html
<p>
  <span lang="zh-hant">我試試看中文</span>
  <span lang="en">and English</span>
  <span lang="zh-hant">夾雜</span>
  <span lang="en">is it ok?</span>
</p>
```

```scss
span:lang(en){
  color: aquamarine;
}

span:lang(zh-hant){
  color: antiquewhite;
}
```