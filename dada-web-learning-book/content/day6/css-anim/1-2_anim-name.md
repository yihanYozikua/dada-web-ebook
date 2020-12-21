# Animation-name

* ``` animation-name ``` 就是**動畫名稱**
* 注意事項
  * 名稱大小寫有區別
  ```scss
  @keyframes dada{}
  @keyframes DADA{}
  // 以上這兩個代表的是不一樣的！
  ```
  * 特殊字詞不能使用
  ```scss
  @keyframes None{}
  @keyframes Initial{}
  // 以上兩個都會噴error
  ```
  * 一定要設定