# Selektoren verschachteln und kombinieren

Abhängig davon, in welchen Übergeordneten Elementen und Containern etwas verschachtelt ist, können wir das Aussehen steuern. Für alle Beispiele nehmen wir folgenden HTML-Code an:&#x20;

```html
<header>
  <nav class="navi">
    <a href="home.html" class="nav-link">Home</a>
    <a href="services.html" class="nav-link active">Services</a> 
    <div class="subnavi">
      <a href="reparaturen.html" class="nav-link">Reparaturen</a>
    </div>
  </nav>
</header>

<main>
  <h1>Services</h1>
  <p>Dies ist unter Super-Service</p>
  <p>Wir bieden <a href="reparaturen.html">Reparaturen</a> an.</p>
</main>

<footer>
  <nav>
    <a href="kontakt.html">Kontakt</a> | 
    <a href="datenschutz.html">Impressum & Datenschutz</a>
  <nav>
</footer>
```

## Mehrere Elemente auswählen

Teilen sich mehrere Elemente die gleichen Regeln, sollten diese zusammengefasst werden. Dazu werden mehrere Selektoren hintereinander geschrieben, getrennt durch Kommas:&#x20;

```css
h1, .subnavi, footer {
  font-style: italic;
}
```

## Nachfahren-Selektor

Nachfahren sind alle Elemente innerhalb eines anderen Elements (Kinder, Kindeskinder etc.). Dieser Selektor adressiert also bestimmte Elemente, welche in HTML in einem anderen Element verschachtel sind. Die Eltern- und Nachfohr-Selektoren werden durch ein Leerzeichen getrennt:&#x20;

```css
header a { /* Formatiert alle Links im Header */
  color: red;
}
```

## Kind-Selektor (direkte Nachfahren)

Beim Kind-Selektor werden zwei Selektoren durch ein `>` voneinander getrennt. Der Selektor spricht das zuletzt erwähnte Element nur dann an, wenn es ein direktes Kind des vorhergehenden Elements ist.

Als Kind werden alle Elemente _direkt unterhalb_ eines anderen Elements bezeichnet.

```css
.navi > a {/* Formatiert nur "Home" und "Services", aber nicht "Reparaturen" */
  color: red;
}
```

## Next-Sibling-Kombinator

Wählt ein Element aus, welches unmittelbar auf ein anderes Element auf der gleichen Ebene folgt.

```
h1 + p { /* Formatiert nur das nav-Element direkt nach h1 */
  font-style: bold;
}
```

## Mehrfach-Selektoren

Um Elemente auszuwählen, welche mehrere Selektoren gleichzeitig erfüllen, kette die Selektoren einfach aneinander **ohne Leerzeichen** dazwischen:

```css
/* Gilt nur für Links mit der Klasse "nav-link" */
a.nav-link {
  text-decoration: none;
}
/* Gilt nur für Elemente mit Klassen "subnav-link" UND "active" in einem Element */
.nav-link.active {
  color: red;
}
```

## 🛠️ Aufgabe

Auf deiner Seite "Über mich":

* Gebe allen Links in der Tabelle eine andere Farbe ([Nachfahren-Selektor](03-selektoren.md#nachfahren-selektor))
* Gebe allen Links im Footer eine andere Farbe
* Schau, wo du aktuell doppelte Style-Definitionen hast und fasse sie zusammen ([Mehrere Elemente auswählen](03-selektoren.md#mehrere-elemente-auswahlen))
* Was bewirkt folgende Definition? \
  `h2 + p { font-weight: bold; }`
