# 🛠️ Aufgabe Navigation

## Einfache Navigation

Lade das Grundgerüst herunter und entpacke es in ein neues Verzeichnis:

{% file src="../../.gitbook/assets/aufgabe-navigation.zip" %}

1. Formatiere den `<nav>`-Container mit CSS als Flexbox. Die Navigationspunkte sollen nebeneinander angeordnet werden, gleichmässig über die Fensterbreite verteilt. Wenn das Fenster zu schmal ist, sollen sie umgebrochen werden.&#x20;
2. Verschönere die Navigation, indem du die Links formatierst: Nutze dazu padding, border, background-color, :hover etc.

<div align="left"><figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure></div>

3. Teste das Layout und das Verhalten im Browser.&#x20;
4. Wenn alles gut aussieht, kannst du diese Navigation für alle Übungsseiten kopieren.&#x20;

**Zusatzaufgabe:**

1. Gestalte einen "smoothen" Hover-Effekt mit der Eigenschaft `transition`.

## Zusatzaufgabe: Zweistufige aufklappende Navigation

Erstelle eine 2-stufige Navigation mit ausklappenden Untermenüs nur mit HTML & CSS, ohne JavaScript. Recherchiere dazu bei Bedarf selbständig im Netz:&#x20;

1.  Erstelle im HTML-Dokument eine 2-stufige verschachtelte Navigation mit Listen-Elementen aufgebaut ist, oder nutze das folgende Gerüst und studiere die Verschachtelung!&#x20;

    ```
    <nav>
      <ul>
        <li>
          <a href="...">Hauptmenü 1</a>
          <ul>
            <li><a href="...">Untermenü 1</a></li>
            Weitere Untermenüs...
          </ul>
        </li>
        Weitere Hauptmenüs...
      </ul>
    </nav>
    ```
2.  Im CSS sollen erst mal die Aufzählungszeichen der Liste entfernt werden:&#x20;

    ```
    nav ul {
      margin: 0;
      padding: 0;
      list-style: none;
    }
    ```
3. Erstelle CSS-Regeln dazu, welches die Hauptmenüs horizontal anordnet und die Untermenüs drunter vertikal aufgeklappt (`position: absolute;`). Nutze für beides Flexbox-Definitionen.
4.  Erstelle CSS-Regeln, welche bei Hover über das `<li>`-Element des Hauptmenüs das Untermenü (`<ul>`) automatisch einblendet. Das könnte so was ähnliches sein:&#x20;

    ```css
    nav ul ul {
      position: absolute;
      display: none;
    }
    nav li:hover > ul {
      display: block;
    }
    ```
5. Findest du heraus, wie die Untermenüs dynamisch sliden können, **ohne** JavaaScript?&#x20;

Du kannst auch ausgeklügeltere Beispiele im Internet suchen anschauen und etwas davon übernehmen. Z.B. [https://codepen.io/dinhhoa-214/pen/wjLyeR](https://codepen.io/dinhhoa-214/pen/wjLyeR)

