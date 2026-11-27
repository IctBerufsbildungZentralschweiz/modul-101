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
/* Beim Ausdrucken soll der Hintergrund nicht rot sein 
   und die Navigation ausgeblendet werden. */
@media print {
    body {
        background: none;
    }
    nav {
        display: none;
    }
}
```

## Medien-Features

Media Queries lassen sich auf diverse `Features` anwenden.\
Eine Liste aller verfügbaren Features befindet sich hier: [developer.mozilla.org/en-US/docs/Web/CSS/@media#Media\_features](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#Media_features).

Die Syntax setzt sich zusammen aus `(feature-name: Wert)`.

### Fensterbreite: `min-width` / `max-width`

Die mit Abstand am meisten verwendeten Features sind `min-width` und `max-width`. Damit kannst du dein Layout dynamisch auf die Bildschirmgrösse von Desktops, Tablets und Smartphones anpassen.

```css
.container {
    width: 1200px;
}

/**
 * Sobald das Browserfenster weniger breit wird als
 * 1200px, soll der Container nur noch 600px breit sein.
 */
@media (max-width: 1199px) {
    .container {
        width: 600px;
    }
}
```

**Achtung:** Gerade wenn es um die Bildschirmbreite geht, möchte man diese oft nur für _Bildschirme_ anwenden, nicht etwa wenn die Website ausgedruckt wird. Aus diesem Grund macht es Sinn im Filter zwei Features mit dem `and` Operator zu verketten:

```css
@media screen and (min-width: 1200px) {
    /** 
     * Diese Styles werden garantiert nur bei der Anzeige
     * auf Bildschirmen angewendet.
     */
}
```

#### Verkettung mehrerer Bedingungen

Wie schon bei `@media screen and (min-width: 1200px)` kann ich auch mehrere Bedingungen verknüpfen, z.B. um nur bestimmte Fensterbreiten anzusprechen:

```css
@media screen and (min-width: 800px) and (max-width: 1199px) {
    /** 
     * Diese Styles werden garantiert nur bei der Anzeige
     * auf Bildschirmen angewendet.
     */
}
```

### Fensterbreite: Media Query Range Syntax

Seit kurzem können auch Vergleichs-Operatoren genutzt werden, die sog. Media Query Range Syntax. Dies vereinfacht einiges.&#x20;

**Vorsicht:** Dieses Feature ist sehr neu und wird auf Mobiles erst seit November 2026 unterstützt. Siehe [caniuse.com](https://caniuse.com/?search=Media+Query+Range+Syntax).

```css
/* statt (max-width: 1199px): */
@media screen and (width < 1200px) {
  /* … */
}
@media screen and (width >= 1200px) {
  /* … */
}
```

Damit können auch Bereiche einfach abgefragt werden:

```css
/* statt screen and (min-width: 800px) and (max-width: 1199px): */
@media screen and (800px <= width < 1200px) {
  /* … */
}
```

### Ausrichtung: Hoch- / Querformat

Wenn ich wissen will, ob ein Bildschirm im Hoch- oder Querformat benutzt wird, kann ich dies abfragen:

```css
@media screen and (orientation: landscape) { /* Oder portrait für Hochformat */
  /* Styling für Querformat */
}
```

Das ist eher unüblich, öfter wird einfach die Fensterbreite (min-width/max-width) abgefragt.

## Optional: Container-Queries

Media-Queries beziehen sich immer auf die Breite des ganzen Ausgabe-Mediums (also das Fenster oder Display).&#x20;

In verschachtelten Layouts kann man auch auf die Breite eines einzelnen Containers innerhalb der Website reagieren. Dazu gibt es neu die Container-Queries. Mehr dazu bei den [Optionalen Themen > Container Queries](../../tag-3/optionale-themen/media-queries-1.md).
