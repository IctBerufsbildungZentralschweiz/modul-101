# 🛠 Grid Aufgabe

Du weisst jetzt, wie man ein Layout mit CSS Grids definiert. Nutze dein Wissen um folgendes Layout in CSS nachzubauen.

## Aufgabenstellung

![](../../.gitbook/assets/ralph.png)

Setze das unten dargestellte Layout mit einem CSS Grid um.&#x20;

![Aufgabe](../../.gitbook/assets/aufgabe.png)

Erstelle dazu ein neues Verzeichnis mit den Dateien `layout.html` und `styles.css`.&#x20;

Als Starthilfe wird dir folgendes CSS vorgegeben:

```css
body {
    margin: 0;
}
.container {
    display: grid;
    background: lightgrey;
    margin: 0 auto;
    width: 100%;
    max-width: 1100px;
    min-height: 100vh;

    grid-template-columns: /* ... */;
    grid-template-rows:    /* ... */;
}
.header {
    grid-area: /* ... */;
    background-color: lightgray;
}
```

Danach kannst du noch folgende Fragen beantworten:&#x20;

* Was bewirkt `body { margin: 0; }`?
* Was bedeutet `margin: 0 auto` und was bewirkt es?
* Was bedeutet `min-height: 100vh` und was bewirkt es?
* Füge zwischen allen Zeilen und Spalten einen Abstand von `80px` ein.
* Füge eine horizontale Navigation an der entsprechenden Stelle ins Layout ein.
