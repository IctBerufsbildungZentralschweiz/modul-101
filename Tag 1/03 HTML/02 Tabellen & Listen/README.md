# Tabellen & Listen
## Tabellen
Eine Tabelle ist eine strukturierte Zusammenstellung von Daten in Spalten und Reihen. Eine Tabelle erlaubt es, eine Vielzahl von Daten mit einem konkreten Zusammenhang zu interpretieren und zu vergleichen.

![Tabelle](src/tabelle.png)

Nun erstellen wir gemeinsam die Tabelle oben:

Der Inhalt jeder Tabelle wird umschlossen von diesen zwei Tags: `<table></table>`:

```html
<table></table>
```
Der kleinste Teil einer Tabelle ist eine Zelle. Eine Zelle wird mit dem `<td>`-Tag ('td' steht für 'table data') erstellt. Erstellen wir nun die Inhalte der Tabelle:

```html
<table>
    <td>Name</td>
    <td>Alter</td>
    <td>Petra</td>
    <td>15</td>
    <td>Marion</td>
    <td>18</td>
    <td>Peter</td>
    <td>14</td>
    <td>Martin</td>
    <td>17</td>
</table>
```
Wie du jetzt feststellen wirst sind die einzelnen Reihen nicht untereinander, sondern alle in einer Reihe. Geben wir somit keine weiteren Informationen mit, werden sämtliche `<td>`-Tags als eine Reihe betrachtet.

Um dies zu verhindern und eine neue Reihe zu erzwingen, können wir das `<tr>`-Tag nutzen ('tr' steht für 'table row'). Deklariere nun mit dem `<tr>`-Tag das Anfang und Ende einer Tabellen-Reihe:

```html
<table>
    <tr>
        <td>Name</td>
        <td>Alter</td>
    </tr>
    <tr>
         <td>Petra</td>
         <td>15</td>   
    </tr>
    <tr>
        <td>Marion</td>
        <td>18</td>
    </tr>
    <tr>
        <td>Peter</td>
        <td>14</td>
    </tr>
    <tr>
        <td>Martin</td>
        <td>17</td>
    </tr>
</table>
```
Die erste Reihe eine Tabelle ist meistens etwas spezielles, da sich dort keine Daten befinden, sondern Überschriften. HTML hat darum dafür ein eigenes Tag vorgesehen, das `<th>`-Tag ('th' steht für 'Table Heading'). Ersetze nun die `<td>`-Tags der ersten Reihe mit `<th>`-Tags:

```html
<table>
    <tr>
        <th>Name</th>
        <th>Alter</th>
    </tr>
    <tr>
         <td>Petra</td>
         <td>15</td>   
    </tr>
    <tr>
        <td>Marion</td>
        <td>18</td>
    </tr>
    <tr>
        <td>Peter</td>
        <td>14</td>
    </tr>
    <tr>
        <td>Martin</td>
        <td>17</td>
    </tr>
</table>
```

## Listen
Wie auch Tabellen verfügen auch Listen über eine spezielle Anordnung der HTML-Elemente. So wird jede Liste mit einem `<ul>`-Tag ('ul' steht für 'unordered List') oder einem `<ol>`-Tag ('ol' steht für 'ordered List) umschlossen. Wir erstellen dazu gleich zwei Beispiele:

```html
<ul></ul>
<ol></ol>
```

Der kleinste Teil einer Liste ist ein Aufzählungspunkt. Ein Aufzählungspunkt wird mit dem `<li>`-Tag  erstellt. Erstellen wir nun die Inhalte der beiden Liste:

```html
<ul>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt</li>
    <li>Dritter Punkt</li>
</ul>
<ol>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt</li>
    <li>Dritter Punkt</li>
</ol>
```

Indem man eine Liste in einen Aufzählungspunkt setzt, wird keine Unterliste erstellt:

```html
<ul>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt</li>
    <li>Dritter Punkt
        <ul>
            <li>Erster Unterpunkt</li>
            <li>Zweiter Unterpunkt</li>
        </ul>
    </li>
</ul>
<ol>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt</li>
    <li>Dritter Punkt
        <ol>
            <li>Erster Unterpunkt</li>
            <li>Zweiter Unterpunkt</li>
        </ol>
    </li>
</ol>
```

Die Listen-Typen lassen sich auch beliebig miteinander kombinieren:

```html
<ul>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt</li>
    <li>Dritter Punkt
        <ol>
            <li>Erster Unterpunkt</li>
            <li>Zweiter Unterpunkt</li>
        </ol>
    </li>
</ul>
<ol>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt</li>
    <li>Dritter Punkt
        <ul>
            <li>Erster Unterpunkt</li>
            <li>Zweiter Unterpunkt</li>
        </ul>
    </li>
</ol>
```


