# CSS-Kaskadierung
An einem Punkt wird es dazu kommen, dass mehrerere CSS-Regeln das gleiche Element ansprechen.

##### index.html
```html
<p class="red">Mein roter Text.</p>
```
##### style.css
```css
p {
    color: black;
}

.red {
    color: red;
}
```
In diesen Fällen stellt sich die Frage: Welche CSS Regel «gewinnt» und wird auf das angesteuerte Element angewendet? Dies wird nicht einfach dem Zufall überlassen, sondern über einen Mechanismus namens «Cascading» oder Kaskadierung bestimmt.

## Kaskadierung
CSS ist ein Akronym für ***Cascading** Style Sheet* - dies zeigt die Bedeutung der Kaskadierung für die Gestaltung mit CSS. Grundsätzlich entscheiden drei Faktoren darüber, welche CSS Regel «gewinnt»:

1. Wichtigkeit
2. Spezifizierung
3. Platzierung/Reihenfolge

Die Faktoren sind nach ihrer Anwendungsreihenfolge gegliedert: Somit ist die Wichtigkeit zuerst angewendet, anschliessend die Spezifizierung und zum Schluss die Platzierung.

### Wichtigkeit

In CSS kann man mit einer speziellen Syntax sicher stellen, dass einige Deklarationen *immer* wichtiger sind als andere: `!important`.

##### index.html
```html
<p class="red">Mein roter Text.</p>
```

##### style.css
```css
p {
    color: black !important;
}

.red {
    color: red;
}
```

Im oben gezeigten Beispiel wird die Schrift schwarz angezeigt, da diese CSS-Regel mit der Syntax `!important` als wichtig deklariert wurde.

**WICHTIG:** Es macht nur Sinn diese Syntax einzusetzen, wenn man absolut keine andere Wahl hat. Diese Syntax ändert nähmlich die Art und Weise komplett, wie die Logik der Kaskadierung normalerweise funktioniert.
Die Notwendigkeit, `!important` zu verwenden, ist meist ein Hinweis auf schlecht strukturierten CSS-Code.

### Spezifizierung
Eine CSS-Regel ist umso stärker, desto spezifischer der Selektor definiert wurde.

* Typen-Selektoren (`p`) haben die niedrigste Spezifizierung und sind deshalb am schwächsten.
* `class`-Selektoren (`.red`) haben eine höhere Spezifizierung und sind deshalb stärker als Typen-Selektoren.
* `id`-Selektoren (`#help`) haben die höchste Spezifität und sind deshalb stärker als Typen- und `class`-Selektoren.


Als kleine Überlegungshilfe gibt es hier das [Punktesystem](src/kaskadierung_spezifikation.pdf).

### Platzierung
Sind sowohl Wichtigkeit und Spezifizierung von zwei Selektoren identisch, entscheidet schlussendlich die Platzierung, welche CSS-Regel tatsächlich angewendet wird.

Regeln die später im Code auftauchen überschreiben Regeln, welche vorher definiert wurden.

```css
p {
  color: blue;
}

/* Diese Regel überschreibt die oben aufgeführte Regel. */
p {
  color: red;
}
```

## Aufgabe
Versuche nun mit Hilfe der Kaskadierung eine CSS-Regel des `paper.css` zu überschreiben. Färbe dazu den Schatten (`box-shadow`) des Papiers blau.