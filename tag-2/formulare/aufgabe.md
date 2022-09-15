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
