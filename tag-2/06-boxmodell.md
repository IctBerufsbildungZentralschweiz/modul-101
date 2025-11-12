# Header / Footer: Positionierung

Praktisch jede Webseite hat einen Header- und einen Footer-Bereich. Um sie nice zu gestalten, brauchen wir ein paar Positionierungs-Features:&#x20;

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

## 🛠️ Aufgaben

Stelle sicher, dass deine Seite "Über mich" mindestens die drei Strukturelemente `<header>`, `<main>` und `<footer>` enthält. Sie sollen direkt unter dem \<body>-Element sein, nicht tiefer verschachtelt.&#x20;

**Gestalte nun den Header:**&#x20;

* Positioniere ein Logo darin absolut, 30px von oben und 30px von links.
* Positioniere einen Slogan im Header absolut, 40px von oben und 30px von rechts.

**Gestalte den Footer:**&#x20;

* Fixiere den Footer so, dass er immer am unteren Rand ist, 80px hoch und über dem Inhalt der Website (`z-index`).
* Stelle sicher, dass die Inhalte ganz am Ende der Seite nicht vom Footer überdeckt werden. Wie? Du kannst z.B. dem Bereich `<main>` unterhalb einen Abstand (`margin`) von 80px geben.



## Optional: Display-Eigenschaft

Die `display`-Eigenschaft bestimmt, wie ein Element im Layout dargestellt wird.

* **`display: none`** - Element wird ausgeblendet und der Platz freigegeben.&#x20;
* **`display: block`** - Element nimmt die gesamte verfügbare Breite ein und beginnt auf einer neuen Zeile.
* **`display: inline`** - Element nimmt nur so viel Platz ein, wie es benötigt, und erlaubt andere Elemente neben sich.
* **`display: inline-block`** - Wie display: inline, kann aber Höhe, Breite etc. haben.
* **`display: flex`** - [Siehe Flexbox](01-flexbox/)
* **`display: grid`** - [Siehe CSS Grid](../tag-3/04-css-grids/)

**`display: none`** / **`display: block`** kann somit genutzt werden, um Elemente je nach Belieben ein- oder auszublenden, z.B. bei kleinen Bildschirmen, bei Hover-Effekten oder für die Druck-Version einer Seite.
