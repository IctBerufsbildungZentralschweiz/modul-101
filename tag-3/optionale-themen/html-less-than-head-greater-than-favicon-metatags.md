# HTML \<head>, Favicon, Metatags

Wozu ist eigentlich der `<head>`-Bereich im HTML-Dokument da?&#x20;

Er liefert dem Browser viele Hintergrund-Informationen, die über die visuelle Darstellung der Webseite hinausgehen. Die Liste der Möglichkeiten ist lang, wir schauen hier auf die wichtigsten.&#x20;

## Minimum: Titel, Charset, Skalierung, CSS

Bisher hatten wir den Titel, den Zeichensatz, die Skalierung und Import von CSS gesehen:&#x20;

```html
  <head>
    <meta charset="utf-8">
    <title>Meine neue Seite</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="css/style.css" rel="stylesheet">
  </head>
```

## Weitere empfohlene Tags

### Favicon und App-Icons

Ein "Favicon" ist das kleine Icon, welches im Browser-Tab und bei Suchresultaten auf Google & Co. als Icon genutzt wird. Es wird auch verwendet, wenn du einen Link auf dem Startbildschirm eines mobilen Gerätes erstellst.&#x20;

<div align="left"><figure><img src="../../.gitbook/assets/grafik (2).png" alt=""><figcaption></figcaption></figure></div>

Favicon kann man sich leicht erzeugen lassen mit einem Generatoren, z.B.:&#x20;

* [realfavicongenerator.net](https://realfavicongenerator.net/)
* [www.ionos.de/tools/favicon-generator](https://www.ionos.de/tools/favicon-generator)

Danach bindest du sie im HTML-Head ein:&#x20;

```html
<link rel="icon" href="/favicon.ico" sizes="any">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/apple-touch-icon.png">
```

### JavaScript einbinden

```html
<script src="/js/main.js" defer></script>
```

### Für Suchmaschinen: Description und Canonical

**Meta-Tag Description:** Liefert den Text, den die Suchmaschinen bei der Trefferbeschreibung anzeigen kann (aber nicht muss). Sollte 140-160 Zeichen lang sein und wichtige Keywords enthalten, welche auch auf im Seiteninhalt vorkommen.&#x20;

```html
<meta name="description" 
      content="Informationen zu wichtigen Tags im HTML-Head für professionelle Websites.">
```

**Canonical URL:** Sagt dem Browser bei mehrfach vorkommenden Inhalten, welches die bevorzugte Variante ist. Ist nur nötig, wenn unter mehreren URLs teilweise der gleiche Text erscheint:&#x20;

```html
<link rel="canonical" href="https://example.com/seite/">
```

### Open Graph (OG-Tags) für Sharing auf Social Media

Was Social Networks wie Insta, Facebook, etc. beim Sharen als Vorschau anzeigen sollen, kann man über OG-Tags gezielt steuern. Mindestens `og:title`, `og:description` und `og:image` sind zu empfehlen:&#x20;

```html
<meta property="og:type" content="website">
<meta property="og:locale" content="de_DE">
<meta property="og:site_name" content="M101 - Webauftritt erstellen und veröffentlichen">
<meta property="og:title" content="HTML-Head, Favicons und Metatags">
<meta property="og:description" content="Informationen zu wichtigen Tags im HTML-Head für professionelle Websites.">
<meta property="og:image" content="https://example.com/images/social.jpg">
<meta property="og:url" content="https://example.com/">
```

## 🛠️ Aufgaben

1. Definiere ein paar OG-Tags und prüfe dann in einem Social-Media-Kanal, was angezeigt wird.
2. Definiere ein Favicon und prüfe, ob es im Browser-Tab angezeigt wird.
