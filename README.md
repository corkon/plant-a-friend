# Plant a friend (Prototyp als Web-App)

Das ist eine PWA: eine Web-App aus HTML, die du wie eine App auf den Home-Bildschirm legst.
Sie braucht keinen Mac, kein Xcode und keinen App Store.

## Dateien

- `index.html` – die ganze App (Oberfläche, Pflanzen, Regeln)
- `manifest.json` – Name, Farben und Icon für den Home-Bildschirm
- `sw.js` – speichert die App für den Offline-Betrieb
- `icons/` – App-Symbole

## Ausprobieren auf dem Computer

Doppelklick auf `index.html` öffnet die App im Browser. Der Offline-Modus und das Installieren
funktionieren erst, wenn die Dateien über `https://` erreichbar sind (siehe unten).

## Kostenlos ins Netz stellen

Die Dateien müssen irgendwo über https erreichbar sein. Zwei einfache Möglichkeiten
(die Oberflächen der Anbieter ändern sich manchmal, im Zweifel in deren Hilfe nachsehen):

1. **Netlify Drop:** Auf netlify.com die Seite „Drop" öffnen und den ganzen Ordner
   `plant-a-friend-pwa` hineinziehen. Du bekommst sofort eine Adresse.
2. **GitHub Pages:** Neues Repository anlegen, die Dateien hochladen, unter
   Settings → Pages den Zweig `main` auswählen.

## Auf das Handy holen

- **iPhone (Safari):** Adresse öffnen, auf Teilen tippen, dann „Zum Home-Bildschirm".
- **Android (Chrome):** Adresse öffnen, Menü mit den drei Punkten, dann „App installieren"
  oder „Zum Startbildschirm hinzufügen".

## Wichtig zu wissen

- **Daten:** Alles liegt nur auf dem Gerät, im Speicher des Browsers. Es gibt kein Konto und
  keinen Server. Sichere deine Daten regelmäßig über Menü → Einstellungen → Daten sichern.
- **Benachrichtigungen:** Eine Warnung kurz vor dem Verwelken, die dich bei geschlossener App
  erreicht, geht mit einer reinen Web-App nicht ohne Server. Im Prototyp zeigt die Dringlich-Gruppe
  oben, was Aufmerksamkeit braucht, und die Wochenübersicht erscheint beim Öffnen.
- **Schrift:** Die Pixel-Schrift „Pixelify Sans" kommt von Google Fonts. Ohne Internet beim
  allerersten Start sieht die App mit einer Ersatzschrift anders aus. Danach merkt sie sich die Schrift.
- **Beispieldaten:** Beim ersten Start siehst du sechs Beispiel-Pflanzen. Entfernen geht über
  das Menü oben links.

## Was du leicht selbst ändern kannst

- Farben: oben in `index.html` im Block `:root { ... }`
- Rhythmus der Kategorien (7, 21, 60 Tage): `GRADES` in `index.html`
- Wiederbelebungen pro Monat: `JOKERS` (aktuell 3)
- Ab wann eine Pflanze „dringlich" ist: in der Funktion `info` (aktuell ab 75 % des Rhythmus)
