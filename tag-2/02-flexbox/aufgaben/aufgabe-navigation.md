# Aufgabe Navigation

## Einfache Navigation

1. Erstelle in deinen bisherigen HTML-Dokumenten zwischen `<header>` und `<main>` ein Block imt dem Element `<nav>`&#x20;
2. Füge ein paar Links zu deinen verschiedenen Seiten ein
3. Formatiere den `<nav>`-Container mit CSS als Flexbox. Nutze die Definition `display: flex`, `justify-content`, `align-items` (und weitere nach Bedarf). Die Navigationspunkte sollen nebeneinander angeordnet werden. Wenn das Fenster zu schmal ist, sollen sie umgebrochen werden.&#x20;
4. Verschönere die Navigation, indem du die Links formatierst: Nutze dazu padding, border, background-color, :hover etc.
5. Teste das Layout und das Verhalten im Browser.&#x20;
6. Wenn alles gut aussieht, kannst du diese Navigation für alle Übungsseiten kopieren.&#x20;

## Zusatzaufgabe: Zweistufige aufklappende Navigation

Erstelle eine 2-stufige Navigation mit ausklappenden Untermenüs nur mit HTML & CSS, ohne JavaScript. Recherchiere dazu bei Bedarf selbständig im Netz:&#x20;

1. Erstelle im HTML-Dokument eine 2-stufige verschachtelte Navigation mit Listen-Elementen aufgebaut ist, oder nutze dieses Gerüst: \
   `<nav>`\
   &#x20; `<ul>`\
   &#x20;   `<li>`\
   &#x20;     `<a href="...">Hauptmenü 1</a>`\
   &#x20;     `<ul>`\
   &#x20;       `<li><a href="...">Untermenü 1</a></li>`\
   &#x20;       `Weitere Untermenüs...`\
   &#x20;     `</ul>`\
   &#x20;   `</li>`\
   &#x20;   `Weitere Hauptmenüs...`\
   &#x20; `</ul>`\
   `</nav>` \
   Studiere die Verschachtelung!&#x20;
2. Erstelle CSS-Regeln dazu, welches die Hauptmenüs horizontal anordnet und die Untermenüs drunter vertikal aufgeklappt (`position: absolute;`). Nutze für beides Flexbox-Definitionen.
3.  Erstelle CSS-Regeln, welche bei Hover über das `<li>`-Element des Hauptmenüs das Untermenü (`<ul>`) automatisch aufklappt. Das könnte so was ähnliches sein:&#x20;



    ```css
    nav ul ul {
      display: none;
      position: absolute;
    }

    nav li:hover > ul {
      display: block;
    }
    ```
4. Findest du heraus, wie die Untermenüs dynamisch sliden können, **ohne** JavaaScript?&#x20;

Du kannst auch ausgeklügeltere Beispiele im Internet suchen anschauen und etwas davon übernehmen. Z.B. [https://codepen.io/dinhhoa-214/pen/wjLyeR](https://codepen.io/dinhhoa-214/pen/wjLyeR)

