# Media Queries

Media Queries ermöglichen es, CSS-Regeln abhängig von gerätespezifischen Attributen (Bildschirmgrösse, Pixeldichte) oder Sensordaten des Geräts (Lichtsensor) zu definieren.

Mit Media Queries ist es möglich Websites zu erstellen, die sich automatisch an die Merkmale von verschiedensten Geräten anpassen.

## Allgemeine Deklaration

```css
@media <filter> {
    /**
     * Diese Regeln sind nur dann aktiv, wenn der
     * <filter> auf das Gerät des Besuchers zutrifft.
     */
}
```

## Medien-Typen 

Um einzelne Medien-Typen zu filtern, kann `all`, `screen`, `print` oder `speech` (spezielle Styles für Screenreader) verwendet werden.

```css
body {
    background: red;
}

/**
 * Beim Ausdrucken der Website soll der Seitenhintergrund
 * nicht rot sein.
 */
@media print {
    body {
        background: none;
    }
}
```

## Medien-Features

Media Queries lassen sich auf diverse `Features` anwenden. Dies kann z. B. die Bildschirmgrösse, Pixeldichte des Displays oder ein Wert des Lichtsensors sein (ist es hell oder dunkel?).

Eine Liste aller verfügbarer Features befindet sich hier: [https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features).

Die Syntax setzt sich zusammen aus `(feature-name: Wert)`.

**Achtung:** Mit der `CSS Media Queries Level 4` Spezifikation wurden viele neue Features eingeführt, die momentan [noch nicht in allen Browsern](https://caniuse.com/#feat=css-media-interaction) unterstützt werden.

```css
body {
    background: white;
    color: black;
}

@media (light-level: dim) {
    /**
     * Bei dunkeln Lichtverhältnissen soll der Website-Hintergrund
     * zu schwarz wechseln.
     */
    body {
        background: black;
        color: white;
    }
}
```


### `min-width` / `max-width`

Die mit Abstand am meisten verwendeten Features sind `min-width` und `max-width`.  Damit kannst du dein Layout dynamisch auf die Bildschirmgrösse von Desktops, Tablets und Smartphones anpassen.

```css
.container {
    width: 1200px;
}

/**
 * Sobald das Browserfenster weniger Breit wird als
 * 1200px, soll der Container nur noch 600px Breit sein.
 */
@media (max-width: 1200px) {
    .container {
        width: 600px;
    }
}
```

**Achtung:** Gerade wenn es um die Bildschirmbreite geht möchte man diese oft nur für *Bildschirme* anwenden, nicht etwa wenn die Website ausgedruckt wird. Aus diesem Grund macht es Sinn im Filter zwei Features mit dem `and` Operator zu verketten.

```css
@media screen and (max-width: 1200px) {
    /** 
     * Diese Styles werden garantiert nur bei der Anzeige
     * auf Bildschirmen angewendet.
     */
}
```
