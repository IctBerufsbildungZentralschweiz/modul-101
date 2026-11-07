# Container Queries

Während Media Queries sich auf die Fensterbreite bezieht, fragen Container Queries die Breite des beinhaltenden Containers ab.

{% hint style="info" %}
**Achtung neues Feature:** Container Queries werden von den meisten Desktop-Browsern seit 2023 unterstützt, von Android-Browsern jedoch erst seit Okt./Nov. 2026. ⇒ Noch zurückhaltend verwenden!

Siehe [caniuse.com](https://caniuse.com/?search=%40container)
{% endhint %}

## Deklaration

Nehmen wir eine Navigation an:

```html
<nav>
  <ul>
    <li><a href="page-1.html">Menu 1</a></li>
    <li><a href="page-2.html">Menu 2</a></li>
    <li><a href="page-3.html">Menu 3</a></li>
  </ul>
</nav>
```

```css
/* Default: Mobile first = Vertikale Anordnung */
nav ul {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
```

### Anonyme Container ohne Verschachtelung

Anonyme Container reichen in den meisten Fällen:&#x20;

```css
/* Anonymen Container deklarieren */
nav {
  container-type: inline-size;
}
/* Container query ohne Namen */
@container (width >= 800px) {
  /* Desktop: Horizontale Anordnung */
  nav ul {
    flex-direction: row;
  }
}
```

### Container mit Namen für Verschachtelung

Container sollten einen Namen haben, falls es mehrere verschachtelte Container Queries gibt:

```css
/* Benannter Container deklarieren */
nav {
  container-type: inline-size;
  container-name: navigation; /* Beliebiger Name */
  /* Oder zusammengefasst in 1 Zeile: */
  container: navigation / inline-size;
}
/* Container mit Namen ansprechen */
@container navigation (width >= 800px) {
  nav ul {
    flex-direction: row;
  }
}
```

## 🛠️ Aufgabe

Wende die Container Queries auf die Newsportal-Aufgabe an, wenn du sie gemacht hast, sonst auf die Navigations-Aufgabe:&#x20;

* Aufgabe Newsportal: Ab wann haben die Überschriften in den NEws-Artikeln nicht mehr Platz auf 1 Zeile? Passe die Fontgrösse für Überschrift für kleine Container an.
* Aufgabe Navigation: Mache die Schrift generell etwas grösser und füge in der Navigation etwas längere Texte (mind. 20 Zeichen) ein. Schau dann, ab welcher Container-Breite die Menü-Optionen nicht mehr auf 1 Zeile platz haben und verkleinere dann die Schriftgrösse.
