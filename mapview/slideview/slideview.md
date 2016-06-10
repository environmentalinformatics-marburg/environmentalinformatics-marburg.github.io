# slideView

![](http://i.creativecommons.org/l/by-nc-sa/3.0/88x31.png) (CC-BY-NC-SA)

This document was produced on _Fr Jun 10 2016_ using **mapview** version **1.1.0**

------

### slideView


```r
library(mapview)
library(raster)

stck1 <- subset(poppendorf, c(3, 4, 5))
stck2 <- subset(poppendorf, c(2, 3, 4))
slideView(stck1, stck2)
```

<!--html_preserve--><div id="htmlwidget-43" style="width:909.12px;height:480px;" class="slideView html-widget"></div>
<script type="application/json" data-for="htmlwidget-43">{"x":{"message":{"a":"a","b":"b"},"img1":"stck1","img2":"stck2"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

------
