# CSS Grids vs. Flexbox

Der Unterschied zwischen Flexbox und CSS Grids ist auf den ersten Blick nicht klar ersichtlich. In bestimmten Anwendungsfällen ist Flexbox die richtige Wahl, in anderen CSS Grids. 

Eine klare Antwort auf «Wann verwende ich welche Methode?» gibt es nicht. Folgende Fakten können dir aber bei der Entscheidung helfen:

* Flexbox ist primär für das Platzieren von Elementen in einer Dimension konzipiert, also für horizontal oder vertikal (Beispiel: Navigation).
* Grids sind für das Platzieren von Elementen in zwei Dimensionen konzipiert (Beispiel: Basislayout, Bildergalerien).
* In vielen Anwendungsfällen lassen sich theoretisch beide Varianten verwenden. Der Aufwand und die Codemenge können sich bei der Umsetzung jedoch deutlich unterscheiden.
* Flexbox eignet sich besser zum Umsetzen von einzelnen Komponenten bei denen viel Kontrolle über die Platzierung von Elementen und Text benötigt wird.
* CSS Grids benötigen sehr wenig Code wenn es darum geht eine Website responsive zu machen. Bei Flexbox müssen meistens mehr Eigenschaften für unterschiedliche Bildschirmgrössen überschrieben werden.
* Bei komplexeren Layouts wird das HTML Markup und der CSS Code deutlich übersichtlicher sein, wenn du mit CSS Grids arbeitest.
* Ausgefallene Layouts lassen sich mit CSS Grids einfacher umsetzen als mit Flexbox (siehe z. B. https://codepen.io/rrenula/pen/LzLXYJ).
* Flexbox hat aktuell den besseren Browser-Support falls alte Browser (< IE11) unterstützt werden müssen.

### Aufgabe: Konzept erstellen
Bildet Gruppen von 3 Personen und überlegt euch, wie sich das [vorgefertigte Design](./src/design_hochzeit.pdf) am besten in HTML und CSS umsetzen lässt. Macht euch Gedanken darüber...

* ...wo der Einsatz von CSS Grids sinnvoll ist.
* ...wo der Einsatz von Flexbox sinnvoll ist.
* ...wo ihr welche semantischen Tags einsetzt.

Zeichnet dazu die entsprechenden Bereiche im Design ein und notiert die dazugehörigen Tags und CSS-Attribute.