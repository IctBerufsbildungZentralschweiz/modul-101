# CSS Boxmodell

Wie dir vielleicht bereits aufgefallen ist, geht es bei Webseiten oft darum, Boxen zu erstellen (HTML) und Boxen zu gestalten (CSS). Die meisten HTML-Elemente sind somit Boxen oder Schachteln, welche übereinander und nebeneinander gestapelt werden.

Mit CSS können Grösse, Farben, Position usw. bestimmt werden.

<div align="center"><img src="../../.gitbook/assets/boxmodell-gif.gif" alt="boxmodell-gif"></div>

## Eigenschaften von Boxen

Das CSS-Layout basiert auf dem Box-Modell. Jede Box, die Platz auf einer Webseite einnimmt, hat unter anderen folgende Eigenschaften:

* **Aussenabstand (`margin`):** \
  Der Abstand vom Border bis zum nächsten benachbarten Element.
* **Rahmen (`border`):** \
  Der Border ist der Rahmen um ein Element.
* **Innenabstand (`padding`):** \
  Das Padding ist der Raum zwischen Inhalt und Rahmen eines Elements.

![Boxmodell](../../.gitbook/assets/boxmodell.png)

### Aufgabe

1. Rufe eine beliebige Website im Internet auf, öffne die "Developer Tools" (Rechtsklick auf ein Element > "Untersuchen" oder `F12`) und suche das Tab "Computed".&#x20;
2. Schau dir die Grafik des Box-Models eines HTML-Elements unter "Computed" an und darunter, woher die Abstände in CSS kommen.&#x20;
3. Wechsle zwischen den Tabs "Styles" und "Computed", das ist anders?&#x20;
4. Untersuche noch ein paar andere Elemente auf der gleichen Seite.

### Beispiele: 4 Seiten einer Box - top, right, bottom, left

Die Abstände und Rahmen einer Box können für alle 4 Seiten einzeln oder zusammen oder einzeln definiert werden. Ein paar Beispiele:&#x20;

```css
.element-x {
    margin: 20px; /* Aussenabstand 20px, auf allen Seiten gleich */
    border: 1px solid blue; /* Rahmen: 1px breit, durchgezogen, blau */
    border-bottom: 2px double; /* Rahmen unten überschreiben (breiter) */
    padding-top: 10px; /* Innenabstände... */
    padding-right: 20px;
    padding-bottom: 15px;
    padding-left: 20px;
}
.element-y {
    margin: 0 40px; /* Aussenabstand oben & unten 0px, rechts & links 40px */
    border: 2px dashed #CC0000; /* Rahmen: 2px, gestrichelt, rot */
    border-radius: 10px; /* Runde Ecken */
    padding: 10px 20px 15px 20px; /* Innenabstand wie oben, zusammengefasst: oben rechts unten links */
}
.image {
    border-radius: 50%; /* Schneidet ein Bild kreisrund aus */
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

**Hinweis:** Standardmässig beziehen sich `width` und `height` nur auf den Inhaltsbereich. Padding und Border kommen zusätzlich dazu. Mit `box-sizing: border-box;` kann das Verhalten geändert werden, sodass `width` und `height` den gesamten Bereich inkl. Padding und Border umfassen.

### Übergroser Inhalt (`overflow`)

Wenn der Inhalt einer Box grässer ist als die angegebene Breite oder Höhe der Box, kannst du bestimmen, was passieren soll:&#x20;

* `visible`: Inhalt soll über die Box hinausragen
* `hidden`: Zu grosser Teil soll ausgeblendet werden
* `scroll`: Scrollbalken anzeigen

Genauere Beschreibungen findest du z.B. auf [https://css-tricks.com/css-is-awesome/](https://css-tricks.com/css-is-awesome/)

### Positionierung

Mit der `position`-Eigenschaft kannst du bestimmen, wie ein Element im Dokumentenfluss platziert wird.

* **`position: static`** (Standard) - Elemente folgen dem normalen Dokumentenfluss. Dies ist die Standardeinstellung.
*   **`position: relative`** - Das Element wird relativ zu seiner normalen Position verschoben, ohne den Platz im Dokumentenfluss freizugeben.

    ```
    .box {
      position: relative;
      top: 20px;
      left: 10px;
    }
    ```
*   **`position: absolute`** - Das Element wird aus dem normalen Dokumentenfluss entfernt und relativ zum nächsten positionierten Elternelement platziert. z.B. ein Mobile-Menu:\
    .mobile-menu {

    ```
    .mobile-menu {
      position: absolute;
      top: 80px;
      right: 0;
    }
    ```
*   **`position: fixed`** - Das Element wird relativ zum Browserfenster positioniert und bleibt beim Scrollen an der gleichen Stelle. Z.B. "Sticky Header":

    ```
    header {
      position: fixed;
      top: 0;
      width: 100%;
    }
    ```

### z-index

Mit `z-index` kannst du die Stapelreihenfolge von positionierten Elementen steuern. Ein höherer Wert bedeutet, dass das Element weiter vorne liegt.

```css
.hintergrund {
  position: absolute;
  z-index: 1;
}
header {
  position: absolute;
  z-index: 10;
}
```

**Wichtig:** `z-index` funktioniert nur bei Elementen mit einer `position`-Eigenschaft (außer `static`).

### Display-Eigenschaft

Die `display`-Eigenschaft bestimmt, wie ein Element im Layout dargestellt wird.

* **`display: none`** - Element wird ausgeblendet und der Platz freigegeben.&#x20;
* **`display: block`** - Element nimmt die gesamte verfügbare Breite ein und beginnt auf einer neuen Zeile.
* **`display: inline`** - Element nimmt nur so viel Platz ein, wie es benötigt, und erlaubt andere Elemente neben sich.
* **`display: inline-block`** - Wie display: inline, kann aber Höhe, Breite etc. haben.
* **`display: flex`** - [Siehe Flexbox](../../tag-2/01-flexbox/)
* **`display: grid`** - [Siehe CSS Grid](../../tag-2/04-css-grids/)

**`display: none`** / **`display: block`** kann somit genutzt werden, um Elemente je nach Belieben ein- oder auszublenden, z.B. bei kleinen Bildschirmen, bei Hover-Effekten oder für die Druck-Version einer Seite.

