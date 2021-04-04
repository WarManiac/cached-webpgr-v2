# cached-webpgr-v2
base on [cached-webpgr.js](https://github.com/webpgr/cached-webpgr.js)

# v2
Don't change
```
var requireScript = new Array()
```
Your js and css files add
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
