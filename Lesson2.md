Browsers and incompatibilities, javascript, DHTML, communication: cookies, GET&POST, REST, JSON.

# Lesson plan #
  * 5 min: [HTTP](https://docs.google.com/present/edit?id=0AfLEQb_5Yz6RZGdwYzM0aDZfOWcyN3R6a2N4)
  * 20 min: Demo: [telnet](http://upload.wikimedia.org/wikipedia/commons/c/c6/Http_request_telnet_ubuntu.png), Network panel (chrome's console or Firebug), javascript panel.
  * 15 min: [REST](https://docs.google.com/presentation/d/1IWkWScq7YSnupzUDN0N_2leTGlr34Q5xH_7kfHQw93A/edit)
  * [mockito](https://code.google.com/p/mockito/) (with examples)
  * [MVP pattern](http://dl.google.com/io/2009/pres/Th_0200_GoogleWebToolkitArchitecture-BestPracticesForArchitectingYourGWTApp.pdf) (pages 53-58).



```
telnet google.com 80
GET index.html

HTTP/1.0 302 Found
Location: http://www.google.com/
Cache-Control: private
Content-Type: text/html; charset=UTF-8
X-Content-Type-Options: nosniff
Date: Mon, 02 Jan 2012 15:39:29 GMT
Server: sffe
Content-Length: 219
X-XSS-Protection: 1; mode=block

<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>302 Moved</TITLE></HEAD><BODY>
<H1>302 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>


telnet www.google.com 80
GET / HTTP/1.1

...

GET / HTTP/1.1
```


# Summary #
You should know the following:
  * [HTTP](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
  * [HTML](http://en.wikipedia.org/wiki/Html)
  * [REST](http://en.wikipedia.org/wiki/REST): GET, POST, PUT, DELETE
  * [Javascript](http://en.wikipedia.org/wiki/JavaScript) and [DHTML](http://en.wikipedia.org/wiki/DHTML)
  * [AJAX](http://en.wikipedia.org/wiki/Ajax_(programming)) and [JSON](http://en.wikipedia.org/wiki/JSON)
  * [Minified](http://en.wikipedia.org/wiki/Minification_(programming)) and [Obfuscated](http://en.wikipedia.org/wiki/Obfuscated_code) code; [GWT obfuscate code](http://code.google.com/webtoolkit/doc/1.6/FAQ_DebuggingAndCompiling.html#Why_is_my_GWT-generated_JavaScript_gibberish?)
  * [Browsers incompatibilities (HTML, CSS, javascript, DOM)](http://en.wikipedia.org/wiki/Cross-browser)