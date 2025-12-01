# 📖 Listen & Tabellen

## Listen

Listen verfügen über eine spezielle Anordnung der HTML-Elemente. Jede Liste wird mit einem `<ul>`-Tag ('unordered list') oder einem `<ol>`-Tag ('ordered list') umschlossen. Darin enthalten sind Aufzählungspunkte, eingefasst durch ein `<li>`-Tag:

{% columns %}
{% column width="58.333333333333336%" %}
**HTML-Code:**

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
{% endcolumn %}

{% column width="41.666666666666664%" %}
**Resultat:**



![](<../../.gitbook/assets/image (5).png>)
{% endcolumn %}
{% endcolumns %}

Die Listen kann man beliebig verschachteln und die Listentypen auch mischen:

{% columns %}
{% column width="58.333333333333336%" %}
**HTML-Code:**

```html
<ul>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt
        <ul>
            <li>Erster Unterpunkt</li>
            <li>Zweiter Unterpunkt</li>
        </ul>
    </li>
    <li>Dritter Punkt</li>
</ul>
<ol>
    <li>Erster Punkt</li>
    <li>Zweiter Punkt
        <ol>
            <li>Erster Unterpunkt</li>
            <li>Zweiter Unterpunkt</li>
        </ol>
    </li>
    <li>Dritter Punkt
        <ul>
            <li>Erster Unterpunkt</li>
            <li>Zweiter Unterpunkt</li>
        </ul>
    </li>
</ol>
```
{% endcolumn %}

{% column width="41.666666666666664%" %}
**Resultat:**



<img src="../../.gitbook/assets/image (6).png" alt="" data-size="original">
{% endcolumn %}
{% endcolumns %}

## Tabellen

Eine Tabelle ist eine strukturierte Zusammenstellung von Daten in Spalten und Reihen:&#x20;

<table><thead><tr><th width="120">Name</th><th width="120">Alter</th></tr></thead><tbody><tr><td>Petra</td><td>15</td></tr><tr><td>Marion</td><td>18</td></tr><tr><td>Martin</td><td>17</td></tr></tbody></table>

Der Inhalt jeder Tabelle wird von einem `<table>`-Tag umschlossen:

```markup
<table>...</table>
```

#### Tabellen-Zellen (Daten)

Der kleinste Teil einer Tabelle ist eine Zelle. Sie wird mit dem `<td>`-Tag ('table data') erstellt:

```markup
<table>
    <td>Name</td>
    <td>Alter</td>
    <td>Petra</td>
    <td>15</td>
    <td>Marion</td>
    <td>18</td>
    <td>Martin</td>
    <td>17</td>
</table>
```

Wenn du den Code z.B. mit [Codepen](https://codepen.io/pen/) testest, wirst du feststellen, dass die einzelnen Reihen nicht untereinander, sondern alle in einer Reihe sind:&#x20;

<table data-header-hidden><thead><tr><th width="90"></th><th width="90"></th><th width="90"></th><th width="90"></th><th width="90"></th><th width="90"></th><th width="90"></th><th width="90"></th></tr></thead><tbody><tr><td>Name</td><td>Alter</td><td>Petra</td><td>15</td><td>Marion</td><td>18</td><td>Martin</td><td>17</td></tr></tbody></table>

#### Tabellen-Zeilen (Rows)

Um die Zellen in Reihe zu unterteilen, nutzen wir das `<tr>`-Tag ('table row'):

```markup
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
        <td>Martin</td>
        <td>17</td>
    </tr>
</table>
```

#### Spalten-Überschriften (Headings)

Die erste Reihe eine Tabelle enthält oft keine Daten, sondern die Spaltenüberschriften. Dafür ist das `<th>`-Tag vorgesehen ('th' steht für 'Table Heading'):

```markup
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
        <td>Martin</td>
        <td>17</td>
    </tr>
</table>
```

<table><thead><tr><th width="120">Name</th><th width="120">Alter</th></tr></thead><tbody><tr><td>Petra</td><td>15</td></tr><tr><td>Marion</td><td>18</td></tr><tr><td>Martin</td><td>17</td></tr></tbody></table>
