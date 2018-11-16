# Formulare

Unter folgendem Link findest du einige Code-Beispiele und Besonderheiten im Zusammenhang mit Formularen:

[https://offline.swiss/vfi/formulare.html](https://offline.swiss/vfi/formulare.html)


## Steuerelemente

In HTML werden Formularfelder mit dem `input` Tag deklariert. Mit dem `type` Attribut können verschiedene Typen spezifiziert werden.

```html
<input type="text">
```

Zusätzlich zu einfachen Text-Inputs gibt es noch mehrzeilige Textfelder (`textarea`) und Schaltflächen (`buttons`).


```html
<textarea rows="10" cols="4"></textarea>

<button type="submit">Formular absenden</button>
```

Damit die Daten korrekt an den Server übermittelt werden, benötigt jedes Formularelement ein `name` Attribut.

```html
<input type="text" name="username">
<input type="password" name="password">
```

## Labels

Ein alleinstehendes Inputfeld ist für den Besucher nicht brauchbar. Was muss er darin eintragen?

Um den einzelnen Feldern einen Beschreibungstext zu geben, können wir das `label` Tag verwenden.

```html
<label>Ihr Name</label>
<input type="text" name="name">
```

Im obenstehenden Beispiel fehlt noch ein wichtiges Detail: Ausser, dass die beiden Elemente im Code nahe beisammen sind, gibt es keien Hinweis darauf, dass das Label unser `name` Feld beschreibt.

Um dieses Problem zu lösen, kann das `for` Attribut im Label verwendet werden, dass auf die `id` des Input-Elements verweist.

```html
<label for="name-field">Ihr Name</label>
<input type="text" name="name" id="name-field">
```

Diese Zuordnung ist besonders für Screenreader wichtig, da er nur so weiss, welches Label vorgelesen werden soll, wenn der Cursor ins Feld platziert wird.

Ein weiterer Bonus ist, dass bei einem Klick auf das Label der Cursor so automatisch ins zugehörige Feld platziert wird.

## Form-Tag

Alle einzelnen Elemente müssen in einem `form` Tag gruppiert werden.

```html
<form action="ziel.php" method="post">

    <label for="feld1">Bezeichnung</label>
    <input name="feld" type="text" id="feld1">

</form>
```

Beim Absenden eines Formulars werden die Daten aller Elemente innerhalb des `form` Tags mit der definierten `method` an die in `action` definierte URL versendet.

## Submit-Button

Ein Formular kann nur dann versendet werden, wenn es einen `submit`-Button beinhaltet. Bei einem Klick darauf wird der Versand der Formulardaten ausgelöst.

Es gibt zwei Schreibwesen für einen Submit-Button. Beide können verwendet werden.

```html
<form action="ziel.php" method="post">

    <label for="feld1">Bezeichnung</label>
    <input name="feld" type="text" id="feld1">

    <!-- ====================================== -->
    
    <input type="submit" value="Formular absenden">
    
    <!-- oder -->
    
    <button type="submit">Formular absenden</button>
    
    <!-- ====================================== -->

</form>
```