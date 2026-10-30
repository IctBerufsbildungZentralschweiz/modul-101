# 🛠️ Aufgabe Responsive Grid

![](../../../.gitbook/assets/ralph.png)

Style nun die Grid-Aufgabe für Tablets und mobile Geräte.&#x20;

## Responsives Layout

### Tablet

1. Sobald für die `1100px` des Containers kein Platz mehr auf dem Bildschirm ist, soll der Container immer `100%` breit sein.
2. Die Subnavigation soll nun horizontal direkt unter die Haupt-Navigation rutschen.
3. Content und Sidebar bleiben zweispaltig.

Nutze dafür folgendes Gerüst:&#x20;

```css
@media (width < 1100px) {
  .container {
    /* Hier kommt dein Code für Tablets (Breite, Grid etc.)... */
  }
}
```

### Handy

1. Ist das Fenster weniger als `600px` breit, sollen alle Elemente untereinander mit `100%` des Bildschirms angezeigt werden.
2. Die Punkte in der Hauptnavigation sollen nun vertikal gestapelt sein. Dafür braucht die Navigation nun im Grid etwas mehr Höhe.
3. Die Sidebar soll ausgeblendet werden. Nutze dazu die `display: none`-Eigenschaft in CSS.

```css
@media (width < 600px) {
  .container {
    /* Hier kommt das Grid für Mobiles... */
  }
  .main-nav {
    /* Elemente untereinander platzieren... */
  }
  aside {
    /* Sidebar verstecken... */
  }
}
```

