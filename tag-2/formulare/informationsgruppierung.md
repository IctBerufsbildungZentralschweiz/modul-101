# Informationsgruppierung

Die Übertragung von Informationen mit Hilfe eines Formularfeldes folgt klaren Regeln und Strukturen. Somit lassen sich Formularelemente grundsätzlich in drei hierarchische Stufen unterteilen:

1. Formularfelder (Textfeld, Checkbox, Radio-Box...)
2. Formularfeld-Gruppe (Fieldset)
3. Formular

## Formularfeld

Die Formularfelder sind die kleinsten Elemente innerhalb eines Formulars. Die verschiedenen Typen ermöglichen es dem Benutzer Informationen einzugeben (Textfelder, Checkboxen...) und/oder definierte Aktionen des Formulars auszulösen (Submit, Reset).

```markup
<label for="firstname">Vorname</label>
<input type="text" id="firstname" name="firstname">

<label for="lastname">Nachname</label>
<input type="text" id="lastname" name="lastname">

<label for="work">Beruf</label>
<input type="text" id="work" name="work">

<label for="workplace">Arbeitgeber</label>
<input type="text" id="workplace" name="workplace">
```

Als kleine Illustration:

![Formularfelder](../../.gitbook/assets/Formularfelder.jpg)

Zur Repetition befindet sich unter folgendem Link ein kleines Cheatsheet zum Thema Formularfelder:

[Übersicht der Formularfelder](https://offline.ch/ict/formulare.html)

## Formularfeld-Gruppen

Das Tag `fieldset` ermöglicht es dem Benutzer die Formularfelder in Sets/Gruppen zu strukturieren. Ausschlaggebend für die Unterteilung ist die thematische Zusammengehörigkeit der einzelnen Felder.

Die Formularfeld-Gruppen erleichtern zum einen die Navigation innerhalb des Dokuments und erhöhen gleichzeitig die Accessability der Seite.

```markup
<fieldset>

    <legend>Informationen zur Person</legend>

    <label for="firstname">Vorname</label>
    <input type="text" id="firstname" name="firstname">

    <label for="lastname">Nachname</label>
    <input type="text" id="lastname" name="lastname">

</fieldset>

<fieldset>

    <legend>Informationen zum Beruf</legend>

    <label for="work">Beruf</label>
    <input type="text" id="work" name="work">

    <label for="workplace">Arbeitgeber</label>
    <input type="text" id="workplace" name="workplace">

</fieldset>
```

Als kleine Illustration:

![Formularfelder](../../.gitbook/assets/Fieldset.jpg)

Accessability/Barrierefreiheit: Kommunikation in der Weise, dass sie von Menschen mit Behinderung und von älteren Menschen in derselben Weise genutzt werden kann, wie von Menschen ohne Behinderung.

## Formular

Das `form` Tag ist auf der höchsten strukturellen Ebene eines Formulars und beinhaltet sämtliche Formularfelder und Formularfeld-Gruppen. Ein Formularfeld zeigt folgende Charakteristiken:

* Das `form` Tag verfügt über kein Aussehen. Das Aussehen wird von den darin enthaltenen Elementen bestimmt.
* Das `form` Tag definiert die Handhabung eines kompletten und abgesendeten Formulars (mit Hilfe des `action` Attributs).
* Das `form` Tag definiert die Methode, mit welcher die Daten versendet werden.

```markup
<form action="http://ict-bz.ch/process.php" method="post">

    <fieldset>

        <legend>Informationen zur Person</legend>

        <label for="firstname">Vorname</label>
        <input type="text" id="firstname" name="firstname">

        <label for="lastname">Nachname</label>
        <input type="text" id="lastname" name="lastname">

    </fieldset>

    <fieldset>

        <legend>Informationen zum Beruf</legend>

        <label for="work">Beruf</label>
        <input type="text" id="work" name="work">

        <label for="workplace">Arbeitgeber</label>
        <input type="text" id="workplace" name="workplace">

    </fieldset>

    <button type="submit" name="form-submit">Anmeldung einreichen</button>

</form>
```

Als kleine Illustration:

![Formularfelder](../../.gitbook/assets/Form.jpg)
