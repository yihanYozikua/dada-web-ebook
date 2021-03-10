# RWD 設計模式（Design Pattern）

#### 主體為流動（Mostly fluid）
* 在大螢幕、或中螢幕上，內容通常維持相同大小，只是會調整邊界
* 在小螢幕上，內容會自動重排，通常是垂直堆疊
* [實際看看效果](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/mostly-fluid.html)
![](https://i.imgur.com/dpDpavy.png)

#### 欄內容下排（Column drop）
* 在大螢幕、中螢幕上，僅調整所有元件的大小
* 螢幕越來越小時，會依序將欄位由右至左往下搬移
* [實際看看效果](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/column-drop.html)
![](https://i.imgur.com/BBVKLte.png)

#### 版面配置位移（Layout shifter）
* 在大螢幕、中螢幕上，僅調整所有元件的大小
* 螢幕小到一定程度時，才會重新排列欄位
* [實際看看效果](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/layout-shifter.html)
![](https://i.imgur.com/689rDvF.png)


#### 微小調整（Tiny tweaks）
* 字面上的意思，就是只調整細部的東西，例如字體大小、影像大小
* 這種設計只適用於單欄的配置（就是一列只有一個column的那種網頁）
* [實際看看效果](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/tiny-tweaks.html)
![](https://i.imgur.com/It8In6g.png)

#### 畫布外空間利用（Off canvas）
* 把比較不常用的內容，放在drawer中，螢幕夠大的時候才會直接顯示
* 例如：把手機版網頁的導覽列做成drawer
* [實際看看效果](https://googlesamples.github.io/web-fundamentals/fundamentals/design-and-ux/responsive/off-canvas.html)
![](https://i.imgur.com/ey7REzE.png)