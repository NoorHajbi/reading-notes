# Read: 13 - Local Storage
## Article: The Past, Present & Future Of Local Storage For Web Applications
- "Persistent local storage is one of the areas where native client applications have held an advantage over web applications."

### Cookies downsides:
- Cookies are included with every HTTP request, thereby ->
1. Slowing down your web application by needlessly transmitting the same data over and over.
2. Sending data unencrypted over the internet (unless your entire web application is served over SSL).
3. Cookies are limited to about 4 KB of data — enough to slow down your application, but not enough to be terribly useful.
---
-  **HTML5 Storage** -> is a way for web pages to store  **key/value** pairs locally(), within the client web browser, *Like cookies*.
- You store data based on a named **key**, then you can retrieve that data with the same key. The named key is a string(the data can be any type but stored as a string.).
- the latest version of pretty much every browser supports HTML5 Storage.
- To detece if the browser supports HTML5 Storage you can use in your JS code -> **Modernizr** which is an open source, MIT-licensed JavaScript library that detects support for many HTML5 & CSS3 features.
*Like that*
```
if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```
---

- You can use square brackets instead of **setter and getter**
```
var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
```

```
var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;
```
are same ..

---
- "If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something."
- The storage event is supported everywhere the localStorage object is supported.


[Article Url](http://diveinto.html5doctor.com/storage.html)