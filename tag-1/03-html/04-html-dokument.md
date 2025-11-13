# 📄 HTML Dokument

## Aufbau eines HTML-Dokumentes

Jedes HTML-Dokument sollte minimal die folgenden Elemente enthalten. Du kannst den Code als Gerüst für all deine neuen Seiten benutzen:&#x20;

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Meine Testseite</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  </head>
  <body>
    Inhalt ...
  </body>
</html>
```

**\<!DOCTYPE html>** — der Dokumenttyp. Diese Zeile teilt dem Webbrowser mit, in welcher Version von HTML das Dokument verfasst wurde. Die einfache `html` Definition steht für `HTML5`. Für ältere Versionen wurden längere und spezifischere Tags verwendet. (siehe [thoughtco.com](https://www.thoughtco.com/list-of-doctypes-and-the-web-pages-they-generate-3467257))

**\<html>\</html>** — das `<html>` Element. Dieses Element umhüllt den ganzen Inhalt. Manchmal wird es auch als root-Element bezeichnet.

**\<head>\</head>** — das `<head>` Element. In dieses Element ist alles eingeschlossen, was nicht auf der Seite angezeigt wird. Dies enthält Informationen wie Schlüsselwörter, eine Seitenbeschreibung, welche in Suchmaschinen erscheint, CSS um unseren Inhalt zu designen, usw.

**\<meta charset="utf-8">** — Dieses Element setzt die Zeichenkodierung deines Dokuments auf `utf-8`, in der die Schriftzeichen von fast allen Sprachen enthalten sind. Umlaute wie Ä und Ü werden ohne dieses Tag evtl. nicht richtig angezeigt.

**\<title>\</title>** — Dies setzt den Titel der Seite, welcher im Tab angezeigt wird. Dieser wird auch gebraucht, wenn jemand ein Lesezeichen erstellt.

**\<meta name="viewport" content="...">** — Dieses Element sorgt dafür, dass Elemente auf verschiedenen Bildschirmgrössen und Zoomlevels korrekt skaliert werden. Siehe [Responsive Design](../../tag-2/05-responsive-design/responsive-design.md#viewport).

**\<body>\</body>** — das `<body>` Element. Dies beinhaltet alles, was die Betrachter sehen, wenn sie die Website besuchen, egal ob Text, Bilder, Videos, Audiodateien, usw.
