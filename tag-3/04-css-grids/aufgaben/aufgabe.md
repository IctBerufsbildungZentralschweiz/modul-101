# 🛠️ Aufgabe Grid

Du weisst jetzt, wie man ein Layout mit CSS Grids definiert. Nutze dein Wissen um folgendes Layout in CSS nachzubauen.

## Aufgabenstellung

![](../../../.gitbook/assets/ralph.png)

Setze das unten dargestellte Layout mit einem CSS Grid um.&#x20;

![Aufgabe](<../../../.gitbook/assets/aufgabe (1).png>)

Erstelle dazu ein neues Verzeichnis `grid-aufgabe` mit den Dateien `layout.html` und `styles.css`.&#x20;

In `layout.html`  kannst du als Grundgerüst folgenden Code benutzen:&#x20;

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Meine Testseite</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  </head>
  <body>
    <header>Header<header>
    <nav class="main-nav">Menü</nav>
    <nav class="sub-nav">Untermenü</nav>
    <main>Inhalt</main>
    <aside>Sidebar</aside>
    <footer>Footer</footer>
  </body>
</html>
```

In die Datei `styles.css` kannst du als Starthilfe schon mal dies einfügen:

```css
body {
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
}
.container {
    background-color: lightgrey;
    margin: 0 auto;
    max-width: 1100px;
    min-height: 100vh;

    /* Grid */
    display: grid;
    grid-template-columns: /* ... */;
    grid-template-rows:    /* ... */;
}
```

1. Im HTML-`head` solltest du noch das [CSS verlinken](../../../tag-1/04-css/02-einbindung.md#css-datei-einbinden).&#x20;
2. Damit die Bereiche besser sichtbar sind, gib den Menüs, der Sidebar und dem Footer eine neue Hintergrundfarbe, z.B. `darkgray`.
3. Erstelle nun das Grid gemäss obiger Grafik.
4. Füge zwischen allen Spalten einen Abstand von `20px` ein. Zeilen sollen keinen Abstand haben.

**Danach kannst du noch folgende Fragen beantworten:**&#x20;

* Was bewirkt `body { margin: 0; }`?
* Was bedeutet `.container { margin: 0 auto; }` und was bewirkt es?
* Was bedeutet `min-height: 100vh` und was bewirkt es?
