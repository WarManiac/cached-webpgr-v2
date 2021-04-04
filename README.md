# cached-webpgr-v2
base on idess [cached-webpgr.js](https://github.com/webpgr/cached-webpgr.js)

# Idee
js und css Datein werden selten geändert -> warum immer wieder Downloaden?<br>
Muss man nicht!<br>
bsp:<br>
```
| File                                  | Size       |
| ------------------------------------- | ---------- |
| jquery-1.11.1.min.js                  | ca.  94 KB |
| jquery.mobile-1.4.5.min.js            | ca. 196 KB |
| jquery.mobile.structure-1.4.5.min.css | ca.  86 KB |
| jquery.mobile.icons.min.css           | ca. 125 KB |
| themeroller.min.css                   | ca.  11 KB |
|                                 Summe | ca. 512 KB |
```
js und css Download
Aufruf/Seite laden:
1. ca. 512 KB
2. 0 KB

Brwoser Beenden und Start Aufruf/Seite laden:
1. 0 KB
2. 0 KB

Rechnet man das mal hoch pro Benutzer:
Jeder Benutzer ruft die Seite 1 mal pro Tag auf.<br>
Monat mit 30 Tag<br>
```
30 TAGE *   1 USER *  1 CALL * 512 KB =        15.360 KB =      15,36 MB
30 TAGE * 100 USER * 20 CALL * 512 KB =     3.072.000 KB =    3072,00 MB =    3,072 GB
30 TAGE * 999 USER * 99 CALL * 512 KB = 1.519.119.360 KB = 1519119,36 MB = 1519,119 GB = 1,52 TB
```
mit 999 USER und 99 CALL in 30 TAGEN<br>
1,52 TB für js und cs Datein zu verschwenden, so viel zu Datensparsamkeit!!!<br>
Jeder BENUTZER mit Trafficlimit wird sich über jeden gesparten byte freuen! Oder?<br>
Jeder Serverbetreiber die Trafficlimit haben und für jeder weitern TB zahlen um volle Geschwindigkeit haben.<br>
Siehe z.b. [Hetzner](https://docs.hetzner.com/de/robot/general/traffic/)

interssant für:<br>
* Server Vorteil:
  * weniger Trafic

* Benutzer Vorteil:
  * weniger Trafic
  * bei wieder holten Aufruf schnell geladen da js und css im LocalStrong ist

So lang im Browser(Benutzer) der LocalStrong von der WebSeite nicht gelöscht wird!!!

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
