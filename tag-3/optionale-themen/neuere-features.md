# Neuere Features

Ein paar bemerkenswerte Neuerungen der letzten Jahre, welche inzwischen von allen verbreiteten Browsern unterstützt werden, sind folgende:&#x20;

* [CSS-Nesting](neuere-features.md#css-nesting)
* [Preudo-Selektor `:has()`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Selectors/:has) - auch beschrieben auf [css-tricks.com/the-css-has-selector](https://css-tricks.com/the-css-has-selector/)
* [Container-Queries](../05-responsive-design/media-queries-1.md)
* [Media-Query Range Syntax](../05-responsive-design/media-queries.md#fensterbreite-media-query-range-syntax)
* [`backdrop-filter`](https://www.w3schools.com/cssref/css3_pr_backdrop-filter.php)  - siehe auch das [Demo auf W3Schools](https://www.w3schools.com/cssref/playdemo.php?filename=playcss_backdrop-filter)

## CSS-Nesting

### `@`-Regeln

Bereits bekannt ist das [Nesting bei `@`-Regeln](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Nesting/At-rules):

```css
.h1 {
  font-size: 30px;
}
@media screen and (max-width: 800px) {
  .h1 {
    font-size: 20px;
  }
}
```

Neu (seit 2024) geht dies auch umgekehrt:&#x20;

```css
.h1 {
  font-size: 30px;
  @media screen and (max-width: 800px) {
    font-size: 20px;
  }
}
```

Dies war vorher nur mit Precompilern (LESS, SASS) möglich.&#x20;

### Nesting und der Nesting Selektor `&`

Verschachtelte HTML-Elemente konnten bisher nur über Verkettung angesprochen werden:&#x20;

```css
body {
  color: black;
}
body .blog-post {
  color: darkgray;
}
body .blog-post a {
  color: red;
}
```

Seit 2024 können Selektoren auch berschachtelt werden. Auch dies war vorher nur mit Precompilern (LESS, SASS) möglich:&#x20;

```css
body {
  color: black;
  .blog-post {
    color: darkgray;
    a {
      color: red;
    }
  }
}
```

Der Nesting-Selektor & steht für alle übergeordneten Selektoren. Er ist oft freiwillig, bei Verkettung im gleichen Element jedoch erforderlich:&#x20;

```css
body {
  color: black;
  & .blog-post { /* Nesting-Selektor ist freiwillig */
    color: darkgray;
    & a { /* Nesting-Selektor ist freiwillig */
      color: red;
      &:hover { /* Nesting-Selektor ist erforderlich */
        text-decoration: underline;
      }
    }
  }
}
```

Dies wird vom Browser interpretiert wie folgendes:&#x20;

```css
body {
  color: black;
}
body .blog-post {
  color: darkgray;
}
body .blog-post a {
  color: red;
}
```

## Aufgabe neue Features

1. Suche selber nach ein paar weiteren Neuerungen, welche seit 1-2 Jahren von allen gängigen Browsern unterstützt werden. Schau dir dazu auch ein paar [Videos](https://youtube.com/watch?v=pGgy2QFhPtU) an.&#x20;
2. Schau auf [caniuse.com](https://caniuse.com/), wie die Browser-Unterstützung inzwischen ist.&#x20;
3. Teste 1-2 Features, welche du spannend findest.&#x20;
4. Optional: Zeige die Features der Gruppe.&#x20;



