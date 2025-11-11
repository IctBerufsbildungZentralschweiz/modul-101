# CSS Boxmodell

Wie dir vielleicht bereits aufgefallen ist, geht es bei Webseiten oft darum, Boxen zu erstellen (HTML) und Boxen zu gestalten (CSS). Die meisten HTML-Elemente sind somit Boxen oder Schachteln, welche übereinander und nebeneinander gestapelt werden.

Mit CSS können Grösse, Farben, Position usw. bestimmt werden.

![boxmodell-gif](../../.gitbook/assets/boxmodell-gif.gif)

## Eigenschaften von Boxen

Das CSS-Layout basiert auf dem Box-Modell. Jede Box, die Platz auf einer Webseite einnimmt, hat unter anderen folgende Eigenschaften:

### Aussenabstand (`margin`)

Der Abstand vom Border bis zum nächsten benachbarten Element.

### Rahmen (`border`)

Der Border ist der Rahmen um ein Element.

### Innenabstand (`padding`)

Das Padding ist der Raum zwischen Inhalt und Rahmen eines Elements.

![Boxmodell](../../.gitbook/assets/boxmodell.png)

### Beispiele: 4 Seiten einer Box - top, right, bottom, left

Die Abstände und Rahmen einer Box können für alle 4 Seiten einzeln oder zusammen oder einzeln definiert werden. Ein paar Beispiele:&#x20;

```css
.element-x {
    // Aussenabstand 20px, auf allen Seiten gleich
    margin: 20px;
    // Rahmen: 1px breit, durchgezogen blau, auf allen Seiten
    border: 1px solid blue;
    border-bottom: 2px double; // Unten breiter
    // Innenabstände
    padding-top: 10px;
    padding-right: 20px;
    padding-bottom: 15px;
    padding-left: 20px;
}
.element-y {
    // Aussenabstand oben & unten 0px, rechts & links 40px
    margin: 0 40px;
    // Rahmen: 2px breit, gestrichelt, rot, abgerundete Ecken
    border: 2px dashed #CC0000;
    border-radius: 10px;
    // Innenabstand wie oben, aber zusammengefasst: oben rechts unten links
    padding: 10px 20px 15px 20px;
}
```

### Aufgabe

Probier die Möglichkeiten aus: [w3schools.com/css/tryit.asp?filename=trycss\_boxmodel](https://www.w3schools.com/css/tryit.asp?filename=trycss_boxmodel)

## Weitere Eigenschaften von Boxen

### Höhe, Breite

Für jede Box kann die Breite und Höhe definiert werden. Häufige Masseinheiten sind Pixel oder Prozent, manchmal auch `vw`/`vh` , selten rem/em.

```css
.container {
    width: 200px; // Breite 
    max-width: 50%; // Maximum 50% der übergeordneten Box breit
    height: 600px; // Höhe
    min-height: 50vh; // Minimal halbe Viewporthöhe (Fensterhöhe)
}
```

### Übergroser Inhalt (`overflow`)

Wenn der Inhalt einer Box grässer ist als die angegebene Breite oder Höhe der Box, kannst du bestimmen, was passieren soll:&#x20;

* `visible`: Inhalt soll über die Box hinausragen
* `hidden`: Zu grosser Teil soll ausgeblendet werden
* `scroll`: Scrollbalken anzeigen

Genauere Beschreibungen findest du z.B. auf [https://css-tricks.com/css-is-awesome/](https://css-tricks.com/css-is-awesome/)

