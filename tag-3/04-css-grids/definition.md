# Definition

## Grids in CSS definieren

Wir möchten folgendes Grid in CSS umsetzen. \
Dazu kann wie folgt vorgegangen werden:

![Container](<../../.gitbook/assets/code-example-1 (1).png>)

## Container definieren

Als aller erstes muss ein Container definiert werden:

```markup
<div class="container">
    <!-- Hier werden die Inhalte eingefügt -->
</div>
```

In CSS muss dessen `display` Property auf `grid` gesetzt werden.

```css
.container {
    display: grid;
}
```

## Spalten und Zeilen definieren

Um die Spalten zu definieren, kann die `grid-template-columns` Property verwendet werden. Für Zeilen kann die `grid-template-rows` Property verwendet werden.&#x20;

In userem Beispiel wird die erste Spalte auf `80px` und die dritte Spalte auf `260px` fixiert. Die zweite Spalte soll immer den restlichen Platz ausfüllen (`auto`).

Die erste Zeile wird auf `100px` fixiert. Die zweite Zeile soll immer den restlichen Platz ausfüllen (`auto`).

```css
.container {
    display: grid;
    grid-template-columns: 80px auto 260px;
    grid-template-rows:   120px auto;
}
```

## Zwischenräume definieren

Zwischen den Grid-Bereichen kannst du einen Abstand definieren:&#x20;

```css
.container {
    display: grid;
    grid-template-columns: 80px auto 260px;
    grid-template-rows:   120px auto;
    
    /* Zwischenräume zwischen Spalten und Zeilen: */
    gap: 20px;
    /* oder nur zwischen Spalten: */
    column-gap: 20px;
    /* oder nur zwischen Zeilen: */
    row-gap: 20px;
}
```

## Inhalte einfügen

Wenn du jetzt sechs Elemente in deinen Container einfügst, werden diese automatisch in deinem Grid platziert.

```markup
<div class="container">
  <div>A</div>
  <div>B</div>
  <div>C</div>
  <div>D</div>
  <div>E</div>
  <div>F</div>
</div>
```

Siehe [https://codepen.io/anon/pen/ZaePGz](https://codepen.io/anon/pen/ZaePGz).

## Grid mit dynamischer Anzahl von Elementen

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
