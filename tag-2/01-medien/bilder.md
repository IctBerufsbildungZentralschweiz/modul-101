# Bilder

## Aktivierungs-Fragen

Es sollen Bilder für eine Firmen-Website aufbereitet und eingefügt werden, welche Handys repariert. &#x20;

Recherchiere zu den gängigen Bildformaten und überlege, welche Formate für folgende Bilder geeignet sind (+), welche nicht (-), und warum:&#x20;

1. Oben soll ein zweifarbiges Logo eingefügt werden. Die Anzeigegrösse ist je nach Gerät anders.&#x20;
2. Auf der Teamseite sind Portraits aller Angestellten gewünscht.&#x20;
3. Auf der Seite "Statistik" soll ein Kuchen-Diagramm angezeigt werden mit den Anteilen der reparierten Marken. Je nach Display kann es grösser oder kleiner dargestellt sein.
4. Auf der Seite "Technik" soll das Innenleben eines Handys mit Zoom-Funktion gezeigt werden.&#x20;
5. Auf der Seite "Kontakt" soll ein animierter Briefkasten sein, wo ein Brief eingeworfen wird.

Weitere Fragen:&#x20;

1. Auf der Seite "Produkte" sollen Original-Bilder von Geräte-Herstellern eingefügt werden. Worauf ist dabei zu achten?&#x20;
2. Was sind Vor- und Nachteile, wenn du die Bilder in sehr hoher Qualität und Auflösung einfügst?&#x20;

## Bild-Formate

### JPEG

JPEG oder JPG ist ein verlustreiches Bildformat von der Joint Photographic Experts Group.

* Das JPG-Format verfügt über mehr mehrere Millionen Farben. Dies macht es zur idealen Wahl für die Anzeige von Fotografien im Web.
*   JPEG ist ein verlustreiches Bildformat. Die Kompression kann also dazu benutzt werden um die Dateigrösse zu reduzieren: Die Qualität bei einer Kompression von 60% ist meistens absolut ausreichend für das Web. Bei einem Kompressionsfaktor grösser als 75% kann es zu deutlichen Qualitätsverlusten kommen.

    ![JPG-Kompression](../../.gitbook/assets/compression.jpg)
* JPG-Bilder unterstützen keine Transparenz. Sollte ein Teil des Bildes somit transparent sein, eignet sich das JPG-Format nicht.

#### Anwendungsfall

Verwende JPEG für Fotos.

### GIF

GIF steht für Graphics Interchange Format.

*   Das GIF-Format verfügt nur über 256 Farben, dadurch ist die Dateigrösse meistens entsprechend klein.

    ![GIF-Kompression](../../.gitbook/assets/gif.jpg)
* Das GIF-Format ist ein verlustfreies Bildformat, sofern das Original max. 256 Farbtöne hat.
* Das GIF-Format unterstützt Transparenz - dabei gibt es jedoch keine Halbtransparenz (z. B. 50% weiss), sondern immer nur ganz oder garnicht.
* Das GIF-Format unterstützt Animationen - darum kann es gut eingesetzt werden für repetierende, animierte Bilder wie Icons, Emoticons, Banner etc.
* Eignet sich für einfache Grafiken mit wenig Farben, jedoch nicht für Fotografien.

![Loop](../../.gitbook/assets/loop.gif)

#### Anwendungsfall

Verwende GIFs für Animationen oder Bilder, die wenige Farben enthalten und als GIF eine kleinere Dateigrösse aufweisen als als PNG.

### PNG

PNG steht für Portable Network Graphics. Es ist eine alternative zum GIF-Format, welches vom W3C-Konsortium entwickelt wurde.

* Wie das JPEG, verfügt das PNG über Millionen von Farben.
* Wie das GIF, handelt es sich um einen verlustfreien Kompressionsalgorithmus.
* Das PNG-Format unterstützt Transparenz - dabei gibt es die Möglichkeit für teiltransparente Pixel (75% - transparent; 25% - weiss). Es eignet sich deshalb für Bilder mit unterschiedlichen Transparenzstufen.
* Es eignet sich daher für komplexe Bilder und Grafiken.

#### Anwendungsfall

Verwende PNGs nie für Fotos sondern nur für Illustrationen oder Icons. PNGs komprimieren Bilder mit grossen einfarbigen Flächen besonders gut.

### SVG

SVG steht für Scalable Vector Graphics und ist eine XML-basiertes Vektordatei. Obwohl es bereits 2001 entwickelt wurde, wurde das Format erst in den letzten Jahren populär für den Einsatz im Web. Der Grund dafür lag in der schwachen Unterstützung der Webbrowsern für dieses Format. In der Zwischenzeit wird das SVG-Format von den meisten Browsern unterstützt - leider immer noch mit einigen Bugs.

* Das SVG-Format ist weniger ein Bild aus Pixeln, als eine Bauanleitung für Vektoren um daraus ein Bild oder eine Grafik zu bauen. Es eignet sich deshalb vorallem für Grafiken wie Logos, Karten, Icons etc.
* Da es sich um ein Vektor-Format handelt, können die Bilder beliebig und ohne Qualitätseinbussen skaliert werden.
* SVG-Bilder unterstützen Animationen und können via CSS oder JavaScript animiert werden.
* Bei komplexeren Bildern steigt die Dateigrösse von SVG-Bilder rasant an. Darum eignet sich das Format mehr für Grafiken, als für Fotografien.

#### Anwendungsfall

Verwende SVGs dann, wenn ein Bild in verschiedenen Grössen benötigt wird oder eine geringere Dateigrösse als bei PNGs oder GIFs erreicht werden kann. Achte bei der Verwendung im Web auf den Browser-Support.

### WebP

Dieses Bildformat hat jedoch Web in seiner DNA: Es wurde für den Gebrauch im Internet (von Google) entwickelt.

> WebP is a modern **image format** that provides superior **lossless and lossy** compression for images on the web. … WebP lossless images are 26% smaller in size compared to PNGs. WebP lossy images are 25-34% smaller than comparable JPEG images … Lossless WebP supports **transparency** … at a cost of just 22% additional bytes. For cases when lossy RGB compression is acceptable, **lossy WebP also supports transparency**, typically providing 3× smaller file sizes compared to PNG. -- [WebP Website](https://developers.google.com/speed/webp/)

Der Vorteil von WebP ist also, dass es die Vorzüge von JPG und PNG in einem Bildformat kombiniert - ohne dabei auf eine überdimensionale Dateigrösse zu wachsen.

**ACHTUNG:** Leider ist der [Browsersupport](https://caniuse.com/?search=WebP) für das Format noch nicht flächendeckend gewährleistet, insbesondere bei Safari-Versionen vor Sept. 2022. Aus diesem Grund sollte WebP im Moment noch zurückhaltend eingesetzt werden.&#x20;

### **AVIF**

AVIF steht für **AV1 Image File Format** und ist ein modernes Bildformat, das auf dem **AV1-Videokompressionsstandard** basiert. Es wurde entwickelt, um eine noch höhere Effizienz als WebP und andere Bildformate wie JPEG oder PNG zu erreichen.

#### **Vorteile von AVIF:**

* **Hohe Kompressionseffizienz:** AVIF-Bilder bieten eine hervorragende Bildqualität bei wesentlich kleineren Dateigrößen im Vergleich zu JPEG, PNG oder WebP.
* **Unterstützung für HDR:** AVIF unterstützt **High Dynamic Range (HDR)**, was es ideal für Bilder mit hohem Kontrastumfang macht.
* **Transparenz:** Wie PNG und WebP unterstützt auch AVIF Transparenz, allerdings mit einer geringeren Dateigröße.
* **Farbtiefe:** AVIF unterstützt Farbtiefen von bis zu 12 Bit pro Kanal, wodurch es detailreichere und lebendigere Bilder ermöglicht als ältere Formate.

**Nachteile von AVIF:**

* **Rendering-Geschwindigkeit:** Die Codierung und Decodierung von AVIF-Bildern ist derzeit rechenintensiver als bei anderen Formaten, was zu längeren Ladezeiten führen kann.
* **Browser- und Software-Support:** Obwohl der Support für AVIF stetig zunimmt (u. a. in Chrome, Firefox und Edge), gibt es immer noch Einschränkungen, insbesondere bei älteren Browsern und Anwendungen.

#### **Anwendungsfall**

AVIF eignet sich hervorragend für Szenarien, in denen **maximale Bildqualität bei minimaler Dateigröße** gefragt ist, z. B. für Fotografien auf Websites, bei denen schnelle Ladezeiten entscheidend sind. Aufgrund der noch eingeschränkten Browser-Unterstützung sollte jedoch immer ein Fallback auf ein anderes Bildformat wie WebP oder JPEG implementiert werden.

**ACHTUNG:** AVIF ist relativ neu und wird noch nicht von allen Browsern unterstützt, insbesondere Browser-Versionen vor 2023/2024. Siehe [https://caniuse.com/avif](https://caniuse.com/avif)

### Links

* [Das perfekte Bildformat für Websites und Bilder-Sets für verschiedene Bildschirmgrössen](https://app-bis-web.de/perfektes-bildformat-websites/)

## Rechte an Bildern & Inhalten

> Alle Inhalte im Internet sind grundsätzlich urheberrechtlich geschützt und dürfen nicht öffentlich verbreitet werden. Das gilt für Musik, die zwar frei aus dem Web kopiert, aber nur im privaten Kreis ab­gespielt und weitergegeben werden darf, ebenso wie für Fotos: Als Desktop-Hintergrund, Schlafzimmerposter oder Illustra­tion in einer E-Mail an Freunde darf man jedes Bild verwenden. Auf einer öffentlich zugänglichen Homepage aber eben nicht.

\-- [Beobachter Konsum](https://www.beobachter.ch/konsum/webdesign-die-sache-mit-dem-copyright)

{% hint style="info" %}
cyon hat einen guten Artikel zu den Bildrechten: [https://www.cyon.ch/blog/Bilder-im-Internet-rechtssicher-verwenden](https://www.cyon.ch/blog/Bilder-im-Internet-rechtssicher-verwenden)
{% endhint %}

Somit sollten ein Website-Betreiber immer die nötigen Rechte für Bilder haben, welche auf seiner Website gezeigt werden. Mögliche Plattformen für den Erwerb von Bild-Lizenzen:

* [Fotolia](https://de.fotolia.com/)
* [Shutterstock](https://www.shutterstock.com)

Daneben gibt es auch noch komplett kostenlose Bildportale. Meistens sind die Aufnahmen von Amateur- und Hobbyfotografen, die aber deshalb nicht schlechter sein müssen:

* [Unsplash](https://unsplash.com)
* [Pixabay](https://pixabay.com/de/)
* [Pixelio](https://www.pixelio.de/)

## Ladegeschwindigkeit

Die zentrale Rolle der Ladegeschwindigkeit für eine Website zeigt folgendes Beispiel:

![Absprungrate](../../.gitbook/assets/every-second-count.png)

* Nach mehr als zwei Sekunden Ladezeit erhöht sich die Absprungrate (Personen, welche die Website verlassen) um 12%.
* Nach mehr als vier Sekunden Ladezeit erhöht sich die Absprungrate um 25%.

Mehr dazu auf [www.tooltester.com/de/blog/website-ladezeit-statistiken ](https://www.tooltester.com/de/blog/website-ladezeit-statistiken/)

Der Grund für lange Ladezeiten sind häufig schlecht verarbeitete Medien (Bilder, Videos). Durchschnittlich machen Bilder mehr als **65% des Inhaltes** einer Website aus.

![Aufteilung von Website Content](../../.gitbook/assets/chart.png)

### Geschwindigkeitstests

Um die Geschwindigkeit einer Website zu testen gibt es unterschiedliche Tools. Hier zwei davon:

* [Google-PageSpeed-Test](https://pagespeed.web.dev/)
* [WebPagetest](https://www.webpagetest.org/)

### Lazy-Loading

Werden auf einer Seite viele Bilder angezeigt, ein Teil ev. erst beim Scrollen, können diese erst bei Bedarf nachgeladen werden. So wird nicht die ganze Seiten-Ladezeit ausgebremst. Dazu gibt es das Attribut `loading="lazy"`:&#x20;

```html
<!-- Sofort geladene Bilder -->
<img src="/images/wedding.jpg" alt="Wedding">
<img src="/images/rocks.jpg" alt="Rocks">

<!-- Off-screen Bilder (beim Scrollen) -->
<img src="/images/nature.jpg" alt="Nature" loading="lazy">
<img src="/images/underwater.jpg" alt="Underwater" loading="lazy">
<img src="/images/ocean.jpg" alt="Ocean" loading="lazy">
```

## Bild-Grössen

Wichtig ist es nicht nur die Bilder im richtigen Bildformat bereitzustellen, sondern auch in einer angemessenen Grösse. **Bilder sollten immer in der Grösse bereitgestellt werden, in der sie tatsächlich im Web verwendet werden.**

Hier zwei nützliche Werkzeuge: \
Mit [Bulk Resize Photos](https://bulkresizephotos.com/) können mehrere Fotos miteinander verarbeitet werden.\
Mit dem [Online Image Editor](https://www.online-image-editor.com/) kannst du einzelne Bilder online skalieren und zuschneiden.

### Responsive Bildgrössen

Für unterschiedliche Geräte kannst du seit ... unterschiedliche Bildgrössen und Auflösungen anbieten.&#x20;

Dazu gibt es verschiedene Möglichkeiten. Eine empfehlenswerte ist das `<picture>`-Element:

```
<picture>
  <source media="(max-width: 799px)" srcset="person-480w-portrait.jpg">
  <source media="(min-width: 800px)" srcset="person-800w.jpg">
  <img src="person-800w.jpg">
</picture>
<!-- Seit 2023 kann man die neue Range Syntax benutzen: --> 
<picture>
  <source media="(width < 800px)" srcset="person-480w-portrait.jpg" />
  <source media="(width >= 800px)" srcset="person-800w.jpg" />
  <img src="person-800w.jpg" alt="Chris standing up holding his daughter Elva" />
</picture>
```

Das \<img>-Element wird genutzt, falls keine der gegebenen Media-Bedingungen zutrifft.
