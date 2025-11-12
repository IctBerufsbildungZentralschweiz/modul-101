# 🛠️ Aufgabe "Über mich" gestalten

![](../../.gitbook/assets/ralph.png)

## Aufgabenstellung zu Einbindung und Selektoren

Style deine Website "Über mich" und ¨berprüfe nach jedem Schritt das Ergebnis im Browser.&#x20;

1.  Falls noch nicht gemacht: Erstelle eine neue CSS-Datei `styles.css`  in deinem Projekt-Verzeichnis `/ueber-mich/css`, kopiere als Start schon mal folgenden Inhalt rein und verknüpfe sie in deiner `about-me.html` Datei:&#x20;

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
2. Packe den ganzen Inhalt des `<body>`-Elementes in einen Container `<div class="global-wrapper">` . Schau dir das Ergebins im Browser an.
3.  Style die erstelle `about-me.html`, in dem du in deiner CSS-Datei neue Selektoren mit Formatierungen hinzufügst:&#x20;

    * Das ganze Dokument soll die Schriftart "Arial" und die Zeilenhöhe 1.5 haben
    * Der Header soll eine eigene Hintergrundfarbe deiner Wahl haben
    * Zeichne die Tabellenlinien in einem Hellgrau (`#aaaaaa`), 1px breit
    * Mache die Tabellen-Überschriften linksbündig und den Hintergrund der Zellen hellgrau
    * Links sollen dunkelgrau und unterstrichen sein
    * Bei Mouse-Over über die Links sollen die Schrift schwarz werden
    * Das erste Hobby soll eine fette Schrift haben, die anderen nicht (mit Pseudoselektor lösen)
    * Formatiere selber noch etwas, worauf du Lust hast

    Zustzaufgaben für schnelle Lernende:

    * Färbe mit dem geeigneten Pseudoselektor den Hintergrund jeder 2. Zeile der Tabelle hellgelb.&#x20;
    * Wende einen Filter auf dein Bild an: Normal soll es blass/heller oder sogar schwarz-weiss sein, wenn die Maus drüber fährt, soll es in den richtigen Farben erscheinen.&#x20;
4. Schreibe das CSS so, dass möglichst kein `margin` oder `padding` einem `<p>`, `<img>` oder `<table>`-Tag zugewiesen ist, sondern den ensprechenden semantischen Elementen oder `<div>` Containern.
5. Schau, dass möglichst kein Code doppelt ist, z.B. dass für die 2 Adressen.&#x20;
6. Kopiere den Code anschliessend in den [CSS-Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) und korrigiere allfällige Fehler.
