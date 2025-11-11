# Grids vs. Flexbox

Eine klare Antwort auf «Wann verwende ich welche Methode?» gibt es nicht. In bestimmten Anwendungsfällen ist Flexbox die richtige Wahl, in anderen CSS Grids. In vielen Anwendungsfällen lassen sich beide Varianten verwenden. Der Aufwand und die Codemenge können sich jedoch deutlich unterscheiden.&#x20;

Folgende Fakten können dir aber bei der Entscheidung helfen:

* Mit Grids kann eine feste Anzahl von Elementen angeordnet werden, mit Flexbox eine variable Anzahl von Elementen.&#x20;
* **Flexbox** ist primär für das Platzieren von **Elementen in einer Dimension** konzipiert, also für horizontal oder vertikal (Beispiel: Navigation).&#x20;
* Flexbox eignet sich somit besser zum Umsetzen von einzelnen Komponenten, bei denen Kontrolle über die Reihenfolge und Platzierung von Elementen und Text benötigt wird.
* **Grids** sind für das Platzieren von **Elementen in zwei Dimensionen** konzipiert (Beispiel: Basislayout, Bildergalerien).\
  Grids eignen sich deshalb für die Umsetzung komplexer Layouts. Das HTML Markup und der CSS Code werden deutlich übersichtlicher sein, wenn du mit Grids arbeitest.
* Grids benötigen sehr wenig Code, wenn es darum geht, eine Website responsive zu machen. Bei Flexbox müssen meistens mehr Eigenschaften für unterschiedliche Bildschirmgrössen überschrieben werden.
* Ausgefallene Layouts lassen sich mit Grids einfacher umsetzen als mit Flexbox (siehe z. B. [https://codepen.io/rrenula/pen/LzLXYJ](https://codepen.io/rrenula/pen/LzLXYJ)).
