# 🛠️ Aufgabe "Über mich" gestalten

![](../../.gitbook/assets/ralph.png)

## Aufgabenstellung zu Einbindung und Selektoren

Falls noch nicht gemacht: \
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

Style deine Website "Über mich" und ¨berprüfe nach jedem Schritt das Ergebnis im Browser:&#x20;

1. Das ganze Dokument soll die Schriftart "Arial" und die Zeilenhöhe 1.5 haben
2. Der Header soll eine eigene Hintergrundfarbe deiner Wahl haben
3. Definiere in der Seite "Über mich" für alle `<h1>` eine Farbe und eine Schriftart
4. Füge den beiden Adressblöcken uin HTML eine Klasse `class="address"` hinzu und definiere dafür in CSS, dass diese links etwas eingerückt sind ([`margin-left`](https://www.w3schools.com/css/css_margin.asphttps://www.w3schools.com/css/css_margin.asp)) und kursiv ([`font-style`](https://www.w3schools.com/css/css_font_style.asp)) sein sollen
5. Style die Tabelle:&#x20;
   1. Zeichne die Tabellenlinien in einem Hellgrau (`#aaaaaa`), 1px breit
   2. Mache die Tabellen-Überschriften linksbündig und den Hintergrund der Zellen hellgrau
   3. Definiere für alle Tabellen-Header `<th>`, dass sie Linksbündig ([`text-align`](https://www.w3schools.com/css/css_text_align.asp)) sein sollen und eine helle Hintergrundfarbe ([`background-color`](https://www.w3schools.com/css/css_background.asp)) haben.
   4. Entferne die Zwischenräume der Tabellenzellen mit `border-collapse: collapse;`
   5. Definiere für alle Tabellen-Zellen `<th>` und `<td>` einen Innenabstand ([`padding`](https://www.w3schools.com/css/css_padding.asp)) von 8px.
6. Links sollen dunkelgrau und unterstrichen sein. Bei Mouse-Over über die Links sollen die Schrift schwarz werden.
7. Formatiere selber noch etwas, worauf du Lust hast

Zustzaufgaben für schnelle Lernende:

* Das erste Hobby soll eine fette Schrift haben, die anderen nicht (mit Pseudoselektor lösen)
* Färbe mit dem geeigneten Pseudoselektor den Hintergrund jeder 2. Zeile der Tabelle hellgelb.&#x20;
* Wende einen Filter auf dein Bild an: Normal soll es blass/heller oder sogar schwarz-weiss sein, wenn die Maus drüber fährt, soll es in den richtigen Farben erscheinen.&#x20;

1. Schau, dass möglichst kein Code doppelt ist, z.B. für die 2 Adressen.&#x20;
2. Kopiere den Code in den [CSS-Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) und korrigiere allfällige Fehler.
