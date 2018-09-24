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

## Footer
+ Footer mit Copyright fehlt auf der Startseite, ist auf unterseiten vorhanden
+ Sponsorenlogos sind nur fünf auf anhieb zu sehen. Scrollen hilft nicht um mehr zu sehen, nur "drag and drop". Auch auf dem Desktop. Dadurch werden fünf Sponsorenlogos nie automatisch angezeigt, sondern erst nach User-Interaktion

## CSS-Farben
+ 29 verschiedene Hintergrundfarben. Fünf verschiedene Grün-Töne. Zwei verschiedene Blau-Töne.
+ 34 verschiedene Text-Farben. drei verschiedene Grün-Töne. Sechs verschiedene Blau-Töne
