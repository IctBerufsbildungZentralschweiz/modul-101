# Container Queries

Contanier Queries sind relativ neu (seit 2023 gut unterstützt) und ähnlich wie Media Queries.&#x20;

Während Media Queries sich auf die Fensterbreite bezieht, fragen Container Queries die Breite des beinhaltenden Containers ab.

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

Es gibt anonyme Container:

```css
/* Anonymen Container deklarieren */
nav {
  container-type: inline-size;
}
/* Default: Mobile first = Vertikale Anordnung */
nav ul {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
/* Container query */
@container (width >= 800px) {
  /* Desktop: Horizontale Anordnung */
  nav ul {
    flex-direction: row;
  }
}
```

Container sollten einen Namen haben, falls es mehrere verschachtelte gibt:

```css
/* Benannter Container deklarieren */
nav {
  container-type: inline-size;
  container-name: navigation; /* Beliebiger Name */
  /* Oder in 1 Zeile: */
  container: navigation / inline-size;
}
/* Default: Mobile first = Vertikale Anordnung */
nav ul {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
/* Container mit Namen */
@container navigation (width >= 800px) {
  nav ul {
    flex-direction: row;
  }
}
```

## 🛠️ Aufgabe

Wende die Container Queries auf deine Navigation der Aufgabe "Navigation" an:&#x20;

* "Mobile first" heisst, dass die Standard-Anordnung der Menülinks vertikal (übereinander) ist.&#x20;
* Entscheide, ab welcher Containerbreite auf horizontale Anordnung umgeschaltet werden soll.&#x20;
