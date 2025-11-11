# Audio

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
