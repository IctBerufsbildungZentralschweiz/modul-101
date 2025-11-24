# Schriftarten

## Wahl der Schriftarten

Welche Schriften ist wofür geeignet? Für gutes Webdesign gibt es eine einfache Regel:&#x20;

* **Logo:**\
  Ziel ist Unverwechselbarkeit und Wiedererkennung. Deshalb können für Logos auch ausgefallene Fonts benutzt werden.&#x20;
* **Überschriften:**\
  Überschriften sind kurz und dienen der Orientierung. Sie dürfen einen starken Charakter haben, brauchen einen guten Kontrast, sollen skalierbar sein (h1-h6) und sollen ev. auch fett gut aussehen.\
  Die Freiheit ist hier gross, auch ausgefallene Schriftwarten, Serifen-Schriften etc. sind möglich.&#x20;
* **Lauftext:**\
  Lauftexte sind Abschnitte, Sätze, der Hauptinhalt der Website. Wichtig sind leichte Lesbarkeit und guter Lesefluss. Deshalb sollten für Lauftext am Bildschirm schlichte, sehr gut lesbare Schriftarten gewählt werden, ohne Schnörkel und meist ohne Serifen.&#x20;

Binde nicht zu viele Schriftarten und Schriftstile ein. Das Layout wird sonst unruhig und die Ladezeit der Website kann stark beinflussen werden. Oft werden 2 Schriftarten gewählt: Eine für Überschriften und eine für Lauftext.&#x20;

## Schriftarten in CSS definieren

Um die Schriftart eines Elements zu ändern, wird die `font-family` Property verwendet. Die Verwendung von `"Anführungszeichen"` ist optional, wenn die Schriftart keine Leerzeichen im Namen hat:

```css
body {
    font-family: "Lucida Sans";
}
h1 {
    font-family: Calibri;
}
```

## Problem: Unterschiedliche Fonts je nach Gerät

Schriftarten werden **vom Computer des Besuchers** geladen. Je nach Betriebssystem und Software sind jedoch andere Schriftarten vorhanden. Calibri ist beispielsweise auf Windows installiert, auf Mac nicht. Das ergibt Darstellungsprobleme.

<div align="left"><img src="../../.gitbook/assets/calibri (1).png" alt="Fehlende Schriftart"></div>

## Lösung 1: Alternative Schriftarten definieren

Um dieses Problem zu umgehen können mehrere Schriftarten definiert werden.

Diese Definition bezeichnet man als `Font Stack`. Die erste Schriftart, die auf dem System des Besuchers installiert ist, wird verwendet.

```css
body {
    font-family: "San Francisco", "Calibri", "Arial", "Ubuntu";
    /*           ^ Für Mac        ^ für Windows       ^ für Linux */
}
```

Auf [cssfontstack.com](https://www.cssfontstack.com/) gibt es vordefinierte Font Stacks mit ähnlichen Schriftarten.

### Generische Schriftfamilie

Den Font Stack sollte man immer mit den generischen Schriftfamilien `serif`, `sans-serif` oder `monospace` abschliessen.

Wird auf dem System keine der definierten Schriftarten gefunden, wird die **Standard-Schriftart** für den definierten Schrifttyp gewählt. Welche Schriftart das genau ist, ist abhängig vom Betriebssystem, vom verwendeten Browser und von benutzerdefinierten Einstellungen des Besuchers.

```css
body {
    font-family: "Calibri", "San Francisco", "Arial", sans-serif;
}

.code-editor {
    font-family: "Source Sans Pro", "Roboto Mono", "Consolata", monospace;
}
```

## Lösung 2: Schriftarten einbinden

Seit CSS3 können auch eigene Schriftarten verwendet werden. Hier gilt es folgende Punkte zu beachten:

* Die Schriftart **muss auf einem Server** gehostet werden. Sie wird beim Aufruf einer Website heruntergeladen.
* Die Lizenz der Schriftart muss die Verwendung im Web zulassen.
* Die Einbindung einer eigenen Schriftart beeinflusst die **Ladezeit einer Website**, da mehr Daten heruntergeladen werden müssen.

### Woher bekomme ich eine Schriftart?

Es gibt viele Plattformen, welche Fonts anbieten. Ein paar Beispiele:&#x20;

* [Google Fonts](https://fonts.google.com/)
* [Adobe Fonts](https://fonts.adobe.com/)
* [Fontspace](https://www.fontspace.com/)
* [Fontshare](https://www.fontshare.com/pairs)

#### `@font-face`

Mit der `@font-face` Regel können eigene Schriftarten definiert werden:

```css
@font-face {
    font-family: "ICT-BZ Sans";
    src: url("./fonts/ict_bz_sans.otf");
}

body {
    font-family: "ICT-BZ Sans";
}
```

### **Beispiel: Google Web Fonts**

Auf [fonts.google.com](https://fonts.google.com/) befindet sich eine grosse Sammlung von Schriftarten, die uneingschränkt im Web verwendet werden können. Die Schriftarten werden von Google gehosted und können über eine einfache CSS-Datei eingebunden werden. Klicke auf [fonts.google.com](https://fonts.google.com/) auf "Get font" > "Get embed code".

```html
<link href="https://fonts.googleapis.com/css?family=Roboto:400,700" rel="stylesheet">
```

Eine spezielle Funktion von Google Fonts ist, dass überprüft wird, mit welchem Browser die Datei geladen wird und immer nur die Schriftformate (`woff2`, `ttf`, `otf`, etc.) in der CSS-Datei verwendet werden, die der Browser unterstützt.

Wird die CSS-Datei direkt aufgerufen, sehen wir die soeben besprochenen `@font-face` Regeln.

```css
/* Quellcode von https://fonts.googleapis.com/css?family=Roboto:400,700 */

@font-face {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 400;
  src: local('Roboto'), local('Roboto-Regular'), url(https://fonts.gstatic.com/s/roboto/v18/ek4gzZ-GeXAPcSbHtCeQI_esZW2xOQ-xsNqO47m55DA.woff2) format('woff2');
}
@font-face {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 700;
  src: local('Roboto Bold'), local('Roboto-Bold'), url(https://fonts.gstatic.com/s/roboto/v18/d-6IYplOFocCacKzxwXSOFtXRa8TVwTICgirnJhmVJw.woff2) format('woff2');
}

/* ... */
```

#### Problem: Datenschutz

**Achtung:** Gemäss eines Urteils des Landgerichts München von 2022 verstößt das Laden von Google Fonts direkt von Google-Servern ohne Einwilligung der User gegen die DSGVO (Europöische Datenschutz-Grundverordnung), weil eine Verbindung zu Google-Servern in den USA aufgebaut wird und die Server ohne Einwilligung diverse Daten des Besuchers abgreifen.&#x20;

#### Lösung: Google Fonts selber hosten

Dies kann gelöst werden, in dem die Fonts herunter geladen und auf einem eigenen Server gehostet werden. Wähle dazu auf [fonts.google.com](https://fonts.google.com/) "Get font" > "Download all". Entpacke den Font danach aus der Zip-Datei in dein Projekt - erstelle dazu einen Ordner "/fonts". Binde sie dann mit [@font-face()](01-schriftarten.md#font-face) ein.

