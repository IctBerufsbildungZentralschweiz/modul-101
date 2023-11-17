# 🛠 Aufgabe Formulare

![](../../.gitbook/assets/ralph.png)

## Aufgabenstellung

Erstelle ein Anmeldeformular für den nächsten Firmenanlass deines Lehrbetriebes. Die folgenden Daten müssen für die Anmeldung eingetragen werden können:

* Name
* Email
* Strasse
* PLZ und Ort
* Telefonnummer
* Verfügbarkeit eines der folgenden Abos: `Kein Abo`, `GA`, `Halbtax`, `Streckenabo Luzern-Zürich`
* Abendessen `Menü 1` oder `Menü 2`
* Mit oder ohne Übernachtung
* Einzel- oder Doppelzimmer
* Bemerkung

Achte darauf die richtigen Formularfeld-Typen zu verwenden. Zudem sollten die Formularfelder korrekt gruppiert werden.

## Versand

Um dein Formular zu testen, kannst du die Daten an folgenden Endpunkt senden:

```
https://formlog.offline.ch/log
```

Die vom Endpunkt empfangenen Daten werden [hier](https://formlog.offline.ch/) angezeigt:

```
https://formlog.offline.ch/
```

### Variante: POST

```markup
<form action="https://formlog.offline.ch/log" method="POST">
  [...]    
</form>
```

### Variante: GET

```markup
<form action="https://formlog.offline.ch/log" method="GET">
  [...]    
</form>
```

### Vorgehen

1. Erstelle für die Aufgabe einen neuen Ordner und darin ein neues HTML-Dokument `formular.html` für das Formular.
2. Füge das [HTML-Grundgerüst](../../tag-1/03-html/04-html-dokument.md) von Tag 1 ein, ändere den `<title>` und lösche das Bild aus dem `<body>` raus.
3. Kopiere das [Formular-Tag von oben](aufgabe.md#variante-post) in den \<body>
4. Füge nun [alle benötigten Felder](aufgabe.md#aufgabenstellung) in das Formular ein und teste immer wieder, ob es korrekt abgeschickt wird.
5. Denke dran, dass alle Felder eine `name=""`-Attribut haben und ein sinnvolles `<label>` oder einen `placeholder`!
