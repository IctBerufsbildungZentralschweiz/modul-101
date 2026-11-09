# Ergänzung: Dynamische Grids

## Grids mit dynamischer Anzahl von Elementen

Ein Grid kann auch eine dynamische Anzahl von Elementen enthalten. Dann werden nur die Spalten (columns) definiert, die Zeilen (rows) nicht. Z.B. ein dreispaltiges Grid mit variablen Zeilen:&#x20;

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}
```

Für die dynamischen Anzahl Zeilen können optional Eigenschaften gesetzt werden:&#x20;

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: 100px;
}
```

Mehr zu dynamischen Grids: \
[https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Grid\_layout/Auto-placement](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Grid_layout/Auto-placement)
