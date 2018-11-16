# Responsive Design
Responsive Design bezeichnet die Fähigkeit eines Layouts sich automatisch auf verschiedene Geräteattribute anzupassen. Insbesondere ist damit die Grösse eines Displays gemeint.

## Beispiel

Rufe die Website [https://www.smashingmagazine.com/](https://www.smashingmagazine.com/) auf und verändere die Fenstergrösse.

## Grundsätze

Grundsätzlich wird oft zwischen drei Bildschirmgrössen unterschieden: `Desktop`, `Tablet` und `Mobile`. Diese Grössen bieten dir eine gute Basis zum Designen deiner Website, jedoch solltest du dein Layout nicht auf gewisse Bildschirmgrössen fixieren:

Vor einigen Jahren konnte man seine Website für ein iPhone (320x480), ein iPad (768x1024) und Desktops (1920x1080) auslegen. Heute gibt es jedoch so viele unterschiedliche Bildschirmgrössen, dass eine Ausrichtung auf diese Bildschirmauflösungen weniger Sinn macht.

Stattdessen solltest du dein Layout immer bei diesen Grössen verändern, wo dein Inhalt nicht mehr genügend Platz hat um korrekt dargestellt zu werden.

## Viewport
Der Viewport eines Browser ist der für den Benutzer sichtbaren Bereich einer Website.

Der Viewport ist somit abhängig von der Fenstergrösse des Browsers und dem Anzeigegerät. Der Viewport auf einem mobilen Endgerät (Smartphone, Tablets etc.) ist somit tendenziell kleiner als auf einem Computer Bildschirm.

Bevor es Tablets und Smartphones gab, waren Websites einzig für die Anzeige auf Computer Bildschirmen designed. Es war nicht nötig, dass sich die Dimensionen einer Website dynamisch anpassen, darum hatten diese meistens eine fixierte Breite und Höhe (Table-Designs).

Dann, als das Internet auch für Smartphones und Tablets zugänglich wurde, waren die Websites mit fixierter Breite zu breit um in die neuen Viewports zu passen. Um dies zu korrigieren wurden die Browser mit der Funktion erweitert, dass Websites automatisch auf die passende Grösser herunterskaliert wurden.

Dies war definitiv keine perfekte Lösung - aber eine schnelle.

[Hier ein Beispiel dazu: Gehe dazu in den Device-Emulator.](https://www.w3schools.com/css/example_withoutviewport.htm)

### Kontrolle über den Viewport
HTML5 hat eine Methode eingeführt, wie wir als Webdesigner die Kontrolle über den Viewport zurückerhalten - mit einem `<meta>`-Tag.

Folgendes `<meta>`-Tag sollte somit in (fast) jeder Website eingebunden werden:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
`<meta>` - Das `<meta>`-Tag mit dem Namen `viewport` gibt dem Browser eine Anweisung, welche Dimensionen berücksichtigt werden sollen (`width`) und wie sich die Website zu skalierten (`initial-scale`) hat.

`width=device-width` - Mit diesem Attribut teilt man dem Browser mit, dass die Breite des Viewports (`width`) der Breite des Anzeigegerätes (`device-width`) entspricht.

`initial-scale=1.0` - Mit diesem Attribut teilt man dem Browser mit, dass der Viewport - nicht wie im Beispiel oben - herausgezoomt, sondern standardmässig 1 zu 1 angezeigt werden soll.

[Hier ein Beispiel mit Viewport-Meta-Tag: Gehe dazu in den Device-Emulator.](https://www.w3schools.com/css/example_withviewport.htm)
