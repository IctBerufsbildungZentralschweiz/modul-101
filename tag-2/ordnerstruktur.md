# Ordnerstruktur

Bei kleineren Projekten ist es noch einfach ohne sinnvolle Ordnerstruktur den Überblick zu behalten. Werden die Projekte jedoch etwas grösser, verliert man schnell den Überblick:

![Ordnung](../.gitbook/assets/mess.gif)

```
root/
   |-> affen.jpg
   |-> baeren.jpg
   |-> delfine.jpg
   |-> dokument.pdf
   |-> framework.css
   |-> galerie.html
   |-> giraffen.jpg
   |-> header.jpg
   |-> index.html
   |-> kontakt.html
   |-> ueber-uns.html
   |-> styles.css
   |-> zebras.jpg
   |-> ict_bz_sans.otf
```

Bei der Ordnerstruktur gibt es kein Richtig oder Falsch, aber einige "Best-Practices". Eine mögliche Ordnerstruktur ist beispielsweise:

```
root/
   |-> galerie.html
   |-> index.html
   |-> kontakt.html
   |-> ueber-uns.html
   css/
      |-> framework.css
      |-> styles.css
   docs/
      |-> dokument.pdf
   fonts/
      |-> ict_bz_sans.otf
   images/
      |-> affen.jpg
      |-> baeren.jpg
      |-> delfine.jpg
      |-> giraffen.jpg
      |-> header.jpg
      |-> zebras.jpg
```

**Tipps:**

Schreibe für Ordner- und Dateinamen nur Kleinbuchstaben, Zahlen, Minus (-), Bodenstrich (\_) und Punkte, KEINE Umlaute, Sonderzeichen oder Leerzeichen.&#x20;

Für **HTML-Dokumente** wird KEIN Unterordner `/html` genutzt. Dies ergibt unschöne URLs (www.beispiel.ch/html/home.html) und verkompliziert die Verlinkung von Bildern und CSS.

### Relative Pfade

Relative Pfade haben das aktuelle Dokument als Ausgangspunkt für den angegebenen Pfad.

Beziehungen von internen Dateien werden meistens mit einem relativen Pfad angegeben. So können die Dateien problemlos verschoben werden (beispielsweise von der Entwicklungsumgebung auf den Produktivserver).

```
root/
   tiere/
      |-> afrika.html
   images/
      |-> zebras.jpg
```

Beispiel für einen relativen Pfad in `tiere/afrika.html`:

```html
<img src="../images/zebras.jpg" alt="Zebras">
```

`../` - Zwei Punkte und ein Slash vermitteln, dass in die nächsthöhere Ebene gegangen werden soll.

### Absolute Pfade

Absolute Pfade haben immer das Stammverzeichnis eines Servers (Root) als Ausgangspunkt für den angegebenen Pfad. Beispiel für absolute Pfade:

```html
<img src="https://www.example.com/images/zebras.jpg" alt="Zebras">
<!-- oder -->
<img src="/images/zebras.jpg" alt="Zebras">
<!-- Beachte den Slash "/" am Anfang: Pfad startet nach dem Hostnamen, also nach https://www.example.com/, egal in welchem Unterordner die aktuelle Datei ist. -->
```

Werden Beziehungen zu externen Dateien (Frameworks, Schriften etc.) hergestellt, wird der Pfad mit einem absoluten Pfad angegeben. \
Dabei sollte der Anbieter sicherstellen, dass sich der Pfad nicht ändert.

### Probleme mit absoluten lokalen Pfaden

Falls lokale Links (zu Bildern, CSS etc.) nicht relativ, sondern absolut eingefügt wurden, werden diese nach dem Veröffentlichen nicht mehr funktionieren, weil der absolute Link auf dem Webserver nicht vorhanden ist:

```html
<img src="C:\Users\Max\Projekte\Website\root\images\zebras.jpg" alt="Zebras">
```

**Nutze möglichst immer relative Pfade!**

```html
<img src="images/zebras.jpg" alt="Zebras">
```

## 🛠️ Aufgabe

Erstelle in der aktuellen Aufgabe die Ordner /css, /fonts und /images, ev. weitere, und verschiebe CSS, Fonts und Bilder in diese Ordner. Passe dann die Pfade in der HTML-Datei an und teste.&#x20;

**Tipp:** Falls die Fonts nicht mehr gefunden werden, muss du zuerst aus dem CSS-Ordner raus und in den Font-Ordner rein: `../fonts/dein-font.otf` - Warum?&#x20;
