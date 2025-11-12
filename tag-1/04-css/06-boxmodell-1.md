# Weitere Eigenschaften von Boxen / Containern

## Höhe, Breite

Für jede Box kann die Breite und Höhe definiert werden. Häufige Masseinheiten sind Pixel oder Prozent, manchmal auch `vw`/`vh` , selten `rem/em`.

```css
.container {
    width: 200px; // Breite 
    max-width: 50%; // Maximum 50% der übergeordneten Box breit
    height: 600px; // Höhe
    min-height: 50vh; // Minimal halbe Viewporthöhe (Fensterhöhe)
}
```

**Hinweis:** Standardmässig beziehen sich `width` und `height` nur auf den Inhaltsbereich. Padding und Border kommen zusätzlich dazu. Mit `box-sizing: border-box;` kann das Verhalten geändert werden, sodass `width` und `height` den gesamten Bereich inkl. Padding und Border umfassen.

## Übergroser Inhalt (`overflow`)

Wenn der Inhalt einer Box grässer ist als die angegebene Breite oder Höhe der Box, kannst du bestimmen, was passieren soll:&#x20;

* `overflow: visible`: Inhalt soll über die Box hinausragen
* `overflow: hidden`: Zu grosser Teil soll ausgeblendet werden
* `overflow: scroll`: Scrollbalken anzeigen

Genauere Beschreibungen findest du z.B. auf [https://css-tricks.com/css-is-awesome/](https://css-tricks.com/css-is-awesome/)

## Positionierung

Mit der `position`-Eigenschaft kannst du bestimmen, wie ein Element im Dokumentenfluss platziert wird.

* **`position: static`** (Standard) - Elemente folgen dem normalen Dokumentenfluss.
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

## z-index

Mit `z-index` kannst du die Stapelreihenfolge von positionierten Elementen steuern. Ein höherer Wert bedeutet, dass das Element weiter vorne liegt.

<pre class="language-css"><code class="lang-css">.hintergrund {
  position: absolute;
  z-index: 1;
}
.fixed-header {
<strong>  position: absolute;
</strong>  z-index: 10;
}
</code></pre>

**Wichtig:** `z-index` funktioniert nur bei Elementen mit einer `position`-Eigenschaft (außer `static`).

## Display-Eigenschaft

Die `display`-Eigenschaft bestimmt, wie ein Element im Layout dargestellt wird.

* **`display: none`** - Element wird ausgeblendet und der Platz freigegeben.&#x20;
* **`display: block`** - Element nimmt die gesamte verfügbare Breite ein und beginnt auf einer neuen Zeile.
* **`display: inline`** - Element nimmt nur so viel Platz ein, wie es benötigt, und erlaubt andere Elemente neben sich.
* **`display: inline-block`** - Wie display: inline, kann aber Höhe, Breite etc. haben.
* **`display: flex`** - [Siehe Flexbox](../../tag-2/01-flexbox/)
* **`display: grid`** - [Siehe CSS Grid](../../tag-2/04-css-grids/)

**`display: none`** / **`display: block`** kann somit genutzt werden, um Elemente je nach Belieben ein- oder auszublenden, z.B. bei kleinen Bildschirmen, bei Hover-Effekten oder für die Druck-Version einer Seite.

