Convert your graphics to support a mobile/tablet WEB (i.e., surfing to a your site using a mobile browser).
You should do it for both your individual game and your component (the Server team should help the login team to convert their UI to mobile).

  * Surf to your appspot website from a mobile device, and make sure everything works as expected.
  * Make sure dragging on mobile works, and if it doesn't then fix it. See [drag-n-drop on mobile](http://stackoverflow.com/questions/20927759/html5-drag-and-drop-for-mobile). GWT doesn't have enter and leave events, so you will need to use [JSNI](http://www.gwtproject.org/doc/latest/DevGuideCodingBasicsJSNI.html) to handle them.

## Scaling your game ##
Your game should scale itself to fit exactly in the available window size.
Add this JS code to your HTML
```
<script>
function scaleBody() {
  var myGameWidth = ENTER_YOUR_GAME_WIDTH;
  var myGameHeight = ENTER_YOUR_GAME_HEIGHT;
  var scaleX = window.innerWidth / myGameWidth;
  var scaleY = window.innerHeight / myGameHeight;
  var scale = Math.min(scaleX, scaleY);
  var transformString = "scale(" + scale + "," + scale + ")";
  document.body.style.transform = transformString;
  document.body.style['-o-transform'] = transformString;
  document.body.style['-webkit-transform'] = transformString;
  document.body.style['-moz-transform'] = transformString;
  document.body.style['-ms-transform'] = transformString;
  var transformOriginString = "0 0 0";
  document.body.style['transform-origin'] = transformOriginString;
  document.body.style['-o-transform-origin'] = transformOriginString;
  document.body.style['-webkit-transform-origin'] = transformOriginString;
  document.body.style['-moz-transform-origin'] = transformOriginString;
  document.body.style['-ms-transform-origin'] = transformOriginString;
}
window.onresize = scaleBody;
window.onorientationchange = scaleBody;
document.addEventListener("orientationchange", scaleBody);
scaleBody();
</script>
```
You should add the above script tag at the end of your `<body>`,
and add in the `<head>` tag use [viewport](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag):
```
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
```

## Testing your mobile changes ##
One option is to install an emulator, e.g.,
[Android emulator](http://buildcontext.com/blog/2011/android-browser-emulator-windows-7-nexus-s-xoom-tablet).

You can also emulate a mobile device on chrome using
[the emulation panel](https://developers.google.com/chrome-developer-tools/docs/mobile-emulation#enable-emulation-panel).




The emulation panel have a [bug with MGWT](https://groups.google.com/d/msg/mgwt/W9ZxRyhBbBc/-NpMgo5lRP4J) (its a [chrome bug](https://code.google.com/p/chromium/issues/detail?id=133915)), so if you're using [GwtEmulator](http://smg-gwt-emulator.appspot.com/GwtEmulator.html) then you should spoof your user agent to an empty string or turn the user agent off.

Test on Nexus5.