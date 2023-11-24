# Einheiten

In CSS werden verschiedene Einheiten verwendet, um Größenangaben für Abstände, Größen und Positionen von Elementen auf einer Webseite festzulegen. Hier sind einige der wichtigsten Einheiten und ihre Verwendungszwecke:

1. **Pixel (px):**
   * Absolute Einheit, die einen einzelnen Punkt auf einem Bildschirm darstellt.
   * Häufig für feste Größen verwendet, die auf genaue Pixelwerte angewiesen sind.
   * Beispiel: `.slider-image { height: 200px; }`\
     Alle Bilder eines Sliders sollen genau 200px hoch angezeigt werden.&#x20;
2. **Prozent (%):**
   * Relativ zur Größe des übergeordneten Elements.
   * Ermöglicht eine flexible und reaktionsschnelle Gestaltung, da sich die Größe an die des übergeordneten Elements anpasst.
   * Beispiel: `.map-container { width: 50%; }`\
     Einen Kartenausschnitt auf die halbe Breite des umgebenden Containers skalieren.
3. **Viewport Height (vh) und Viewport Width (vw):**
   * Relativ zur Höhe bzw. Breite des Browserfensters.
   * Nützlich, um Elemente proportional zur Größe des sichtbaren Bereichs des Browserfensters zu dimensionieren.&#x20;
   * Beispiel: `.container { min-height: 100vh; }` \
     Einen Container mindestens so hoch wie das Fenster machen&#x20;
4. **Relative Einheiten (em und rem):**
   * "rem" ist relativ zur Schriftgröße des Root-Elements (\<html>). Meist entspricht 1rem = 16px
   * "em" ist relativ zur Schriftgröße des übergeordneten Elements. \
     Ist recht unberechenbar und sollte nicht mehr verwendet werden.
   * Hilfreich für eine skalierbare Gestaltung, insbesondere bei Schriftgrößen, wodurch sich die Größe anderer Elemente entsprechend anpasst. => Heute beide nicht mehr nötig, da Browser auch Pixel korrekt skalieren können.&#x20;
   * Beispiel: `h1 { font-size: 2.5rem; }`\
     Überschrift 1 wird mit 2.5 mal so gross wie Standard-Text angezeigt, also 2.5x16px = 40px&#x20;
5. **Absolute Längeneinheiten (cm, mm, in, pt, pc):**
   * Absolute Einheiten, die physische Größen wie Zentimeter (cm), Millimeter (mm), Zoll (in), Punkte (pt) und Pica (pc) darstellen.
   * Für den Druck oder spezifische Ausgabeformate verwendet, weniger gebräuchlich für Webdesign.
   * Beispiel: `body { width: 21cm; }`\
     Skaliert ein Dokument zum Ausdrucken auf A4-Breite
6. **Kombinierte Masse berechnen (calc(...))**
   * Obige Einheiten können kombiniert werden, beispielsweise um eine Breite relativ zu einem umgebenden Element zu berechnen.
   * Beispiel: `.portrait-text { width: calc(100% - 200px); }`\
     Macht einen Text 200px weniger breit als den gesamten Contanier, z.B. weil daneben noch ein Bild mit 200px Platz haben muss.&#x20;
   * Achtung: Beachte die Leerschläge zwischen den Zahlen und Operatoren!&#x20;
   * Selber ausprobieren: [https://developer.mozilla.org/en-US/docs/Web/CSS/calc](https://developer.mozilla.org/en-US/docs/Web/CSS/calc)
