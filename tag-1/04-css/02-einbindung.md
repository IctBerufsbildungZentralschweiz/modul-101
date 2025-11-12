# CSS Einbindung

## Wo kann CSS definiert werden?

CSS-Regeln können an 3 Orten geschrieben werden:&#x20;

**Extern in CSS-Datei(en)** mittels `<link>`-Element **(empfohlen)**: \
Saubere Trennung von HTML & CSS, CSS kann von mehrere HTML-Dateien genutzt werden.\
`<link href="css/style.css" rel="stylesheet">` \


**Intern** im HTML-Dokument mittels `<style>`-Abschnitt im `<head>` (nicht empfohlen): \
Styles, welche nur auf dieser Seite verfügbar sind.\
`<style>`\
`.navi { color: green; }`\
`</style>`\
\
\


**Inline** als `style` Attribut im HTML-Tag (nicht empfohlen): \
`<p style="font-weight: bold;">` \


**Wichtig:** Inline-Styling sollte vermieden werden! Zweck von CSS ist es, Inhalt (HTML) und Styling (CSS) auseinander zu halten und Styles möglichst über die ganze Website einheitlich zu halten.&#x20;

## CSS-Datei einbinden

### **🛠️ Praxis**

Probieren wir es gleich aus: Kopiere diese drei Zeilen CSS in eine neue Datei im Texteditor und speichere die Datei unter dem Namen `style.css` im gleichen Verzeichnis wie deine HTML-Datei `ueber-mich.html`.

Nun haben wir zwar diese beiden Dateien, diese wissen jedoch noch nichts voneinder. Dies können wir ändern, in dem wir das CSS mit dem HTML-Dokument verknüpfen.

Öffne die Datei `ueber-mich.html` und füge die folgende Zeile irgenwo in den `<head>`-Bereich ein:

```markup
<link href="style.css" rel="stylesheet">
```

**`<link>`** - Mit dem `<link>` kann das HTML-Dokument mit anderen Dokumenten verlinkt werden - es entsteht eine Beziehung (Link) zum angegebenen Dokument.

**`rel`** - Das `rel`-Attribut bestimmt den Typ der Beziehung. Dieses Attribut bestimmt die Art einer Beziehung (rel = relation = Bezug). Hierfür ist eine Reihe von [Attributwerten](https://www.w3.org/TR/html5/links.html#linkTypes) fest definiert.

**`href`** - Das `href`-Attribut zeigt das Ziel der Beziehung. Das `href`-Attribut (href = hyper reference = Hyper(text) -Referenz) gibt somit an, welches andere Dokument in Bezug zum aktuellen steht. Als Wert wird ein gültiger URI erwartet.

Die angegebene URI kann dabei relativ oder absolute definiert werden - dazu ein kleiner [Exkurs](https://github.com/johannesE/modul-101/tree/7ef76a9c9f706911092af198dd248f9a2832f329/Tag%201/04%20CSS/01%20Grundlagen/src/relativ-absolut.pdf).

Betrachte anschliessend die Datei `ueber-mich.html` im Browser - die Absätze sollten nun rot eingefärbt sein.

Verschiebe nun das CSS in ein neues Unterverzeichnis `/css` und passe die Adresse im HTML-Head an.

Um das CSS zu testen, setze für das ganze Dokument (`<body>`) eine Schrift ([`font-family`](https://www.w3schools.com/cssref/pr_font_font-family.php)) und einen Hintergrund ([`background-color`](https://www.w3schools.com/cssref/pr_background-color.php))

### Relative Pfade

Relative Pfaden haben das aktuelle Dokument als Ausgangspunkt für den angegebenen Pfad.

Beispiel für relativer Pfad:

```markup
<link href="../../css/frontpage/style.css" rel="stylesheet">
```

`../` - Zwei Punkte und ein Frontslash vermitteln dem Interpretator des Pfades, dass dieser den aktuellen Ordner verlassen und in die nächst höhere Ebene gehen soll.

```
root/
    html/
       pages/
         |-> index.html
    css/
       frontpage/
         |-> style.css
```

Beziehungen von internen Dateien werden meistens mit einem relativen Pfad angegeben. So können die Dateien problemlos verschoben werden (beispielsweise von der Entwicklungsumgebung auf den Produktivserver).

### Absolute Pfade

Absolute Pfade haben immer das Stammverzeichnis eines Servers (Root) als Ausgangspunkt für den angegebenen Pfad.

Beispiel für absoluter Pfad für die gleiche Ordnersturktur wie oben:

```markup
<link href="/root/css/frontpage/style.css" rel="stylesheet">
<link href="https://www.example.com/root/css/frontpage/style.css" rel="stylesheet">
```

Werden Beziehungen zu externen Dateien (Frameworks, Schriften etc.) hergestellt, wird der Pfad meistens mit einem absoluten Pfad angegeben. Dabei sollte der Anbieter sicherstellen, dass sich der Pfad nicht ändert.&#x20;
