# cached-webpgr-v2
base on idess [cached-webpgr.js](https://github.com/webpgr/cached-webpgr.js)

# Alpha v2
* German<br>
Functions weise.<br>
Erst prüfen ob alle Daten im localstrong sind und Version stimmt. Sollt etwas Fehlen oder version nicht Stimmen.<br>
Wird es geladen<br>
wenn geladen sind "location.reload()" ausgeführt.
Sind alle Daten OK hinzufügen<br>
und function init() wird gestartet wenn document ready || onload ist!<br>

* Support<br>
  * js file<br>
  * css file<br>

your js and css files [add here](https://github.com/WarManiac/cached-webpgr-v2/blob/main/cached-webpgr-v2.js#L10)
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

your code [add here](https://github.com/WarManiac/cached-webpgr-v2/blob/main/cached-webpgr-v2.js#L107)
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
