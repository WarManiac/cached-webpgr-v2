# cached-webpgr-v2
base on [cached-webpgr.js](https://github.com/webpgr/cached-webpgr.js)

# v2

your js and css files [add](https://github.com/WarManiac/cached-webpgr-v2/blob/c3a4472deb5a717a24573101f3e33891febf7a5f/cached-webpgr-v2.js#L3)
```
requireScript.push({
  name: 'Name',
  version: 'Version',
  type: 'Type',
  url: 'Url'
})
```
Name => String dont use space in " " (good = "jQuery-Themes", bad = "jQuery Themes")<br>
Version => String dont use space " "<br>
Type => String "js" || "css"<br>
Url = String "http://to/paht/file" || "https://to/paht/file" || "/to/paht/file"<br>

your code [add]
```
function init() {
  function your_function(){
    // youre code
  }
  //jQuery
  $().resize(function(){
    // youre code
  })
}
```
# License
cached-webpgr-v2.js is released under the [MIT License](https://github.com/WarManiac/cached-webpgr-v2/blob/main/LICENSE).
