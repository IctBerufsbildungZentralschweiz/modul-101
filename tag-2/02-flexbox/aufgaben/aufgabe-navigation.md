# Aufgabe Navigation

## Einfache Navigation

1. Erstelle in deinen bisherigen HTML-Dokumenten zwischen `<header>` und `<main>` ein Block imt dem Element `<nav>`&#x20;
2. Füge ein paar Links zu deinen verschiedenen Seiten ein
3. Formatiere im CSS den `<nav>`-Container mit der Definition `display: flex` und stelle sicher, dass die Navigationspunkte nebeneinander angeordnet werden
4. Mach die Navigation etwas schöner, indem du in CSS die Links formatierst. Nutze dazu Definitionen wie padding, border, background-color, :hover etc.
5. Teste das Layout und Verhalten in deinem Browser.&#x20;
6. Wenn alles gut aussieht, kopiere den `<nav>`-Block in deine anderen Übungsseiten.

## Zusatzaufgabe: Zweistufige aufklappende Navigation

Erstelle eine 2-stufige Navigation mit ausklappenden Untermenüs:

1. Erstelle im HTML-Dokument eine 2-stufige verschachtelte Navigation mit Listen-Elementen aufgebaut ist, oder nutze dieses Gerüst: \
   `<nav>`\
   &#x20; `<ul>`\
   &#x20;   `<li>`\
   &#x20;     `<a href="...">Hauptmenü 1`\
   &#x20;       `<ul>`\
   &#x20;         `<li>Untermenü 1</li>`\
   &#x20;         `Weitere Untermenüs...`\
   &#x20;       `</ul>`\
   &#x20;     `</a>`\
   &#x20;   `</li>`\
   &#x20;   `Weitere Hauptmenüs...`\
   &#x20; `</ul>`\
   `</nav>` \
   Studiere die Verschachtelung!&#x20;
2. Erstelle CSS-Regeln dazu, welches die Hauptmenüs horizontal anordnet und die Untermenüs drunter vertikal aufgeklappt (`position: absolute;`). Nutze für beides Flexbox-Definitionen.
3. Erstelle CSS-Regeln, welche bei Hover über ein Hauptmenü das Untermenü automatisch aufklappt.

Du kannst auch ausgeklügeltere Beispiele im Internet suchen anschauen und etwas davon übernehmen. Z.B. [https://codepen.io/dinhhoa-214/pen/wjLyeR](https://codepen.io/dinhhoa-214/pen/wjLyeR)

