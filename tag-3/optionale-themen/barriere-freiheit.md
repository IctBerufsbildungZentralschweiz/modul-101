# Barriere-Freiheit

Barrierefreiheit bedeutet, dass eine Website so gestaltet ist, dass **alle Menschen – unabhängig von Einschränkungen oder Geräten – sie problemlos nutzen können**.

Für Screenreader etc. ist vor allem korrekter, gut strukturierter HTML-Code wichtig, um die Seite zu verstehen.&#x20;

Einige Elemente sind dafür wichtig:&#x20;

* **Semantische HTML-Elemente verwenden:** \
  Screenreader und Suchmaschinen verstehen nur, _was_ ein Inhalt ist, wenn passende Elemente genutzt werden. \
  Beispiele: `<main>`, `<article>`, `<nav>`
* **Alternativtexte für Bilder:** \
  Visuelle Inhalte müssen für Menschen mit Seheinschränkung zugänglich sein.\
  Beispiel: `<img src="hund.png" alt="Brauner Hund rennt über eine Wiese">`&#x20;
* **Kontraste und lesbare Schriftgrössen:** \
  Text muss gut erkennbar sein – für Menschen mit und ohne Sehbeeinträchtigung.\
  Die Schrift muss genügend Kontrast haben und mind. 16 px gross sein.
* **Formulare richtig beschriften:** \
  Labels müssen mit Inputs verknüpft sein, damit Screenreader und Nutzer:innen verstehen, was sie eingeben sollen.
* **Überschriften:** \
  `<h1>`-`<h6>`-Elemente sind logisch und korrekt eingesetzt.&#x20;
* **ARIA-Attribute („Accessible Rich Internet Applications“):**\
  ARIA-Attribute helfen Screenreadern und ähnlichen Geräten, eine Webseite zu verstehen. Bei einfachen Webseiten und Elementen macht das meist keinen Sinn, da reicht gut strukturiertes HTML. ARIA-Attribute sollten nur bei komplexen Elementen eingesetzt werden. \
  Links: [ARIA-Tutorial](https://gehirngerecht.digital/aria/), [Website auf Barrierefreiheit testen](https://wiki.selfhtml.org/wiki/Barrierefreiheit/Webseiten_auf_Barrierefreiheit_testen), [ARIA-Referenz](https://developer.mozilla.org/de/docs/Web/Accessibility/ARIA/Reference)
