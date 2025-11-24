# 🔗 CSS-Datei einbinden

## Wo kann CSS definiert werden?

CSS-Regeln können an 3 Orten geschrieben werden:&#x20;

**Extern in CSS-Datei(en)** mittels `<link>`-Element **(empfohlen)**: \
Saubere Trennung von HTML & CSS, CSS kann von mehrere HTML-Dateien genutzt werden.\
`<link href="css/style.css" rel="stylesheet">` <br>

**Intern** im HTML-Dokument mittels `<style>`-Abschnitt im `<head>` (nicht empfohlen): \
Styles, welche nur auf dieser Seite verfügbar sind.\
`<style>`\
`.navi { color: green; }`\
`</style>`\
\
<br>

**Inline** als `style` Attribut im HTML-Tag (nicht empfohlen): \
`<p style="font-weight: bold;">` <br>

**Wichtig:** Inline-Styling sollte vermieden werden! Zweck von CSS ist es, Inhalt (HTML) und Styling (CSS) auseinander zu halten und Styles möglichst über die ganze Website einheitlich zu halten.&#x20;

## CSS-Datei einbinden

### **🛠️ Praxis**

Erstelle eine neue CSS-Datei `styles.css`  in deinem Projekt-Verzeichnis `/ueber-mich/css`, kopiere als Start schon mal folgenden Inhalt rein und verknüpfe sie in deiner `about-me.html` Datei:&#x20;

```css
body {
  background-color: #fbf8e2;
  font-family: Arial, sans-serif;
  margin: 0;
}
header, main, footer {
  padding: 20px;
}
```

Nun haben wir zwar diese beiden Dateien, diese wissen jedoch noch nichts voneinder. Dies können wir ändern, in dem wir das CSS mit dem HTML-Dokument verknüpfen.

Öffne die Datei `ueber-mich.html` und füge die folgende Zeile irgenwo in den `<head>`-Bereich ein:

```markup
<link href="css/style.css" rel="stylesheet">
```

**`<link>`** - Mit dem `<link>` kann das HTML-Dokument mit anderen Dokumenten verlinkt werden - es entsteht eine Beziehung (Link) zum angegebenen Dokument.

**`rel`** - Das `rel`-Attribut bestimmt den Typ der Beziehung. Dieses Attribut bestimmt die Art einer Beziehung (rel = relation = Bezug). Hierfür ist eine Reihe von [Attributwerten](https://www.w3.org/TR/html5/links.html#linkTypes) fest definiert.

**`href`** - Das `href`-Attribut zeigt das Ziel der Beziehung. Das `href`-Attribut (href = hyper reference = Hyper(text) -Referenz) gibt somit an, welches andere Dokument in Bezug zum aktuellen steht. Als Wert wird ein gültiger URI erwartet.

Um das CSS zu testen, setze für das ganze Dokument (`<body>`) eine Schrift ([`font-family`](https://www.w3schools.com/cssref/pr_font_font-family.php)) und einen Hintergrund ([`background-color`](https://www.w3schools.com/cssref/pr_background-color.php))

Betrachte anschliessend die Datei `ueber-mich.html` im Browser - Hintergrund und Schrift sollten nun angepasst sein.

Verschiebe nun das CSS in ein neues Unterverzeichnis `/css` und passe die Adresse im HTML-Head an.\
Die angegebene URI kann dabei relativ oder absolute definiert werden - dazu ein kleiner Exkurs.
