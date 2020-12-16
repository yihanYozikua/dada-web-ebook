# 否定
``` :not ```
* 指定除了某種元素不用被套用CSS樣式之外，其他人都要被套用

```html
<section class="">
  <div>
    <div class="sec excp">1</div>
    <div class="sec">2</div>
    <div class="sec excp">3</div>
    <div class="sec excp">4</div>
    <div class="sec">5</div>
    <div class="sec">6</div>
    <div class="sec">7</div>
    <div class="sec">8</div>
  </div>
</section>
```

```scss
.sec:not(.excp){
  background-color: rgb(133, 114, 114);
  color: aliceblue;
}
```

* 也可以一次指定多個
```html
<section class="">
  <div>
    <div class="sec ex1">1</div>
    <div class="sec">2</div>
    <div class="sec ex1">3</div>
    <div class="sec ex1">4</div>
    <div class="sec ex2">5</div>
    <div class="sec">6</div>
    <div class="sec ex3">7</div>
    <div class="sec">8</div>
  </div>
</section>
```

```scss
.sec:not(.ex1):not(.ex2):not(.ex3){
  background-color: rgb(133, 114, 114);
  color: aliceblue;
}
```