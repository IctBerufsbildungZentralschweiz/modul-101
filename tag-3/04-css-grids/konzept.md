# Konzept

## CSS Grids für Layouts

Das `CSS Grid Layout` dient dazu, Elemente zweidimensional anzuordnen, z.B. für ein gridbasierten Layout oder für komplexere Elemente innerhalb einer Seite.

Alternativ können einfache Layouts auch mit Flexbox erstellt werden, für komplexere Layouts sind aber Grids deutlich effizienter.&#x20;

Früher wurden auch Tabellen oder Floats für Layouts verwendet, selten siehst du sie noch in älteren Websites.

## Was ist ein Grid?

Das Grid ist ein Raster, an dem sich alle Elemente in einem Layout ausrichten.

### Container

Grundlage für jedes Grid ist der `Container`.

![Container](<../../.gitbook/assets/abstract-container (1).png>)

Der Container fixiert die Breite des Layouts. Die Höhe kann ebenfalls fixiert werden, wird aber üblicherweise flexibel gelassen.&#x20;

### Columns and Rows

Im Container werden beliebig viele Spalten (`Columns`) und Zeilen (`Rows`) definiert. Alle Inhaltselemente richten sich an diesem Raster aus.

![Cols](<../../.gitbook/assets/abstract-rows-cols (1).png>)

### Gaps

Zwischenräume zwischen `Columns` und `Rows` bezeichnet man als `Gaps`.

![Cols](<../../.gitbook/assets/abstract-gaps (1).png>)

## Beispiel: theguardian.com

### Container

![Container](<../../.gitbook/assets/guardian-container (1).png>)

### Columns

![Cols](<../../.gitbook/assets/guardian-cols (1).png>)

### Rows

![Rows](<../../.gitbook/assets/guardian-rows (1).png>)

### Grid

![Rows](<../../.gitbook/assets/guardian-grid (1).png>)
