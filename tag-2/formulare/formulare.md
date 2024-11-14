# Formulare

Unter [w3schools.com/html/html\_forms.asp](https://www.w3schools.com/html/html\_forms.asp) findest du eine Übersicht wichtiger Elemente von Formularen und die Möglichkeit, es selber auszuprobieren. Nutze auch "[Next >](https://www.w3schools.com/html/html\_form\_elements.asp)" oben rechts.

Unter [offline.ch/ict/formulare.html](https://offline.ch/ict/formulare.html) findest du einige zusätzliche Code-Beispiele und Besonderheiten im Zusammenhang mit Formularen.&#x20;

## Steuerelemente

In HTML werden Formularfelder mit dem `input` Tag deklariert. Mit dem `type` Attribut können verschiedene Typen spezifiziert werden. **Jedes Feld muss zwingend ein `name` Attribut haben**, sonst wird das Feld beim Versenden nicht mitgeschickt.

```markup
<input type="text" name="address">
```

Zusätzlich zu einfachen Text-Inputs gibt es noch mehrzeilige Textfelder (`textarea`), Dropdowns (`select`, `option`) und Schaltflächen (`buttons`).

```markup
<textarea name="remarks" rows="10" cols="4"></textarea>

<select name="anrede">
    <option value="Frau">Frau</option>
    <option value="Herr">Herr</option>
</select>

<button type="submit" name="submit">Formular absenden</button>
```

Damit die Daten korrekt an den Server übermittelt werden, benötigt jedes Formularelement ein `name` Attribut.

```markup
<input type="text" name="username">
<input type="password" name="password">
```

## Labels

Ein alleinstehendes, unbeschriftetes Inputfeld ist für den Besucher nicht brauchbar. Was muss er darin eintragen?

Um den einzelnen Feldern einen Beschreibungstext zu geben, können wir das `label` Tag verwenden.

```markup
<label for="name-field">Ihr Name</label>
<input type="text" name="name" id="name-field">
```

Das `for` Attribut im Label verweist auf die `id` des Input-Elements.&#x20;

Bei einem Klick auf das Label wird somit der Cursor automatisch ins zugehörige Feld platziert wird.

Diese Zuordnung ist zudem für Screenreader wichtig, da er nur so weiss, welches Label vorgelesen werden soll, wenn der Cursor ins Feld platziert wird.

## Form-Tag

Alle Elemente müssen in einem `form` Tag gruppiert werden.

```markup
<form action="ziel.php" method="post">
    <label for="feld1">Bezeichnung</label>
    <input name="feld" type="text" id="feld1">
</form>
```

Beim Absenden eines Formulars werden die Daten aller Elemente innerhalb des `form` Tags mit der definierten `method` an die in `action` definierte URL versendet.

## Submit-Button

Mit einem `submit`-Button kann das Formular versendet werden. Bei einem Klick darauf wird der Versand der Formulardaten ausgelöst.

Es gibt zwei gültige Schreibwesen für einen Submit-Button:

```markup
<form action="ziel.php" method="post">

    <label for="feld1">Bezeichnung</label>
    <input name="feld" type="text" id="feld1">

    <input type="submit" name="submit" value="Formular absenden">
    <!-- oder -->
    <button type="submit" name="submit">Formular absenden</button>

</form>
```
