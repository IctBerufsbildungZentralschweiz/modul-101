# 🛠️ Aufgaben

## Schriftarten

Füge deiner Webseite `about-me.html` eine individuelle Schrift hinzu:&#x20;

1. Wähle eine Schrift von Google-Font aus und binde diese in die Seite ein. Ändere anschliessend die Standardschrift (`body`) per CSS auf die ausgewählte Schriftart.
2. Definiere eine alternative Schift, falls der Google-Font nicht oder langsam lädt.

**Zusatzaufgabe:**

* Datenschutz: Lade die Schriftart von Google herunter, speichere sie in einem neuen Ordner `/fonts` und binde sie von da ein, damit keine Verbingung zu Google mehr nötig ist.

## Farben

Nutze die [1. Flexbox-Aufgabe](broken-reference) für folgende Experimente:&#x20;

1. Untersuche **im Browser** die Quader in der Flexbox, wähle eine andere Farbe mit dem Farbmischer und kopiere den neuen Wert in dein CSS. Probiere die rgb(...)- und die #xxxxxx-Variante aus.
2. Mische eine Hintergrundfarbe für das ganze Dokument (`<body>`-Element) mittels der rgb()-Funktion.
3. Ändere die Transparenz der Quader in der Flexbox einmal mittels rgb()-Funktion und danach mittels #hex-wert, und schau, welche anderen Farbmodelle ev. noch Transparenz erlauben.&#x20;
4. Untersuche ein Flexbox-Element mit den Developer Tools im Browser und teste direkt in den DevTools das Farbmodell [LAB](02-farben.md#lab-cielab).

**Zusatzaufgabe:**

* Stelle mit einem Farbwähler eine Farbkombination von 5 Farben zusammen und wende sie sinnvoll auf deine Seite "Über mich" an. Du kannst dafür CSS-Variabeln nutzen, wenn du willst.

## Einheiten (optional)

1. Skaliere ein Bild in deiner Seite "Über mich" mit verschiedenen Einheiten: `px, %, vw`&#x20;
2. Füge ein breites Bild ein und mache das Fenster so schmal, bis das Bild nicht mehr Platz hat. Was passiert? Teste nun das gleiche, wenn du für das Bild `max-width: 100%` definierst.
3. Teste zusätzlich zu `width` die CSS-Eigenschaft `min-width: 50%` oder `max-width: 50%` an einem Element.

**Zusatzaufgabe:**

* Teste verschiedene Funktionen für einen Textblock oder ein Bild: `min(), max(), calc(), clamp()`&#x20;

## CSS-Variablen

Überarbeite dein bisheriges Stylesheet (CSS):&#x20;

1. Welche Werte nutzt du ev. mehrmals oder später noch noch für andere Elemente?&#x20;
2. Definiere für sie CSS-Variablen und setze sie in den Selektoren ein.
3. Überlege, wofür sie noch sinnvoll sind (z.B. Navigation, Buttons, Footer...) und wende sie da auch an.&#x20;
4. Falls du verschiedene Elemente mit runden Ecken hast, kannst du den Radius auch als Variable definieren.&#x20;

