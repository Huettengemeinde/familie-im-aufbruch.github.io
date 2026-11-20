# Familie im Aufbruch

Die Website ist unter [familie-im-aufbruch.de](https://familie-im-aufbruch.de) erreichbar.

## Erste Schritte (Windows)

### 1. Voraussetzungen installieren

- **Git for Windows**: [git-scm.com](https://git-scm.com/download/win) herunterladen und mit den Standardoptionen installieren.
- **Visual Studio Code**: [code.visualstudio.com](https://code.visualstudio.com/) herunterladen. Beim Installer den **System Installer** wählen und **„Zu PATH hinzufügen“** aktivieren.

### Das richtige KI-Modell auswählen

Wähle in GitHub Copilot bevorzugt **GPT-6 Luna Medium** mit einem **272K-Kontextfenster** aus und prüfe vor jeder Anfrage, dass es ausgewählt ist.

## Inhalte

- `docs/index.html` – Inhalt und Aufbau der Website
- `docs/main.css` – Gestaltung
- `docs/img/` – Bilder

Die Website bleibt statisches HTML: Styles gehören in `docs/main.css`; JavaScript wird nicht verwendet.

## Änderungen mit GitHub Copilot

Manuel kann Änderungen in normaler Sprache beschreiben. GitHub Copilot übernimmt die Git-Schritte automatisch:

- Für jede neue Änderung einen Feature-Branch (`feature/*`) erstellen.
- Nach jedem Commit den aktuellen Branch zu `origin` pushen.
- Keine Pull Requests erstellen.
- Bei „veröffentlichen“ den Feature-Branch direkt in `main` mergen, `main` zu `origin` pushen und den Feature-Branch lokal sowie auf `origin` löschen.
