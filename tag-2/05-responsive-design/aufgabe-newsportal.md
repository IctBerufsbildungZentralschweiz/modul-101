# 🛠️ Aufgabe Newsportal

Die Aufgabendateien findest in der Datei «newsportal.zip». Lade die Datei herunter und entpacke das Zip-Archiv.&#x20;

{% file src="../../.gitbook/assets/newsportal.zip" %}
Download Aufgabendateien
{% endfile %}

## Aufgabe 1

Lade die HTML- und CSS-Dateien `index.html`, `style.css` und `flex.css` herunter. Ergänze die Datei `flex.css` nun mit den nötigen CSS-Regeln, damit folgendes Layout angezeigt wird:

### Bildschirmbreite: 1300px

![Order](../../.gitbook/assets/news-1.png)

Dabei dürfen die anderen Dateien `index.html` und `style.css` **nicht verändert werden**.

## Aufgabe 2

Die CSS-Regeln innerhalb der geschweiften Klammern der folgenden `@media`-Eigenschaft werden nur interpretiert, wenn die Breite des Bildschirms kleiner als 768px ist - sprich auf Tablets und Smartphones

```css
@media screen and (max-width: 768px) {
    /* Wird nur interpretiert, wenn der 
    Bildschirm weniger breit als 768px ist. */
}
```

Ergänze nun CSS-Regeln in den geschweiften Klammern, damit das Layout wie folgt auf dem Tablet angezeigt wird, ohne dass sich die Anzeige auf grösseren Bildschirmen ändert:

### Bildschirmbreite: kleiner als 768px

![Order](../../.gitbook/assets/news-2.jpg)

## Aufgabe 3

Die CSS-Regeln innerhalb der geschweiften Klammern der folgenden `@media`-Eigenschaft werden nur interpretiert, wenn die Breite des Bildschirms kleiner als 480px ist.

```css
@media screen and (max-width: 480px) {
    /* Wird nur interpretiert, wenn der 
    Bildschirm weniger breit als 480px ist. */
}
```

Ergänze nun CSS-Regeln in den geschweiften Klammern, damit das Layout wie folgt auf dem Smartphone angezeigt wird, ohne dass sich die Anzeige auf grösseren Bildschirmen ändert:

### Bildschirmbreite: kleiner als 480px

![Order](../../.gitbook/assets/news-3.jpg)
