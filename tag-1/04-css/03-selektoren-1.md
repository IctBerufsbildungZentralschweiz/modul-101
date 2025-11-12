# Selektoren kombinieren und verschachteln

Für alle Beispiele nehmen wir folgenden HTML-Code an:&#x20;

```html
<h1>Eine neue Seite</h1>

<nav class="navi">
  <a href="seite-1.html" class="nav-link">Link 1</a>
</nav>

<nav class="sub-navi">
  <a href="seite-2.html" class="subnav-link">Link 2</p>  
  <div>
    <a href="seite-3.html" class="subnav-link active">Link 3</a>
  </div>
</nav>

<footer><a href="kontakt.html">Kontakt></footer>
```

## Mehrere Elemente auswählen

Teilen sich mehrere Elemente die gleichen Regeln, sollten diese zusammengefasst werden. Dazu werden mehrere Selektoren hintereinander geschrieben, getrennt durch Kommas:&#x20;

```css
h1, .sub-navi, footer {
  color: red;
}
```

## Nachfahren-Selektor

Nachfahren sind alle Elemente innerhalb eines anderen Elements (Kinder, Kindeskinder etc.). Dieser Selektor adressiert also bestimmte Elemente, welche in HTML in einem anderen Element verschachtel sind. Die Eltern- und Nachfohr-Selektoren werden durch ein Leerzeichen getrennt:&#x20;

```css
.sub-navi a { /* Formatiert Link 2 & Link 3 */
  color: red;
}
```

## Kind-Selektor (direkte Nachfahren)

Beim Kind-Selektor werden zwei Selektoren durch ein `>` voneinander getrennt. Der Selektor spricht das zuletzt erwähnte Element nur dann an, wenn es ein direktes Kind des vorhergehenden Elements ist.

Als Kind werden alle Elemente _direkt unterhalb_ eines anderen Elements bezeichnet.

```css
.sub-navi > a {/* Formatiert nur Link 2 */
  color: red;
}
```

## Next-Sibling-Kombinator

Wählt ein Element aus, welches unmittelbar auf ein anderes Element auf der gleichen Ebene folgt.

```
h1 + nav { /* Formatiert nur das nav-Element direkt nach h1 */
  color: red;
}
```

## Mehrfach-Selektoren

Um Elemente gleichzeitig über mehrere Attribute auszuwählen, kette diese einfach aneinander:

```css
/* Gilt nur für Elemente mit Klassen "subnav-link" UND "active" in einem Element */
.subnav-link.active {
  color: red;
}
/* Gilt nur für <nav>-Elemente mit Klasse "sub-navi" */
nav.sub-navi {
  border: 1px solid blue;
}
```

## 🛠️ Aufgabe

* Gebe allen Links im Footer eine andere Farbe.
