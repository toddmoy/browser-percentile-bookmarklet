Browser Percentile Bookmarklet
==============================

This bookmarklet overlays a transparent png which shows averaged browser height percentiles. 

![screenshot](https://raw.github.com/toddmoy/browser-percentile-bookmarklet/master/browser-overlay-example.png)

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
    overlay.setAttribute('style', 'position:fixed\;left:0\;top:0\;width:100%\;height:6000px\;background-image:url(https://raw.github.com/toddmoy/browser-percentile-bookmarklet/master/browser-overlay.png)\;z-index:9999\;');                  
    document.body.appendChild(overlay); 
  } else {
    overlay.parentNode.removeChild(overlay);
  }
 }());
 ```
