# Farben

### RGB-Farbmodell

Auf Bildschirmen und Beamer werden die Farben _additiv_ aus den drei Grundfarben **R**ot, **G**rün und **B**lau zusammengemischt:&#x20;

<figure><img src="../../.gitbook/assets/rgb-farbmodell-1-1024x623.png" alt=""><figcaption><p>RGB Farbodell</p></figcaption></figure>

In CSS können Farben mit Farbnamen oder Farbwerten Arten definiert werden.

### Farben in CSS mit Farbnamen

z.B. black, white, red, darkgrey, lightblue, rebeccapurple, orange.&#x20;

```css
.navigation {
    color: darkblue;
    background-color: lightgrey;
}
```

\> [Liste aller unterstützen Farbnamen](https://www.w3schools.com/cssref/css\_colors.php)

### Farben in CSS mit Farbwerten

Es gibt viele [verschiedene Farbmodelle](https://developer.mozilla.org/en-US/docs/Web/CSS/color\_value), die in CSS genutzt werden können. Die häufigsten sind Angaben auf RGB-Basis:&#x20;

<figure><img src="../../.gitbook/assets/rgb-farbmodell.png" alt=""><figcaption><p>RGB Farbmodell mit Farbwerten</p></figcaption></figure>

```css
/* RGB (Red, Green, Blue): */
color: rgba(254, 233, 93);

/* RGB Hexadezimal: */
color: #fee95d;
```

Wenn die beiden Hexadezimal-Ziffern je Farbe übereinstimmen, können die abgekürzt werden:&#x20;

```css
color: #fff; /* = #ffffff */
color: #d20; /* = #dd2200 */
color: #000; /* = #000000 */
```

Beide können zusätzlich eine 4. Zahl für Transparenz enthalten:&#x20;

```css
/* RGB (Red, Green, Blue) mit 50% Transparenz: */
color: rgba(254, 233, 93, 0.5);

/* RGB Hexadezimal mit 50% Transparenz*/
color: #fee95d88;
```

### Farbwähler im Browser und Visual Studio Code nutzen

Im Browser kannst du über Rechts-Klick > Untersuchen oder mit \[F12] in die DevTools wechseln und dort die Farbe eines Elements in CSS finden und verändern:&#x20;

<figure><img src="../../.gitbook/assets/Browser-Color-Tool.png" alt=""><figcaption><p>DevTools Farbwähler</p></figcaption></figure>

In Visual Studio Code gibt es beim Bearbeiten von CSS ein ähnliches Tool:&#x20;

<figure><img src="../../.gitbook/assets/VSC-Color-Tool.png" alt=""><figcaption><p>Farbwähler in Visual Studio Code</p></figcaption></figure>

1. Farbwähler öffnen
2. Zwischen Farbmodellen umschalten
3. Transparenz setzen

### Links

* [Farbwähler: Farbwerte finden und umwandeln](https://www.hexcolortool.com/) (Hexcolortool)
* [Farbrad zum Generieren einer ganzen Farbpalette](https://color.adobe.com/de/create/color-wheel) (Adobe)
* [Weitere Arten von Farbwerten selber ausprobieren](https://developer.mozilla.org/en-US/docs/Web/CSS/color) (Mozilla)
