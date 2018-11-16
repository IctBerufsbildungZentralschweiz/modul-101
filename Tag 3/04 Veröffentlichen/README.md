# Veröffentlichen

Als `Veröffentlichung` oder `Deployment` einer Website bezeichnet man den Vorgang um den neusten Entwicklungsstand einer Website für die Öffentlichkeit zugänglich zu machen.

Methoden zur Veröffentlichung von Websites gibt es wie Sand am Meer: Von der einfachen manuellen Methode bis zum vollautomatischen Testing mit anschliessender Veröffentlichung auf mehrere Server gleichzeitig.

Im Prinzip sind alle Methoden gleich:

![Deployment](./src/schema.png)

* Der Code wird von der lokalen `Entwicklungsumgebung` auf einen `Webserver` geladen
* Die Entwicklungsumgebung ist deine Arbeitsstation
* Der Webserver ist `über das Internet zugänglich` und stellt Daten `24/7` bereit. Üblicherweise nimmst du dafür die Dienstleistungen eines `Hostinganbieters` in Anspruch, der diesen Webserver für dich betreibt und betreut
* Im Idealfall wird eine Source Code Verwaltung (wie z. B. [`git`](https://git-scm.com/)) dazwischen geschaltet
* Für unser Anwendungsfall genügt ein direktes und manuelles Veröffentlichen

## Transfer

Für den Transfer gibt es ebenfalls verschiedenste Methoden um den Quellcode auf den Server zu übertragen. 

Die meist verbreitete Methode für das manuelle Veröffentlichen ist der Upload via `FTP`.

### File transfer Protocol

Das File Transfer Protocol stammt aus dem Jahre 1971 und wurde primär dafür konzipiert, Dateien in einem Netzwerk von A nach B zu übertragen.

Dazu wird ein FTP Server betrieben, zu dem jeder beliebige FTP Client eine Verbindungen aufbauen kann.

Mit einem Benutzernamen und Passwort kann man sich gegenüber dem Server (Port 21) authentifizieren. Anschliessend können Dateien in beide Richtungen übertragen werden.

### WinSCP

Ein beliebter FTP-Client für Windows ist [`WinSCP`](https://winscp.net/eng/download.php). Die Software ist kostenlos erhältlich. 

**Achte darauf, den Download von der offiziellen Projektseite [winscp.net](https://winscp.net/eng/download.php) zu verwenden. Es gibt diverse Installer für WinSCP mit gebundelter Malware im Internet zu finden.**

## Aufgabe

Veröffentliche eine Datei auf den FTP Server der ICT-BZ und rufe sie auf deinem Smartphone auf.
