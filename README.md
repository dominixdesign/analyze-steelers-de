
# Analyse von steelers.de

## Allgemein

+ kein automatisches https (widerspricht der eigenen Datenschutzverordnung)


## Größe der Webseite
+ eine durchschnittliche Webseite hat momentan ca. 3MB: https://speedcurve.com/blog/web-performance-page-bloat/ steelers.de hat 14 MB (beim Start am Freitag waren es noch 30MB).
+ alleine das Bild im Footer ist 2,9 MB groß
+ alle Daten werden über http/1.1 ausgeliefert (http://www.chip.de/artikel/HTTP_2-Der-neue-Web-Standard_139963048.html)
+ kein cache-control, d.h. alle Daten werden immer ausgeliefert (gefixt am 25.9.))
+ keine Bild-Optimierung. Testweise ein Spielerbild durch https://tinypng.com/ und dabei 74%(!) gespart
+ Vector grafiken wurden unnötigerweise in pixelgrafiken umgewandelt. (Logo svg)
+ png zur Nutzung von Fotos (https://www.sitepoint.com/gif-png-jpg-which-one-to-use/)
+ Anzahl Webfonts: 9 (neun!!!) widerspricht allem was Design ausmacht (https://www.lifewire.com/use-fewer-fonts-1074171)

Speedtest Ergebnisse (Stand: 24.09.2018):

Speedtest alte Seite:
[![Speedtest alte Seite](/pages/speedtest-old.png)](https://tools.pingdom.com/#5982eb57ca000000)

Speedtest neue Seite:
[![Speedtest neue Seite](/pages/speedtest-new.png)](https://tools.pingdom.com/#5982ebb78dc00000)

Speedtest esvk.de:
[![Speedtest ESVK](/pages/speedtest-esvk.png)](https://tools.pingdom.com/#5982cc3c4d400000)

## Javascript
+ 30 verschiedene Javascript dateien
+ kein minify, kein kombinieren der Scripts
+ TeamCountdown Javascript wird doppelt geladen
+ owlCarousel wird doppelt geladen

## CSS
+ 16 verschiedne CSS-Dateien
+ Vier CSS-Dateien von Template und Wordpress. Keines mit Minify, alle einzeln und nicht kombiniert.
+ zwei verschiedene Icon-Fonts
+ 29 verschiedene Hintergrundfarben. Fünf verschiedene Grün-Töne. Zwei verschiedene Blau-Töne.
+ 34 verschiedene Text-Farben. drei verschiedene Grün-Töne. Sechs verschiedene Blau-Töne
![CSS Farben](/pages/css-colors.PNG "CSS Farben")

## Footer
+ Footer mit Copyright fehlt auf der Startseite, ist auf Unterseiten vorhanden
+ Sponsorenlogos sind nur fünf auf anhieb zu sehen. Scrollen hilft nicht um mehr zu sehen, nur "drag and drop". Auch auf dem Desktop. Dadurch werden fünf Sponsorenlogos nie automatisch angezeigt, sondern erst nach User-Interaktion (gefixt am 25.9., scrollt nun automatisch durch, dennoch immer die selbe Reihenfolge und man muss für hintere Sponsoren warten)

## Header
+ Header mit Socialmedia, Mail und teelfon ist nur auf manchen Unterseiten. Und sowohl E-Mail-Adresse als auch Telefonnummer linken auf auf die aktuell offene Seite.

## Seiten

### Startseite
+ Nächstes Spiel hat immer zwei Buttons "Match Details" und "zu den Tickets". "Match Details" linkt erst auf Vorbericht, oder auf eine leere Seite, nach dem Spiel auf Spielbericht. "zu den Tickets" geht immer zur Ticketübersicht, nciht zum konkreten Spiel. Auch bei Auswärtsspielen
+ Nächstes Spiel ist dreifach! Erst mit Countdown, dann darunter nochmal in der Box dann mit Sprade.
+ Dresden-Spiel linkt auf URL "speiltag5"
+ Links zu spielen sind inkonsistent. Mal "spieltag1" mal spiel "bayreuth-tigers-steelers". Auf jeden Fall unmöglich es über mehrere Spielzeiten konistent zu nutzen

### News
+ Alle News werden von User "Steelers" geschrieben, obwohl in den Beiträgen der richtige Author genannt wird.
+ Kommentar Funktion vollkommen unklar. Was ist eine "Author URL"? Warum ist die Beschriftung des Formulars in Englisch?
+ Datumsformat ist Englisch, "continue reading" statt "weiterlesen"
+ Kleine Bilder werden fast doppelt so groß dargestellt und verpixeln dadurch

### Social Media
+ Falscher Grünton bei der Facebook-Integration.
+ Unnötiges Plugin für Facebook integration.

### Steelers-Aktionstage und Sponsoren-Aktionstage
+ Unterschiedliche Darstellung für den selben Inhalt
+ Keine Übersicht über alle Aktionstage auf einer Seite
+ Keine Informationen ohne eine PDF runterladen zu müssen

### Saison / Spielplan
+ Absolut unnötige Pagination des Spielplanes. Eine Übersicht über alle Spiele ist nicht möglich.
+ Einfaches herausfinden, z.B. welche Spiele Ende Januar sind ist unmöglich ohne viele Seiten aufzurufen
+ fehlender ics download

### Tabelle
+ Hintergrundbild kachelt und sorft für unlesbarkeit der Tabelle
+ Hintergrundbild ist das selbe wie im footer, aber mit GET-Paramtern versehen, so dass es ein zweites Mal geladen wird
+ Mauszeiger ändert sich zur Hand bei den Teams, obwohl nichts klickbar ist
+ Keine Legende an der Tabelle
+ Viele fehlende Informationen (Siege? Niederlagen?)
+ Teamlogos werden direkt von Holema geladen, kein Caching

### Ligaspielplan
+ Mauszeiger ändert sich zur Hand bei den Spielen, obwohl nichts klickbar ist
+ keine Legende
+ keine Filtermöglichkeit

### Die Steelers / Team / Spieleransicht
+ URL Design wird Probleme verursachen bei Spielern mit selbem Nachnamen
+ keine Spielerstatistik
+ keine Übersicht über Spielerdaten
+ kein Padding an Spielerbeschreibung, dadurch Text sehr eingequetscht
+ Spielerbilder in Detailansicht sind 1000 Pixel hoch, werden aber nichtmal halb so groß angezeigt.
+ Auch Spielerbilder in der Übersicht werden im Browser noch verkleinert
+ Länderflaggen werden direkt von der DEL2 Homepage geladen, kein Caching.
+ Mauszeiger ändert sich zur Hand bei den Spieler-Details, aber nichts ist klickbar

### Teampartner
+ alle Sponsorenlogos werden von der Domain neu.steelers.de geladen

### Spielerstatistik
+ nicht gekennzeichneter externer Link

### Tickets
+ nicht gekennzeichneter externer Link

### Dauerkarten
+ Mauszeiger ändert sich zur Hand bei den Tabellenzeilen, aber nichts ist klickbar
+ Legende nicht mehr lesbar, sobald man nach unten scrollt
+ Blöcke mal in der fetten Überschrift, mal in der normalen Schrift darunter

### Fanshop
+ nicht gekennzeichneter externer Link



### Sponsoren
+ keine einheitliche Aufmachung bei drei Seiten. Mal in Zeilen, mal in Spalten
+ Mauszeiger ändert sich zur Hand bei den Tabellenzeilen, aber nichts ist klickbar
+ alle Sponsorenlogos werden von der Domain neu.steelers.de geladen

### Galerie
+ Passt vom Design nicht zum restlichen Auftritt, standard darstellung von NextGen Gallery
+ Tippfehler in URL "gallerie"
+ Pagination bricht bei zwei Bildern in letzter Zeile bereits um

### Archiv (warum ist das unter "Galerie"?)
+ nicht gekennzeichneter externer Link

### Stammverein
+ nicht gekennzeichneter externer Link

### EgeTrans Arena
+ nicht gekennzeichneter externer Link

