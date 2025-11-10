# HTML-Grundlagen
HTML ist keine Programmiersprache, sondern eine Auszeichnungssprache; sie ist dazu gedacht, einer Website Struktur zu verleihen.

Die Sprache besteht aus einer Reihe von Elementen, Tags genannt, welche um verschiedene Teile des Inhalts herum platzieren werden können, um diesem eine spezielle Aufgabe zuzuweisen. Zum Beispiel kann damit einen Text in einen Link verwandelt werden.

Ein Beispiel:

```markup
Meine Katze hat zwei Pfötchen.
```

Mit `<p>` können spezifizieren, das es sich um einen Absatz handelt:

```markup
<p>Meine Katze hat zwei Pfötchen.</p>
```
## Aufbau eines HTML-Elements (Tag)

Das oben beschriebene Beispiel zeigt, wie ein HTML-Element aufgebaut ist:

![Aufbau eines HTML-Elements](src/html-grundlagen.jpg)

* **Das öffnende Tag:** Dieses besteht aus dem Namen des Elements (in diesem Fall ein p für _paragraph_ (engl.: Absatz)), welcher zwischen zwei spitzen Klammern eingesetzt ist. Dies zeigt an, wo das Element beginnt — in diesem Fall am Anfang unseres Absatzes.
* **Der Inhalt:** Dies ist der Inhalt des Elements, in diesem Fall einfach nur Text.
* **Das schliessende Tag:** Dieses sieht genauso aus wie das öffnende Tag, bis auf den zusätzlichen Schrägstrich (Slash) vor dem Namen des Elements. Dieser Tag kommt an das Ende des Elementes — in diesem Fall am Ende des Absatzes.
* **Das Element:** Das öffnende Tag, der Inhalt und das schliessende Tag gemeinsam ergeben zusammen das Element.

## Attribute

Elemente können Attribute enthalten. Das sieht so aus:

![Attribut eines HTML-Elements](src/html-attribut.jpg)

Attribute enthalten Zusatzinformationen über das Element, welche nicht als eigentlicher Inhalt anzeigt werden. Das `class`-Attribut beispielsweise kann später dazu verwendet werden, das Element mit CSS zu gestalten.

Syntax von Attributen:

* Vor dem Attribut muss immer ein **Abstand (Leerzeichen)** stehen.
* Die **Attributnamen** sind vordefiniert, siehe [Referenz der HTML-Attribute](https://developer.mozilla.org/de/docs/Web/HTML/Reference/Attributes).
* Nach dem Attributnamen folgt meist ein Gleichheitszeichen, gefolgt von einem **Wert** in Anführungs- und Schlusszeichen.

## Verschachtelte Elemente

Mehrere Elemente können ineinander verschachtelt werden. Wenn wir also besonders betonen wollen, dass unsere Katze **zwei** Beine hat, können wir dieses einzelne Wort in einem `<strong>` Element verpacken.

```markup
<p>Meine Katze hat <strong>zwei</strong> Pfötchen.</p>
```

Folgendes Beispiel ist **nicht richtig**, da die Elemente nicht ineinander verschachtelt sind, sondern überlappen. Das Element, das zuerst geöffnet wird, muss als letztes geschlossen werden.

```markup
<p>Meine Katze hat <strong>zwei Pfötchen.</p></strong>
```

## Leere Tags
Gewisse Elemente haben keinen Inhalt, diese werden leere Elemente genannt. Beispielsweise das `<img>` Element:

```markup
<img src="images/mein-logo.png" alt="Mein Firmenlogo">
```

Das `<img>`-Tag beinhaltet zwei Attribute, aber es gibt kein schliessendes `</img>`-Tag und keinen Inhalt in dem Element. Das `<img>`-Tag braucht keinen Inhalt um einen Effekt zu haben. Es bindet ein Bild an der entsprechenden Stelle in der HTML-Seite ein.

## Liste der HTML-Tags
Unter folgendem Link befindet sich eine Liste der HTML-Tags mit Beschreibung und Beispielen:

[Liste von HTML-Tags](https://www.w3schools.com/tags/)

## 🛠️ Aufgabe

Gehe auf [Codepen.io](https://codepen.io/pen/) und probiere folgende Tags aus:

```markup
- <h1> bis <h6>
- <em>
- <a>
- <img>
```
