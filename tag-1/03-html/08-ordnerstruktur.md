# 📂 Ordnerstruktur

Bei kleineren Projekten ist es noch einfach ohne sinnvolle Ordnerstruktur den Überblick zu behalten. Werden die Projekte jedoch etwas grösser, verliert man schnell den Überblick:

![Ordnung](../../.gitbook/assets/mess.gif)

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

Bei der Ordnerstruktur gibt es kein richtig oder falsch, sondern nur ein übersichtlich und ein nicht-übersichtlich. Eine gute Methode dies zu überprüfen ist es, die Ordnerstruktur jemand anderem zu zeigen und zu schauen, wie schnell sich die Person zurechtfindet.

Eine mögliche Ordnerstruktur für die Dateien oben wäre beispielsweise:

```
root/
   |-> galerie.html
   |-> index.html
   |-> kontakt.html
   |-> ueber-uns.html
   img/
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
