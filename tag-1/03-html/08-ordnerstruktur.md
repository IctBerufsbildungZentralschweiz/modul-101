# 📂 Ordnerstruktur

Bei kleineren Projekten ist es noch einfach ohne sinnvolle Ordnerstruktur den Überblick zu behalten. Werden die Projekte jedoch etwas grösser, verliert man schnell den Überblick:

![Ordnung](<../../.gitbook/assets/mess (1).gif>)

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
   |-> style.css
   |-> zebras.jpg
```

Bei der Ordnerstruktur gibt es kein richtig oder falsch, sondern nur ein übersichtlich und ein nicht-übersichtlich. Eine mögliche Ordnerstruktur ist beispielsweise:

```
root/
   |-> galerie.html
   |-> index.html
   |-> kontakt.html
   |-> ueber-uns.html
   images/
      |-> affen.jpg
      |-> baeren.jpg
      |-> delfine.jpg
      |-> giraffen.jpg
      |-> header.jpg
      |-> zebras.jpg
   css/
      |-> framework.css
      |-> style.css
   docs/
      |-> dokument.pdf
```

**Hinweis:** \
**HTML-Dokumente** werden meist nicht in einem Unterordner platziert. Dies würde unschöne URLs ergeben (www.meine-domain.ch/html/home.html) und verkompliziert die Verlinkung von Bildern und CSS.

### Relative Pfade

Relative Pfaden haben das aktuelle Dokument als Ausgangspunkt für den angegebenen Pfad.

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

`../` - Zwei Punkte und ein Frontslash vermitteln, dass in die nächst höhere Ebene gegngen werden soll.

### Absolute Pfade

Absolute Pfade haben immer das Stammverzeichnis eines Servers (Root) als Ausgangspunkt für den angegebenen Pfad. Beispiel für absolute Pfade:

```html
<img src="/images/zebras.jpg" alt="Zebras"> <!-- Beachte den Slash "/" am Anfang -->
<!-- oder -->
<img src="https://www.example.com/images/zebras.jpg" alt="Zebras">
```

Werden Beziehungen zu externen Dateien (Frameworks, Schriften etc.) hergestellt, wird der Pfad meistens mit einem absoluten Pfad angegeben. Dabei sollte der Anbieter sicherstellen, dass sich der Pfad nicht ändert.&#x20;

### Probleme mit absoluten lokalen Pfaden

Falls lokale Links (zu Bildern, CSS etc.) nicht relativ, sondern absolut eingefügt wurden, werden diese nach dem Veröffentlichen nicht mehr funktionieren, weil der absolute Link auf dem Webserver nicht vorhanden ist:&#x20;

```html
<img src="C:\Users\Max\Projekte\Website\root\images\zebras.jpg" alt="Zebras">
```

**Nutze möglichst immer relative Pfade!**

```html
<img src="images/zebras.jpg" alt="Zebras">
```
