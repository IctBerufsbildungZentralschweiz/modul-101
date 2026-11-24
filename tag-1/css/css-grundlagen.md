# 📖 CSS-Grundlagen

Wie HTML ist auch CSS keine Programmiersprache sondern eine Stylesheet-Sprache.

CSS erlaubt es, für Elemente auf einer Website das Aussehen festzulegen. Zum Beispiel benötigt man folgenden CSS-Code, um alle Absätze (`<p>`) auszuwählen und deren Inhalt rot einzufärben:

```css
p {
  color: red;
}
```

## Aufbau einer CSS-Regel

Die ganze Struktur wird Regelsatz (oder oft nur Regel) genannt:

![CSS-Grundgerüst](../../.gitbook/assets/css-bezeichnungen.jpg)

### Bestandteile

**Selektor** - Der HTML-Elementname steht am Anfang der Regel. Er wählt die Elemente, die gestaltet werden sollen (in diesem Beispiel `p`). Selektoren dienen dazu, in CSS bestimmte Elemente eines HTML-Dokuments zu adressieren, um sie zu gestalten:

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

**Deklaration** - Eine einzelne Anweisung wie `color: red;` gibt an, welche Eigenschaft des Elements gestaltet werden soll. Eine Deklaration besteht aus einer Eigenschaft (`color`) und einem Eigenschafts-Wert (`red`).

**Eigenschaft (englisch: property)** - Art wie das ausgewählte HTML-Element gestaltet werden soll. In diesem Fall ist `color` eine Eigenschaft des `<p>` Elements.

**Eigenschafts-Wert (englisch: property value)** - Rechts neben der Eigenschaft, nach dem Doppelpunkt, steht der Wert der Eigenschaft. Dieser gibt eine von vielen Möglichkeiten wieder, wie die Eigenschaft das Aussehen eines Elements verändern kann.

### Syntax

* Hinter dem Selektor stehen die zugehörigen Regeln innerhalb geschwungener Klammern (`{}`).
* Innerhalb einer Deklaration muss man einen Doppelpunkt (`:`) nutzen, um Eigenschaft und Wert zu trennen.
* Am Ende jeder Deklaration muss ein Semikolon (;) gesetzt werden. Dieses trennt mehrere Deklarationen voneinander ab.

```css
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

## Kommentare

Wie in HTML können auch in CSS Kommentare zur besseren Verständlichkeit des Codes hinzugefügt werden:

```css
/* Styles for Buttons */
button {
    border-radius: 5px;
}
```

CSS-Code kann auch auskommentiert werden, wenn er aktuell nicht interpretiert werden soll:

```css
button {
    border-radius: 5px;
    /*font-weight: bold; */
}
```

In diesem Beispiel wird eine Formatierung aktuell nicht berücksichtigt.

**I**m Browser in den DevTools > Styles erkennt der Browser dann zwar die Deklaration, deaktiviert sie jedoch:

<div align="left"><figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div>
