# cached-webpgr-v2
base on [cached-webpgr.js](https://github.com/webpgr/cached-webpgr.js)

# v2
```
var requireScript = new Array()
```
```
requireScript.push({
  name: 'Name',
  version: 'Version',
  type: 'Type',
  url: 'Url'
})
```
Name => String dont use space in " " (good = "jQuery-Themes", bad = "jQuery Themes") 
Version => String dont use space " "
Type => String "js" || "css"
Url = String "http://to/paht/file" || "https://to/paht/file" || "/to/paht/file"

# License
cached-webpgr-v2.js is released under the [MIT License](https://github.com/WarManiac/cached-webpgr-v2/blob/main/LICENSE).
