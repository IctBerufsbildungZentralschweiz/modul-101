# Spezielle Tags

## Bilder

Das `<img>`-Tag bettet ein Bild an der Stelle der Seite ein, wo es in der HTML-Struktur eingegliedert ist. Es tut dies mit dem `src` ('src' steht für 'source') Attribut, welches den Pfad zum gewünschen Bild beinhaltet.

```markup
<img src="images/mein-logo.png" alt="Mein Firmenlogo">
```

Das genauso wichtige Attribut ist das `alt`-Attribut. Diese Attribut muss immer vorhanden sein. Es darf jedoch explizit leer gelassen werden.

Der Text im `alt`-Attribut wird angezeigt, wenn das Bild nicht geladen werden kann. Dies ist nützlich für Sehbehinderte, für Suchmaschinen (können keine Bilder sehen) und wenn es einen Fehler beim Laden des Bildes gibt. Dieser alternative Satz sollte dem Leser eine Informationen geben, damit er sich vorstellen kann, was auf dem Bild angezeigt ist.

![Alt Tag eines \<img>](../../.gitbook/assets/img-alt.jpg)

## Überschriften

Mit Überschriftelementen können bestimmte Teile des Inhaltes als Überschrift deklariert werden. Wie ein Buch einen Hauptitel und Kapitelüberschriften haben kann, können HTML Dokumente eine Hauptüberschrift und weitere Überschriften haben.

HTML besitzt sechs Überschrifttypen, wobei meist nur 3-4 gebraucht werden: `<h1>–<h6>`

```markup
<h1>Ich bin eine Hauptüberschrift</h1>
<h2>Ich bin die höchste Unterüberschrift</h2>
<h3>Ich bin eine Unterüberschrift</h3>
<h4>Ich bin eine weitere Unterüberschrift</h4>
```

Jede Seite sollte genau eine Hauptüberschrift `<h1>` und beliebig viele Unterüberschriften `<h2>`-`<h6>` haben. Um eine logische Dokumentenstruktur zu erhalten, sollten keine Ebenen übersprungen werden (z. B. `<h3>` gefolgt von `<h5>`).

## Links

Links sind sehr wichtig. Sie sind, was das Internet zu einem **NETZ/WEB** macht. Um einen Link zu implementieren, müssen wir das `<a>`-Element verwenden. Das `a` ist die Kurzform für "Anker" (engl. "anchor"). Um einen Text innerhalb des Absatzes in einen Link zu verwandeln, führen wir folgende Schritte aus:

Zuerst schreiben wir einen Absatz mit einem Satz.

```markup
<p>Heute ist ein schöner Tag in Luzern.</p>
```

Nun wählen wir die Wörter aus, welche wir als Link definieren möchten und umschliessen diesen Bereich mit einem `<a>`-Tag.

<pre class="language-markup"><code class="lang-markup"><strong>&#x3C;p>Heute ist ein &#x3C;a>schöner Tag&#x3C;/a> in Luzern.&#x3C;/p>
</strong></code></pre>

Nun definieren wir mit dem `href`-Attribut, wo der Link hinzeigen soll.

```markup
<p>Heute ist ein <a href="https://luzerntourismus.roundshot.com/">schöner Tag</a> in Luzern.</p>
```

**Link in neuem Fenster / Tab öffnen:**

Wenn ein Link auf eine externe Website oder ein PDF verweist, ist es üblich, diese in einem neuen Tab oder neuen Fenster zu öffnen. Grund ist, dass das Ziel die bisherige Navigation nicht mehr anbietet und so die Besucher nicht mehr leicht zurück finden. Dazu gibt es das Attribut `target`:

```html
<p>Heute ist ein <a href="https://luzerntourismus.roundshot.com/" target="_blank">schöner Tag</a> in Luzern.</p>
```
