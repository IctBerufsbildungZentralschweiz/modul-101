# Media Queries

Media Queries ermöglichen es, CSS-Regeln abhängig von gerätespezifischen Attributen (Bildschirmgrösse, Pixeldichte), Ausgabegerät (Bildschirm, Drucker) oder Sensordaten des Geräts (Lichtsensor, ist es hell oder dunkel?) zu definieren.

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

Media Queries lassen sich auf diverse `Features` anwenden. \
Eine Liste aller verfügbarer Features befindet sich hier: [developer.mozilla.org/en-US/docs/Web/CSS/@media#Media\_features](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features).

Die Syntax setzt sich zusammen aus `(feature-name: Wert)`.

### Fensterbreite: `min-width` / `max-width`

Die mit Abstand am meisten verwendeten Features sind `min-width` und `max-width`. Damit kannst du dein Layout dynamisch auf die Bildschirmgrösse von Desktops, Tablets und Smartphones anpassen.

```css
.container {
    width: 1200px;
}

/**
 * Sobald das Browserfenster weniger Breit wird als
 * 1200px, soll der Container nur noch 600px Breit sein.
 */
@media (min-width: 1200px) {
    .container {
        width: 600px;
    }
}
```

**Achtung:** Gerade wenn es um die Bildschirmbreite geht möchte man diese oft nur für _Bildschirme_ anwenden, nicht etwa wenn die Website ausgedruckt wird. Aus diesem Grund macht es Sinn im Filter zwei Features mit dem `and` Operator zu verketten.

```css
@media screen and (min-width: 1200px) {
    /** 
     * Diese Styles werden garantiert nur bei der Anzeige
     * auf Bildschirmen angewendet.
     */
}
```

#### Verkettung mehrerer Bedingungen

Wie schon bei `@media screen and (min-width: 1200px)` kann ich auch mehrere Bedingungen verknüpfen, z.B. um nur bestimmte Fensterbreiten anzusprechen:&#x20;

```
@media screen and (min-width: 800px) and (max-width: 1199px) {
    /** 
     * Diese Styles werden garantiert nur bei der Anzeige
     * auf Bildschirmen angewendet.
     */
}
```

### Fensterbreite: Media Query Range Syntax

Seit 2023 können auch Vergleichs-Operatoren genutzt werden, sog. media query range features:&#x20;

```css
/* statt (max-width: 1199px): */
@media (width < 1200px) {
  /* … */
}
@media (width => 1200px) {
  /* … */
}
```

Damit können auch Bereiche einfach abgefragt werden:&#x20;

```css
/* statt screen and (max-width: 800px) and (max-width: 1199px): */
@media screen and (800px <= width < 1200px) {
  /* … */
}
```

### Ausrichtung: Hoch- / Querformat

Wenn ich wissen will, ob ein Bildschirm im Hoch- oder Querformat benutzt wird, kann ich dies abfragen:&#x20;

```
@media screen and (orientation: landscape) { /* Oder portrait für Hochformat */
  /* Styling für querformat */
}
```

Das eher unüblich, öfter wird einfach die Fensterbreite (min-width/max-width) abgefragt.&#x20;

### Helligkeit: `light-level`

Mit der `CSS Media Queries Level 4` Spezifikation wurden viele neue Features eingeführt. \
**Achtung:** Manche davon werden momentan [noch nicht in allen Browsern](https://caniuse.com/?search=CSS%20Media%20Queries%20Level%204) unterstützt.

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
