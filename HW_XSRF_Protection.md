Add [XSRF protection](http://code.google.com/webtoolkit/doc/latest/DevGuideSecurityRpcXsrf.html) to your game. You will need to add to your GWT:
```
  public void onModuleLoad() {
    Cookies.setCookie("JSESSIONID", "JSESSIONID", null, null, "/", false);
    ...
  }
```