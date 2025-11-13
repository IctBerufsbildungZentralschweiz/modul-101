# Medien: Videos, Audio

## Videos

### Eigene Videodateien einbinden

HTML5 bietet für die Integration das `<video>`-Element. Dazu musst du dein Video in ein Format konvertieren, welches möglichst von allen Browsern unterstützt wird. Es empfiehlt sich mp4 oder seit 2024 auch WebM. Videos kannst du z.B. mit dem [VLC-Player](https://www.videolan.org/) konvertieren oder einen [Online-Konverter](https://www.google.com/search?q=Video+online+konvertieren) nutzen.&#x20;

Du kannst alternative Formate angeben für Browser, welche dein bevorzugtes Format nicht kennen, plus einen Text, falls ein Browser gar nichts versteht:

```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
```

**Vorteile:**&#x20;

* Du bist unabhängig von externen Plattformen
* Besserer Datenschutz

**Nachteile:**&#x20;

* Videos brauchen viel Platz auf deinem Server&#x20;
* Du musst dich selber um Browser-Kompatibilität kümmern, ev. mehrere Versionen hochladen

### Externe Videos von einbinden

Viele Plattformen wie Youtube, Vimeo etc. bieten fertigen Code an, um ein Video einzubetten:&#x20;

* **Youtube, Vimeo, Dailymotion:** Klicke auf "Teilen > Einbetten", wähle die gewünschten Optionen und kopiere den Coode in deine Website.
* **Instagram:** Hat leider keine direkte Embed-Funktion, man braucht etwas JavaScript, um einen Post in die eigene Website zu integrieren.

**Vorteile:**&#x20;

* Das Video belegt keinen Platz auf deinem Server und wird performant ausgeliefert
* Du musst dich nicht um Browser-Kompatibilität kümmern

**Nachteile:**&#x20;

* Ein Video muss erst auf einer anderen Plattform veräffentlich werden
* Der Datenschutz ist meist deutlisch schlechter

### Responsive Videos - Grösse  anpassen

**Wie passe ich ein eingebettetes Video an mein Layout an?**&#x20;

Der Embed-Code von Youtube & Vimeo enthält eine fixe Grösse in Pixeln. Im folgenden Video siehst du, wie du das an deinen vorhandenen Platz im Layout anpassen und responsive machen kannst:&#x20;

{% embed url="https://www.youtube.com/watch?v=2h9CqRlHzrc" %}

## Audio

Ähnlich die bei Videos kannst  ein Audio-Beitrag selber gehostet oder von einer Plattform eingebunden werden. Die Vor- & Nachteile sind analog der Videos.&#x20;

### Eigene Audiodatei einbinden

Audio-Formate kannst du ebenfalls mit dem [VLC-Player](https://www.videolan.org/) konvertieren oder mit einem [Online-Dienst](https://www.google.com/search?q=Audio+online+konvertieren).

Folgendes Beispiel spielt einen Beitrag direkt beim Laden der Seite ab, aber erst mal "gemutet" (still):&#x20;

```
<audio controls autoplay muted>
  <source src="podcast-episode-1.ogg" type="audio/ogg">
  <source src="podcast-episode-1.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

### Externen Audiobeitrag einbetten

* Vimeo: [https://help.soundcloud.com/hc/en-us/articles/115003453587-Embedded-players](https://help.soundcloud.com/hc/en-us/articles/115003453587-Embedded-players)
* Spotify: [https://developer.spotify.com/documentation/embeds/tutorials/creating-an-embed](https://developer.spotify.com/documentation/embeds/tutorials/creating-an-embed)

## **🛠️** Aufgabe

Ergänze die HTML-Datei `media.html` au den Bilder-Aufgaben: &#x20;

1. Erstelle darin ein `<main>`-Element mit einer Überschrift 1 und drei `<article>`-Elementen. Diese Elemente sollen jeweils eine Überschrift 2 enthalten ("Bilder", "Videos", "Audios").&#x20;
2. Probiere darin die beschriebenen Medien-Elemente aus:&#x20;
   * Externes Video
   * Externer Audiobeitrag
   * Video responsive an Layout & Bildschirmgrösse anpassen
3. Zusatzaufgaben für schnelle Lernende:&#x20;
   * Eigenes Video: Z.B. mit Handy filmen oder herunterladen, Format konvertieren, einbetten
   * Eigenes Audio-Element
