# Formulare

Unter [w3schools.com/html/html\_forms.asp](https://www.w3schools.com/html/html_forms.asp) findest du eine Übersicht wichtiger Elemente von Formularen und die Möglichkeit, es selber auszuprobieren. Nutze auch "Next >" oben rechts.

## Steuerelemente

In HTML werden die meisten Formularfelder mit dem `input` Tag deklariert. Mit dem `type` Attribut können verschiedene Typen spezifiziert werden.&#x20;

**Jedes Feld muss zwingend ein `name` Attribut haben**, sonst wird das Feld beim Versenden nicht mitgeschickt.

Unter W3School.com findest du alle [Input-Typen](https://www.w3schools.com/html/html_form_input_types.asp) mit Beispielen.&#x20;

```markup
<input type="text" name="address">
<input type="email" name="mail">
<input type="checkbox" id="coffee" name="coffee"><label for="coffee">Kaffee</label>
```

Zusätzlich zu einfachen Text-Inputs gibt es noch mehrzeilige Textfelder (`textarea`), Dropdowns (`select`, `option`) und Schaltflächen (`buttons`).

Unter W3School.com findest du zudem die [Form-Elemente](https://www.w3schools.com/html/html_form_elements.asp) mit Beispielen.&#x20;

```markup
<textarea name="remarks" rows="10" cols="4"></textarea>

<select name="anrede">
    <option value="Frau">Frau</option>
    <option value="Herr">Herr</option>
</select>

<button type="submit" name="submit">Formular absenden</button>
```

## Labels vs. Placeholder

### Labels

Ein alleinstehendes, unbeschriftetes Inputfeld ist für den Besucher nicht brauchbar. Was muss er darin eintragen? Um den Feldern einen Beschreibungstext zu geben, können wir das `label` Tag verwenden.

```markup
<label for="name-field">Ihr Name</label>
<input type="text" name="name" id="name-field">
```

Das `for` Attribut im Label verweist auf die `id` des Input-Elements. \
Bei einem Klick auf das Label wird somit der Cursor automatisch ins zugehörige Feld platziert wird.

Diese Zuordnung ist zudem für Screenreader wichtig, da er nur so weiss, welches Label vorgelesen werden soll, wenn der Cursor ins Feld platziert wird.

### Placeholder

Alternatif kann innerhalb des Feldes ein Placeholder eingefügt werden. Dieser verschwindet, sobald etwas ins Feld geschrieben wird.&#x20;

* **Vorteil:** Das Formular ist kompakter als mit Labels&#x20;
* **Nachteil:** Dann ist die Feldbezeichnung also nicht mehr sichtbar.&#x20;

```html
<input type="email" name="mail" placeholder="E-Mail-Adresse">
```

## Form-Tag

Alle Elemente müssen in einem `form` Tag gruppiert werden.

```markup
<form action="ziel.php" method="post">
    <label for="feld1">Bezeichnung</label>
    <input name="feld" type="text" id="feld1">
</form>
```

Beim Absenden eines Formulars werden die Daten aller Elemente innerhalb des `form` Tags mit der definierten `method` an die in `action` definierte URL versendet.

In diesem Kurs kann zum Testen das Ziel [https://formlog.ict-bz.ch/](https://formlog.ict-bz.ch/) verwendet werden. Deine Daten werden dort 7 Tage gespeichert und danach gelöscht. \
**Wichtig:** Dieser Server fordert die Methode "post" im `<form>`-Element, "get" funktioniert nicht.

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
