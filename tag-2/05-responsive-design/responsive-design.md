# Responsive Design

Responsive Design bezeichnet die Fähigkeit eines Layouts sich automatisch auf verschiedene Geräteattribute anzupassen. Insbesondere ist damit die Grösse eines Displays gemeint.

## Beispiel

Rufe die Website [https://www.smashingmagazine.com/](https://www.smashingmagazine.com/) auf und verändere die Fenstergrösse.

## Grundsätze

Grundsätzlich wird oft zwischen drei Bildschirmgrössen unterschieden: `Desktop`, `Tablet` und `Mobile`. Diese Grössen bieten dir eine gute Basis zum Designen deiner Website, jedoch solltest du dein Layout nicht auf gewisse Bildschirmgrössen fixieren:

Vor einigen Jahren konnte man seine Website für ein iPhone (320x480), ein iPad (768x1024) und Desktops (1920x1080) auslegen. Heute gibt es jedoch so viele unterschiedliche Bildschirmgrössen, dass eine Ausrichtung auf diese Bildschirmauflösungen weniger Sinn macht.

Stattdessen solltest du dein Layout immer bei diesen Grössen verändern, wo dein Inhalt nicht mehr genügend Platz hat um korrekt dargestellt zu werden.

## Mobile first vs. Desktop first

Jede Website sollte zwar auf Mibiles und Desktop funktionieren. Je nach Zielgruppe und Komplexität der Website wird diese aber primär für mobile oder für Desktop-Geräte entwickelt.&#x20;

### Mobile first

**Mobile-First-Design** ist ein Webdesign-Ansatz, bei dem die Website zuerst für Benutzer von Mobilen Geräten optimiert wird. Danach wird eine Version für grössere Bildschirme entworfen.&#x20;

**Im CSS** werden zuerst die Definitionen für kleine Bildschirme geschrieben, danach mittels Media-Queries für grosse Displays überschrieben.&#x20;

**Wann wähle ich diesen Ansatz?**\
Für einfachere Websites und Applikationen, die oft unterwegs benutzt werden.&#x20;

**Beispiel:** Ein B2C-Webshop (Business to Customer) für Ticket-Verkauf.

### Desktop first

**Desktop-First-Design** ist ein Webdesign-Ansatz, bei dem das Desktop- oder Laptop-Erlebnis im Vordergrund steht. Die Website wird zunächst für den Desktop-Nutzer entworfen und dann an kleinere Bildschirme angepasst.

**Im CSS** werden zuerst die Definitionen für grosse Bildschirme geschrieben, danach mittels Media-Queries für kleine Displays übersteuert.&#x20;

**Wann wähle ich diesen Ansatz?** \
Für komplexe Websites mit vielen Elementen oder Business-Websites, welche oft im Büro aufgerufen werden.&#x20;

**Beispiel:** Ein B2B-Webshop (Business to Business) für Material-Bestellung.



## Nützliche Links

* [softermii.com/blog/web-development-mobile-first-or-desktop-first](https://www.softermii.com/blog/web-development-mobile-first-or-desktop-first) (english)

