# Zusammenarbeit

## Problemstellung: Gemeinsamer Code

Wenn ihr in einem kleinen Projekt zu zweit oder mehr arbeitet, habt ihr gemeinsamen Code, den ihr beide / alle ändern und testen wollt, ohne einander Arbeit zu überschreiben. Wie geht das?&#x20;

Es gibt diverse Tools dafür, kostenpflichtige, komplexe oder einfache:&#x20;

* In VS Code z.B. wird die Extension "**Live Share**" und zum Testen "Live Server" angeboten. Die beiden arbeiten leider nicht gut zusammen und "Live Share" macht oft Probleme.&#x20;
* Gemeinsame **Code-Verwaltung mit Git**: Ist der Standard für grössere Projekte, jedoch recht komplex und synchronisiert nicht sofort oder automatisch.&#x20;
* Dateien **hin und her kopieren**: Ist möglich, aber mühsam, und die Ordner-Struktur wird nicht automatisch korrekt übernommen.&#x20;
* **Empfehlung für dieses Modul:** \
  **OneDrive** plus eigener CSS-Datei plus gute Absprache.

## Workflow mit **OneDrive** plus eigener CSS-Datei

1. Erstellt das Projekt auf OneDrive und teilt es miteinander.&#x20;
2. Besprecht, wie ihr sicherstellt, dass nicht beide gleichzeitig an der gleichen Datei arbeiten.&#x20;
   * Erstellt zuerst zusammen ein `template.html`, welches eine HTML-Grundstruktur plus Header, Navigation, leeres Mail und Footer enthält. Kopiert dieses Datei dann für alle geplanten Seiten (index.html, unterseite-xy.html...).&#x20;
   * Bei HTML-Dateiein könnt ihr euch nun leicht absprechen, wer aktuell an welcher arbeitet und wer nicht.&#x20;
   * Bei einer zentralen CSS-Datei ist das schwieriger: SIe wird oft von beiden (fast) gleichzeitig bearbeitet. Eine Möglichkeit sind temporäre CSS-Dateien für weitere Team-Mitglieder:&#x20;
     1. Die 1. Person kann an der Haupt-Datei (z.B. `styles.css`) arbeiten, die 2. (oder 3.) Person erstellt für sich eine temporäre zusätzliche Datei (z.B. `temp-styles.css` oder `temp-mein-name.css`) und arbeitet darin.&#x20;
     2. In allen HTML-Dokumenten bindet ihr im `<head>` zuerst die `styles.css`, danach die `temp-styles.css` ein.&#x20;
     3. Immer wenn die 2. (oder 3.) Person etwas fertig hat, könnt ihr zusammen den Code aus `temp-styles.css` an sinnvolle Stellen in `styles.css` rein kopieren und dann aus `temp-styles.css` löschen.&#x20;
     4. Das `temp-styles.css` kann bei Projektabschluss gelöscht werden, wenn alles in die Haupt-CSS transferiert ist, danach die Links in den HTML-Dateien entfernt werden.&#x20;

## **🛠️** Aufgabe

Wähle ein Gegenüber und probiere diesen Workflow einmal aus:&#x20;

* Gemeinsames Projekt auf OneDrive.
* 2 HTML-Dateien mit Grundgerüst erstellen.
* 2 CSS-Dateien wie oben beschrieben erstellen und in den HTML-Dateien verlinken.
* Sprecht euch ab, wer in welcher Datei arbeitet und fügt ein paar Tags (HTML) und ein paar Regeln (CSS) ein. Testet dann im Browser und schaut, ob ihr auch die Änderungen der anderen Person in eurem Browser seht.&#x20;
* Kopiert die 2 CSS zusammen, löscht die temporäre Datei und entfernt den Link aus den HTML-Dateien.&#x20;
