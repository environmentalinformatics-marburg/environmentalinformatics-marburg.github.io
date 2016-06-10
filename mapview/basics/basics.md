# mapview basics

![](http://i.creativecommons.org/l/by-nc-sa/3.0/88x31.png) (CC-BY-NC-SA)

This document was produced on _Fr Jun 10 2016_ using **mapview** version **1.1.0**

------


```r
library(mapview)
mapview()
```

<!--html_preserve--><div id="htmlwidget-7171" style="width:909.12px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-7171">{"x":{"calls":[{"method":"addProviderTiles","args":["CartoDB.Positron",1,"CartoDB.Positron",{"errorTileUrl":"","noWrap":false,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false}]},{"method":"addProviderTiles","args":["OpenStreetMap",2,"OpenStreetMap",{"errorTileUrl":"","noWrap":false,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false}]},{"method":"addProviderTiles","args":["Esri.WorldImagery",3,"Esri.WorldImagery",{"errorTileUrl":"","noWrap":false,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false}]},{"method":"addProviderTiles","args":["Thunderforest.Landscape",4,"Thunderforest.Landscape",{"errorTileUrl":"","noWrap":false,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false}]},{"method":"addProviderTiles","args":["OpenTopoMap",5,"OpenTopoMap",{"errorTileUrl":"","noWrap":false,"zIndex":null,"unloadInvisibleTiles":null,"updateWhenIdle":null,"detectRetina":false,"reuseTiles":false}]},{"method":"addLayersControl","args":[["CartoDB.Positron","OpenStreetMap","Esri.WorldImagery","Thunderforest.Landscape","OpenTopoMap"],[],{"collapsed":true,"autoZIndex":true,"position":"topleft"}]},{"method":"addScaleBar","args":[{"maxWidth":100,"metric":true,"imperial":true,"updateWhenIdle":true,"position":"bottomleft"}]}],"setView":[[50.814772,8.770862],18,[]]},"evals":[],"jsHooks":{"render":["\nfunction(el, x, data) {\n  // we need a new div element because we have to handle\n  // the mouseover output seperately\n  debugger;\n  function addElement () {\n    // generate new div Element\n    var newDiv = $(document.createElement('div'));\n    // append at end of leaflet htmlwidget container\n    $(el).append(newDiv);\n    //provide ID and style\n    newDiv.addClass('lnlt');\n    newDiv.css({\n      'position': 'relative',\n      'bottomleft':  '0px',\n      'background-color': 'rgba(255, 255, 255, 0.7)',\n      'box-shadow': '0 0 2px #bbb',\n      'background-clip': 'padding-box',\n      'margin': '0',\n      'color': '#333',\n      'font': '9px/1.5 \"Helvetica Neue\", Arial, Helvetica, sans-serif',\n    });\n    return newDiv;\n  }\n\n  // check for already existing lnlt class to not duplicate\n  var lnlt = $(el).find('.lnlt');\n  if(!lnlt.length) {\n    lnlt = addElement();\n    // get the leaflet map\n    var map = HTMLWidgets.find('#' + el.id);\n\n    // grab the special div we generated in the beginning\n    // and put the mousmove output there\n    map.on('mousemove', function (e) {\n      lnlt.text(' Latitude: ' + (e.latlng.lat).toFixed(5) +\n      ' | Longitude: ' + (e.latlng.lng).toFixed(5) +\n      ' | Zoom: ' + map.getZoom() + ' '\n      );\n    })\n  };\n}\n"]}}</script><!--/html_preserve-->

