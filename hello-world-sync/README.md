# Hello World storage.sync

Use chrome.storage.sync to share small chunks of data among all of your Chrome devices. To test, open this app in two different devices, both signed in with the same user.

Important: needs "key" in manifest.json to support testing outside of CWS, so that sync storage is shared among different instances.


```javascript
// app.js
chrome.storage.sync.set({"myValue": newValue}, mycallback);
...
chrome.storage.onChanged.addListener(
  function(changes, namespace) {
    // do something
  }
);
...
chrome.storage.sync.get("myValue", 
  function(val) {
    // do something
  }
);
```

## APIs

* [Storage sync](http://developer.chrome.com/extensions/storage.html)
