# Einheiten

In CSS werden verschiedene Einheiten verwendet, um Grössenangaben für Abstände, Grössen und Positionen von Elementen auf einer Webseite festzulegen. Hier sind einige der wichtigsten Einheiten und ihre Verwendungszwecke:

## Häufig verwendete Einheiten

**Pixel (`px`)**

* Absolute Einheit, die einen einzelnen Punkt auf einem Bildschirm darstellt.
* Häufig für feste Grössen verwendet, die auf genaue Pixelwerte angewiesen sind.
* Beispiel: `.slider-image { height: 200px; }`\
  Alle Bilder eines Sliders sollen genau 200px hoch angezeigt werden.

**Prozent (`%`)**

* Relativ zur Grösse des übergeordneten Elements.
* Ermöglicht eine flexible und reaktionsschnelle Gestaltung, da sich die Grösse an die des übergeordneten Elements anpasst.
* Beispiel: `.map-container { width: 50%; }`\
  Einen Kartenausschnitt auf die halbe Breite des umgebenden Containers skalieren.

**Relative Einheiten (`rem` und `em`)**

Die CSS-Einheit **em** stammt aus dem traditionellen Buchdruck und der Typografie und steht dort für die Breite des Großbuchstabens **M** (englisch _equal to m_)

* "rem" ist relativ zur Schriftgrösse des Root-Elements (\<html>).\
  Das Root-Element hat meist die Schriftgrösse 1rem = 16px.
* "em" ist relativ zur Schriftgrösse des übergeordneten Elements.\
  _&#x49;st recht unberechenbar und sollte nur in Ausnahmen verwendet werden._
* **Anwendungsbereich:** Wird vor allem eingesetzt für skalierbare Schriftgrössen, Masse und Abstände für barrierefreie Websites. Wird die Standard-Schriftgrösse des Browsers verändert, dann werden rem-Einheiten proportional dazu skaliert.
* **Beispiel:** `h1 { font-size: 2.5rem; }`\
  Überschrift 1 wird 2.5 mal so gross wie Standard-Text angezeigt, also 2.5x16px = 40px

**Viewport Height (`vh`) und Viewport Width (`vw`)**

* Relativ zur Höhe bzw. Breite des Browserfensters.
* Nützlich, um Elemente proportional zur Grösse des sichtbaren Bereichs des Browserfensters zu dimensionieren.
* Beispiel: `.container { min-height: 100vh; }`\
  Den Container mind. so hoch wie das Fenster machen, damit der Footer unten bleibt.

## Berechnete Einheiten

**Kalkulation: calc()**

* Obige Einheiten können kombiniert werden, beispielsweise um eine Breite relativ zu einem umgebenden Element zu berechnen.
* Beispiel: `width: calc(100% - 200px);`\
  Macht einen Text 200px weniger breit als der gesamte Container, z.B. weil daneben noch ein Bild mit 200px Platz haben muss.
* Achtung: Beachte die Leerschläge zwischen den Zahlen und Operatoren!
* Selber ausprobieren: [https://developer.mozilla.org/en-US/docs/Web/CSS/calc](https://developer.mozilla.org/en-US/docs/Web/CSS/calc)

**Vergleichen: min(), max(), clamp():**

* min() liefert das kleinere von 2 Massen, z.B. width: min(200px, 50%);
* max() liefert das grössere von 2 Massen, z.B. width: max(200px, 50%);
* clamp() vergleicht 3 Werte: Einen Mindestwert, einen Idealwert und einen Höchstwert, z.B. width: clamp(200px, 50%, 400px);

**min(), max(), clamp()** sind anschaulich beschrieben auf [https://web.dev/articles/min-max-clamp](https://web.dev/articles/min-max-clamp).

## Selten genutzte Einheiten

**Absolute Längeneinheiten (`cm`, `mm`, `in`, `pt`, `pc`)**

* Absolute Einheiten, die physische Grössen wie Zentimeter (cm), Millimeter (mm), Zoll (in), Punkte (pt) und Pica (pc) darstellen.
* **Anwendungsbereich:** Für den Druck oder spezifische Ausgabeformate verwendet.\
  _&#x57;eniger gebräuchlich für Webdesign._
* **Beispiel:** `body { width: 21cm; }`\
  Skaliert ein Dokument zum Ausdrucken auf A4-Breite

## 🛠️ Aufgaben (optional)

1. **Skaliere** ein Bild in deiner Seite "Über mich" mit verschiedenen Einheiten: `px, %, vw`
2. Teste, was `border-radius: 50%;` mit deinem Portraitbild macht.
3. **Zu breite Bilder:** Füge ein breites Bild ein und mache das Fenster so schmal, bis das Bild nicht mehr Platz hat. Was passiert? Teste nun das gleiche, wenn du für alle Bilder `max-width: 100%` definierst. Welchen Selektor brauchst du, damit die Regel für alle Bilder gilt?
4. Teste zusätzlich zu `width` die CSS-Eigenschaft `min-width: 50%` oder `max-width: 50%` an einem Element.

**Zusatzaufgabe:**

* Teste verschiedene Funktionen für einen Textblock oder ein Bild: `min(), max(), calc(), clamp()`
