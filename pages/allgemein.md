# Allgemein

## Größe der Webseite
+ eine durchschnittliche Webseite hat momentan ca. 3MB: https://speedcurve.com/blog/web-performance-page-bloat/ steelers.de hat 14 MB (beim Start am Freitag waren es noch 30MB).
+ alleine das Bild im Footer ist 2,9 MB groß
+ alle Daten werden über http/1.1 ausgeliefert (http://www.chip.de/artikel/HTTP_2-Der-neue-Web-Standard_139963048.html)
+ kein cache-control, d.h. alle Daten werden immer ausgeliefert (https://developer.mozilla.org/de/docs/Web/HTTP/Headers/Cache-Control)
+ keine Bild-Optimierung. Testweise ein Spielerbild durch https://tinypng.com/ und dabei 74%(!) gespart
+ vector grafiken wurden unnötigerweise in pixelgrafiken umgewandelt. (Logo svg)
+ png zur Nutzung von Fotos (https://www.sitepoint.com/gif-png-jpg-which-one-to-use/)
+ Anzahl Webfonts: 9 (neun!!!) widerspricht allem was Design ausmacht (https://www.lifewire.com/use-fewer-fonts-1074171)

Speedtest Ergebnisse (Stand: 24.09.2018):

Speedtest alte Seite:
[![Speedtest alte Seite](/pages/speedtest-old.png)](https://tools.pingdom.com/#5982eb57ca000000)

Speedtest neue Seite:
[![Speedtest neue Seite](/pages/speedtest-new.png)](https://tools.pingdom.com/#5982ebb78dc00000)

Speedtest esvk.de:
[![Speedtest ESVK](/pages/speedtest-esvk.png)](https://tools.pingdom.com/#5982cc3c4d400000)

## Footer
+ Footer mit Copyright fehlt auf der Startseite, ist auf unterseiten vorhanden
+ Sponsorenlogos sind nur fünf auf anhieb zu sehen. Scrollen hilft nicht um mehr zu sehen, nur "drag and drop". Auch auf dem Desktop. Dadurch werden fünf Sponsorenlogos nie automatisch angezeigt, sondern erst nach User-Interaktion

## CSS
+ 16 verschiedne CSS-Dateien
+ Vier CSS-Dateien von Tempalte und Wordpress. Keines mit Minify, alle einzeln und nicht kombiniert.
+ zwei verschiedene Icon-Fonts
+ 29 verschiedene Hintergrundfarben. Fünf verschiedene Grün-Töne. Zwei verschiedene Blau-Töne.
+ 34 verschiedene Text-Farben. drei verschiedene Grün-Töne. Sechs verschiedene Blau-Töne
![CSS Farben](/pages/css-colors.PNG "CSS Farben")
