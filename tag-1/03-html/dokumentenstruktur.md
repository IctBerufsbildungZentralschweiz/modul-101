# Strukturelemente (Container)

### Strukturelement \<div>

Um Elemente innerhalb eines Dokuments besser zu strukturieren, hat HTML das Strukturelement `<div>` vorgesehen. Das `<div>`-Element (Document Division Element) ist ein generischer Container für Inhalte, der keine eigene Bedeutung hat, ausser dass er Elemente zusammenfasst, z.B. um sie zu stylen (mit Hilfe des `class` oder `id` Attributs).

Beispiel: Wir möchten, dass die folgenden Absätze mit einer Hintergrundfarbe hinterlegt sind, ohne einen weissen Absand dazwischen zu haben.

```markup
<p>Ich bin ein erster Absatz.</p>
<p>Ich bin ein zweiter Absatz.</p>
```

```css
p {
    background-color: indianred;
}
```

Dies entspricht jedoch nicht unserem gewünschten Ergebnis:

![Absätze mit Hintergrund](../../.gitbook/assets/p-background.PNG)

Um das Ziel zu erreichen, umklammern wir die beiden Absätze mit einem `<div>`-Strukturelement und stylen das `<div>`-Element:

```markup
<div class="red">
    <p>Ich bin ein erster Absatz.</p>
    <p>Ich bin ein zweiter Absatz.</p>
</div>
```

```css
.red {
    background-color: indianred;
}
```

![Div mit Hintergrund](../../.gitbook/assets/div-background.PNG)

**Aufgabe:** Teste dieses \<div>-Element mit [Codepen.io](https://codepen.io/sternenvogel/pen/dPMypGe)

### Semantische Strukturelemente

Semtantische Elemente sind gleichbedeutend wie `<div>`-Strukturelemente, sie haben aber einen vordefinierten Anwendungszweck.

So sollte das `<header>`-Element ausschliesslich für die Strukturierung des Kopfbereichs von Sektionen und Websites verwendet werden.

| Semantisches Element | Beschreibung                                                                                       | Möglicher Inhalt                         |
| -------------------- | -------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| `<header>`           | Das Element beinhaltet Kopfelemente der Website oder einer Sektion.                                | Navigation, Logo, Suchfeld               |
| `<nav>`              | Das Element beinhaltet eine Navigation.                                                            | Navigation                               |
| `<main>`             | Das Element beinhaltet den Hauptinhalt der Website.                                                | Hauptinhalt                              |
| `<section>`          | Das Element unterteilt ein Dokument in mehrere allgemeine Sektionen.                               | <p>Produkte, <br>News</p>                |
| `<article>`          | Eine Sektion kann mehrere Artikel umfassen.                                                        | <p>Ein Produkt, <br>ein News-Beitrag</p> |
| `<aside>`            | Das Element beinhaltet Informationen, welche mit dem Hauptinhalt der Website in Verbindung stehen. | Sidebar                                  |
| `<footer>`           | Das Element beinhaltet Fusselemente der Website oder einer Sektion.                                | Copyright, nützliche Links               |

Die semantischen Elemente erleichtern vorallem die Human-Readability des HTML- und CSS-Codes.

**Darum gilt:** Generische `<div>`-Elemente sollten nur genutzt werden, wenn kein semantisches Element geeignet ist.

Schau dazu im Browser die HTML-Struktur einer Beispielseite an: \
[der-informationsdesigner.de/agentur-blog/allgemein/was-ist-webdesign](https://www.der-informationsdesigner.de/agentur-blog/allgemein/was-ist-webdesign/)
