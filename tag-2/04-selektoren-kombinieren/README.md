# CSS-Selektoren kombinieren

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

### 🛠️ Ausprobieren

Erstelle eine neue Datei `selektoren-test.html` und ein neues CSS `css/selektoren-test.css` und binde das CSS ins HTML-Dokument ein. Kopiere ein [HTML-Grundgerüst](../../tag-1/03-html/04-html-dokument.md#aufbau-eines-html-dokumentes) in deine neue HTML-Datei und dann innerhalb des Body den obigen HTML-Code.

Testen dann im CSS die folgenden Beispiele aus:

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
main h1 { /* Formatiert die Überschrift 1 im <main>-Container */
  letter-spacing: 2px;
}
```

### Beispiel: Links je nach Kontext anders gestalten&#x20;

```css
/* Links generell gestalten */
a { color: gray; text-decoration: underline; }
/* Links in der Navigation anders darstellen */
nav a { color: black; text-decoration: none; }
/* Links im Footer nochmal anders darstellen */
footer a { color: red; }
```

### Beispiel: Unterschiedliche Seiten-Layouts

Oft hat z.B. die Startseite ein anderes Layout als die restlichen Seiten. Damit wir trotzdem eine gemeinsame CSS-Datei für alles nutzen können, kannst du jeder Seite eine Klasse ins `<body>`-Element geben und darüber das Layout steuern:&#x20;

```html
<!-- index.html (Startseite) -->
<body class="home">
    <header>
        <h1>Home</h1>
    </header>
</body>
```

```html
<!-- contact.html (Konraktseite) -->
<body class="contact">
    <header>
        <h1>Kontakt</h1>
    </header>
</body>
```

```css
/* Basis-Layout für alle Seiten */
header {
    background-color: darkblue;
    height: 200px;
}
/* Für die Startseite einige Styles überschreiben */
.home header {
    height: 400px;
}
```

**Hinweis:** An Tag 3 werden wir Grids für Seiten-Layouts einsetzen. Da wirst du das wieder brauchen können, um je nach Seite unterschiedliche Grid-Layouts zu definieren.&#x20;

## CSS Nesting

{% hint style="info" %}
**Achtung neues Feature:** CSS Nesting wird von den meisten Browsern seit Dezember 2023 unterstützt, von einzelnen mobilen Browsern aber erst kurz (Android-Browser seit Okt./Nov. 2026) oder teils gar nicht. \
⇒ Noch zurückhaltend verwenden.

Siehe [caniuse.com](https://caniuse.com/?search=CSS+Nesting)
{% endhint %}

Verschachtelte Nachfahren-Selektoren können schnell zu unübersichtlichem CSS-Code führen und Änderungen an Selektoren mühsam machen. Abhilfe bietet das "CSS Nesting".&#x20;

CSS Nesting war lange nur mit speziellem CSS-Compiler (LESS/SASS) möglich. Seit kurzem wird das Nesting auch ohne Compiler von den meisten Browsern nativ unterstützt:&#x20;

```css
/* Obiges Beispiel mit CSS Nesting */
.home {
    .container {
        grid-template-rows: 300px 50px 300px auto 150px;
    }
    /* weitere Deklarationen für die Startseite... */
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
  font-weight: bold;
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

## 🛠️ Aufgaben

Auf deiner Seite "Über mich":

* Gebe allen Links in der Tabelle eine andere Farbe ([Nachfahren-Selektor](./#nachfahren-selektor))
* Gebe allen Links im Footer eine andere Farbe
* Schau, wo du aktuell doppelte Style-Definitionen hast und fasse sie zusammen ([Mehrere Elemente auswählen](./#mehrere-elemente-auswahlen))
* Was bewirkt folgende Definition? \
  `h2 + p { font-weight: bold; }`
