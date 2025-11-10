# 🛠️ Aufgabe "Über mich" gestalten

![](../../.gitbook/assets/ralph.png)

## Aufgabenstellung

Style deine Website "Über mich" und ¨berprüfe nach jedem Schritt das Ergebnis im Browser.&#x20;

1.  Erstelle eine neue CSS-Datei `styles.css`  in deinem Projekt-Verzeichnis `/ueber-mich/css`, kopiere als Start schon mal folgenden Inhalt rein und verknüpfe sie in deiner `about-me.html` Datei:&#x20;

    ```css
    body {
      border: 1px solid #888888;
      background: #bbbbbb;
      box-shadow: -6px 6px 12px #888888;
    }
    .global-wrapper {
      background: #ffffff;
      margin: 0 auto;
      width: 900px;
      max-width: 100%;
      min-height: 100vh;
    }
    ```
2. Packe den ganzen Inhalt des `<body>`-Elementes in einen Container `<div class="global-wrapper">` . Schau dir das Ergebins im Browser an.
3. Style die erstelle `about-me.html`, in dem du in deiner CSS-Datei neue Selektoren mit Formatierungen hinzufügst:&#x20;
   * Das ganze Dokument soll die Schriftart "Arial" und die Zeilenhöhe 1.5 haben.
   * Der Hauptcontainer (global-wrapper) soll einen Innenabstand von 40px haben.
   * Der Header soll 200px hoch sein und eine andere Schrift- und Hintergrundfarbe haben als der Rest.
   * Die Blöcke im Inhalt (Artikel) sollen jeweils 40px Abstand (margin) unterhalb haben, also zum nächsten Artikel.
   * Die beiden Adresse sollen nebeneinander stehen: \
     Definiere für beide Adress-Blöcke jeweils eine Breite von 50% und setze jeweils `float: left;`&#x20;
   * Zeichne die Tabellenlinien in einem Hellgrau (`#aaaaaa`), 1px breit.&#x20;
   * Mache die Tabellen-Überschriften linksbündig und den Hintergrund der Zellen hellgrau.
   * Links sollen rot sein und ohne Unterstrich.
   * Formatiere selber noch etwas, worauf du Lust hast.
4. Schreibe das CSS so, dass möglichst kein `margin` oder `padding` einem `<p>`, `<img>` oder `<table>`-Tag zugewiesen ist, sondern den ensprechenden semantischen Elementen oder `<div>` Containern.
5. Schau, dass möglichst kein Code doppelt ist, z.B. dass für die 2 Adressen.&#x20;
6. Kopiere den Code anschliessend in den [CSS-Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) und korrigiere allfällige Fehler.
