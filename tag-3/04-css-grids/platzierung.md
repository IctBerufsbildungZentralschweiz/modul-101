# CSS Grid Layouts & Platzierung

## Arten von Grid-Layouts und Platzierung von Elementen

Es gibt zwei verbreitete Arten, Seitenelemente in einem Grid-Layout anzuordnen:&#x20;

* [**Layout mit benannten Grid Areas (Named Grid Areas)**](platzierung.md#layout-mit-benannten-grid-areas-named-grid-areas)\
  ![](../../.gitbook/assets/named-grid-areas.png)
* [**Layout mit Grid-Linien (Grid Line Placement)**](platzierung.md#layout-mit-grid-linien-grid-line-placement)\
  ![](../../.gitbook/assets/grid-line-placement.png)

Die Arten lassen sich auch kombinieren, z.B. kann das Grundlayout mit Named Grid Areas erstellt sein, im Content (`<main>)`  kann ein Linien-Grid.&#x20;

### Links dazu

* [https://raidboxes.io/blog/webdesign-development/css-grid-layout/](https://raidboxes.io/blog/webdesign-development/css-grid-layout/)
* [https://kulturbanause.de/blog/css-grid-layout-module/](https://kulturbanause.de/blog/css-grid-layout-module/)
* [https://gridbyexample.com/examples/](https://gridbyexample.com/examples/)

### 🛠️ Aufgabe

Untersuche folgende 3 Websites und finde heraus, wo / wie sie Grids nutzen:&#x20;

1. [www.theguardian.com/europe](https://www.theguardian.com/europe)
2. [www.vaude.com](https://www.vaude.com/)
3. [www.berufsberatung.ch/de/berufe/mediamatiker-in-efz](https://www.berufsberatung.ch/de/berufe/mediamatiker-in-efz)

## Layout mit benannten Grid Areas (Named Grid Areas)

Elemente können in einem Grid in Bereichen (areas) platziert werden.&#x20;

### Container: `grid-template-areas`

Mit `grid-template-areas` können bestimmten Bereichen im Grid spezifische Namen vergeben werden.&#x20;

![Container](<../../.gitbook/assets/code-example-3 (1).png>)

In unserem Beispiel gibt es vier Areas: `header`, `social`, `content` und `sidebar`. Die Namen dieser Areas kannst du frei wählen, sie sollten aus Kleinbuchstaben bestehen.

Das Grid wird mit `grid-template-areas` aufgeteilt. Für jede Zeile muss eine Definition erstellt werden. Jede Spalte muss einen Namen erhalten. Spalten und Zeilen mit gleichem Namen gelten als `Area`.

```css
.container {
    display: grid;
    grid-template-columns: 80px auto 260px;
    grid-template-rows:   120px auto;

    /** 
     * Die Kommentare sind nur zur besseren Veranschaulichung
     * der Struktur vorhanden und werden zur eigentlichen
     * Definition natürlich nicht benötigt.
     */
    grid-template-areas: 
         /* S1 */  /* S2 */
        "header    header "   /* Zeile 1 */
        "navi      navi   "   /* Zeile 2 */ 
        "content   sidebar"   /* Zeile 2 */ 
        "footer    footer "   /* Zeile 3 */ 
    ;
}
```

### Items: `grid-area`

Elemente im Grid lassen sich jetzt ganz einfach mit `grid-area` platzieren.

```markup
<div class="container">
  <header>Header</header>
  <main>Content</main>
  <aside>Sidebar</aside>
  <div class="social">Social Media Icons</div>
</div>
```

```css
header  { grid-area: header;  }
main    { grid-area: content; }
aside   { grid-area: sidebar; }
.social { grid-area: social;  }
```

Siehe [https://codepen.io/anon/pen/ooZVoG](https://codepen.io/anon/pen/ooZVoG).

## Layout mit Grid-Linien (Grid Line Placement)

... in Arbeit ...

## Unterstützung in den Browser-DevTools (F12)

In den Entwicklertools findest du unter `Inspect -> Layout` (Firefox) bzw. `Elements -> Layout` (Chrome) den Grid Inspector, der dir beim Arbeiten mit Grids helfen kann:

![Grid Inspector in Firefox](<../../.gitbook/assets/dev-tools-setting (1).png>) ![Container](<../../.gitbook/assets/dev-tools (1).png>)

<figure><img src="../../.gitbook/assets/ChromeDevToolsGrid.png" alt=""><figcaption><p>Grids und Flexboxen sind in Chrome leicht zu finden.</p></figcaption></figure>
