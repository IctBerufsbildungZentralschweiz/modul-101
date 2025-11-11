# CSS-Variablen

Seit 2020 wird ein neues Feature von fast allen Browsern unterstützt, welches bisher nur mit Frameworks und CSS-Kompilern möglich war: CSS-Variablen.

## Einheitliche Gestaltung von Elemente

In einem [Styleguide](../../tag-3/konzeptionierung.md#styleguide) werden für eine Website üblicherweise 2-3 einheitliche Fonts und ein Farbkonzept mit 4-8 einheitlichen Farben definiert. Diese werden in der Website für verschiedene Elemente genutzt, z.B. Überschriften, Navigation, Buttons, Links etc. Um das Layout einheitlich und leicht anpassbar zu halten, sollten für solche Definitionen Variablen genutzt werden:&#x20;

**Früher (mühsam zu ändern):**

```css
/* Wenn eine Farbe oder ein Font verändert werden soll, muss dies  *
 * über alle Zeilen und ev. mehrere CSS-Dateien gemacht werden:    */
body { 
  color: #333333; 
  font-family: Arial, sans-serif; 
}
header { 
  color: #4a69c7; 
  background-color: #ffeab0;
  height: 80px;
}
h1, h2 { 
  color: #4a69c7; 
  font-family: Roboto, Verdana, sans-serif; 
}
button { 
  background-color: #ffeab0; 
  font-family: Roboto, Verdana, sans-serif; 
}
a { 
  color: #4a69c7;
  text-decoration: none;
}
a:hover { 
  color: #333333;
  text-decoration: underline;
}
```

&#x20;**Mit CSS-Variablen:**

```
/* Wenn eine Farbe oder ein Font verändert werden soll,  *
 * kann dies hier einmal zentral gemacht werden:         */
:root {
  --color-text: #333333;
  --color-primary: #4a69c7;
  --color-background: #ffeab0;
  --font-default: Arial, sans-serif;
  --font-alternative: Roboto, Verdana, sans-serif;
}
body { 
  color: var(--color-text); 
  font-family: var(--font-default);
}
header { 
  color: var(--color-primary); 
  background-color: var(--color-background); 
  height: 80px; 
}
h1, h2 { 
  color: var(--color-primary); 
  font-family: var(--font-alternative);
}
button { 
  background-color: var(--color-background); 
  font-family: var(--font-alternative);
}
a { 
  color: var(--color-primary); 
  text-decoration: none;
}
a:hover { 
  color: var(--color-text);
  text-decoration: underline;
}
```

