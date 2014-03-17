Browser Percentile Bookmarklet
==============================

This bookmarklet overlays a transparent png which shows averaged browser height percentiles. 

![screenshot](http://f.cl.ly/items/1K0X0T360Z3V2d1X3517/browser-overlay-example.png)

## To install

In Chrome:

1. Add a new bookmark
1. In the URL field, paste in the following code

```
javascript: (function(){ 
  var overlay = document.getElementById("browser-overlay");
  if (overlay == null){
    overlay = document.createElement('div'); 
    overlay.setAttribute('id', 'browser-overlay');
    overlay.setAttribute('style', 'position:fixed\;left:0\;top:0\;width:100%\;height:6000px\;background-image:url(http://f.cl.ly/items/472i2t3p1G3u3B2o0H2e/browser-overlay.png)\;z-index:9999\;');                  
    document.body.appendChild(overlay); 
  } else {
    overlay.parentNode.removeChild(overlay);
  }
 }());
 ```
