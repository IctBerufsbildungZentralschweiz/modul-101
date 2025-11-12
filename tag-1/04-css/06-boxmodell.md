# Boxmodell

Wie dir vielleicht bereits aufgefallen ist, geht es bei Webseiten oft darum, Boxen zu erstellen (HTML) und Boxen zu gestalten (CSS). Die meisten HTML-Elemente sind somit Boxen oder Schachteln, welche übereinander und nebeneinander gestapelt werden.

Mit CSS können Grösse, Farben, Position usw. bestimmt werden.

<div align="center"><img src="../../.gitbook/assets/boxmodell-gif.gif" alt="boxmodell-gif"></div>

## Eigenschaften von Boxen

Das CSS-Layout basiert auf dem Box-Modell. Jede Box, die Platz auf einer Webseite einnimmt, hat unter anderen folgende Eigenschaften:

* **Aussenabstand (`margin`):** \
  Der Abstand vom Border bis zum nächsten benachbarten Element.
* **Rahmen (`border`):** \
  Der Border ist der Rahmen um ein Element.
* **Innenabstand (`padding`):** \
  Das Padding ist der Raum zwischen Inhalt und Rahmen eines Elements.

![Boxmodell](../../.gitbook/assets/boxmodell.png)

### 🛠️ Erforschen

1. Rufe eine beliebige Website im Internet auf, öffne die "Developer Tools" (Rechtsklick auf ein Element > "Untersuchen" oder `F12`) und suche das Tab "Computed".&#x20;
2. Schau dir die Grafik des Box-Models eines HTML-Elements unter "Computed" an und darunter, woher die Abstände in CSS kommen.&#x20;
3. Wechsle zwischen den Tabs "Styles" und "Computed", das ist anders?&#x20;
4. Untersuche noch ein paar andere Elemente auf der gleichen Seite.&#x20;

### Beispiele: 4 Seiten einer Box - top, right, bottom, left

Die Abstände und Rahmen einer Box können für alle 4 Seiten einzeln oder zusammen oder einzeln definiert werden. Ein paar Beispiele:&#x20;

```css
.element-x {
    margin: 20px; /* Aussenabstand 20px, auf allen Seiten gleich */
    border: 1px solid blue; /* Rahmen: 1px breit, durchgezogen, blau */
    border-bottom: 2px double; /* Rahmen unten überschreiben (breiter) */
    padding-top: 10px; /* Innenabstände... */
    padding-right: 20px;
    padding-bottom: 15px;
    padding-left: 20px;
}
.element-y {
    margin: 0 40px; /* Aussenabstand oben & unten 0px, rechts & links 40px */
    border: 2px dashed #CC0000; /* Rahmen: 2px, gestrichelt, rot */
    border-radius: 10px; /* Runde Ecken */
    padding: 10px 20px 15px 20px; /* Innenabstand wie oben, zusammengefasst: oben rechts unten links */
}
.image {
    border-radius: 50%; /* Schneidet ein Bild kreisrund aus */
}
```

### 🛠️ Ausprobieren

Probier die Möglichkeiten aus: [w3schools.com/css/tryit.asp?filename=trycss\_boxmodel](https://www.w3schools.com/css/tryit.asp?filename=trycss_boxmodel)

## Höhe, Breite

Für jede Box kann die Breite und Höhe definiert werden. Häufige Masseinheiten sind Pixel oder Prozent, manchmal auch `vw`/`vh` , selten `rem/em`.

```css
.container {
    width: 200px; // Breite 
    max-width: 50%; // Maximum 50% der übergeordneten Box breit
    height: 600px; // Höhe
    min-height: 50vh; // Minimal halbe Viewporthöhe (Fensterhöhe)
}
```

**Hinweis:** Standardmässig beziehen sich `width` und `height` nur auf den Inhaltsbereich. Padding und Border kommen zusätzlich dazu. Mit `box-sizing: border-box;` kann das Verhalten geändert werden, sodass `width` und `height` den gesamten Bereich inkl. Padding und Border umfassen.

## Übergroser Inhalt (`overflow`)

Wenn der Inhalt einer Box grässer ist als die angegebene Breite oder Höhe der Box, kannst du bestimmen, was passieren soll:&#x20;

* `overflow: visible`: Inhalt soll über die Box hinausragen
* `overflow: hidden`: Zu grosser Teil soll ausgeblendet werden
* `overflow: scroll`: Scrollbalken anzeigen

Genauere Beschreibungen findest du z.B. auf [https://css-tricks.com/css-is-awesome/](https://css-tricks.com/css-is-awesome/)

## 🛠️ Aufgaben zum Boxmodell

Style deine Website "Über mich" weiter und ¨berprüfe nach jedem Schritt das Ergebnis im Browser.&#x20;

1.  Semantische Strukturelemente:&#x20;

    * Stelle sicher, dass deine Seite die Strukturelemente `<header>`, `<main>` und `<footer>` enthält. Sie sollen direkt unter dem \<body>-Element sein, also nicht tiefer verschachtelt. \
      Die drei Blöcke sollen unterschiedliche Hintergrundfarben haben.&#x20;
    * Die drei Strukturelemente soll einen Innenabstand von 40px haben.
    * Der Header soll 200px hoch sein.

    Teste im Browser mit den Entsicklungswerkzeugen (Untersuchen / F12), ob die Abstände richtig angezeigt werden.
2. Die beiden Adresse sollen nebeneinander stehen: \
   Definiere für beide Adress-Blöcke jeweils eine Breite von 50% und setze jeweils die Eigenschaft `display: inline;`&#x20;

Überprüfe den Code anschliessend mit dem [CSS-Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) und korrigiere allfällige Fehler.\


**Zusatzaufgaben für schnelle Lernende:**

1. Fixiere den Footer so, dass es immer ganz unten am Fensterrand ist, unabhängig von Fenstergrösse und Scrolling.
2. Probiere selber noch was aus.
