# CSS Media Query

* *Media Queries* 指的是網頁會先詢問（query）媒體（media）的屬性，再針對這些屬性定義版面的長相
  * 簡單來說，先知道網頁是以哪種裝置開啟
  * 例如：如果是在印刷裝置被開啟，則render出一個印刷裝置版的頁面
* *Media Types* 就是裝置類型
  * 主要有4種
  * *all* ：所有裝置（**最常用的就是這個**）
  * *print* ：印刷裝置
  * *screen* ：螢幕裝置
  * *speech* ：朗讀裝置，也就是能夠「讀出」頁面的設備
* *Media Features* 裝置的特徵
  * 有四個大類別，每個類別底下還有細項
  * Viewport / Page Dimensions（視窗或頁面尺寸）
    * ``` width ``` ：螢幕寬度，例如： ``` max-width ``` , ``` min-width ```
    * ``` height ``` ：螢幕高度，例如： ``` max-height ``` , ``` min-height ```
    * ``` aspect-radio ``` ：螢幕長寬比，例如： ``` max-aspect-ratio ``` , ``` min-aspect-ratio ```
    * ``` orientation ``` ：螢幕旋轉方向，例如： ``` portrait ``` （直向） , ``` landscape ``` （橫向）
  * Display Quality（顯示品質）
    * ``` resolution ``` ：解析度，也就是dpi, ppx...等，例如： ``` max-resolution ``` , ``` min-resolution ```
    * ``` scan ``` ：電視掃描方式
  * Color（顏色）
  * Interaction（互動）


