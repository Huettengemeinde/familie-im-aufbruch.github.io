# familie-im-aufbruch.github.io

Dieses Repository enthält die Webseite für Familie im Aufbruch, erreichbar unter [familie-im-aufbruch.de](https://familie-im-aufbruch.de).

## Erste Schritte (Windows)

Diese Anleitung richtet sich an neue Mitwirkende unter Windows und führt von der Installation bis zum ersten Pull Request.

### Was ist Git und wozu wird es gebraucht?

**Git** ist ein Programm, das jede Änderung an den Dateien dieser Webseite nachvollziehbar speichert – vergleichbar mit einer sehr ausführlichen "Änderungshistorie" bzw. einem "Speicherstand" wie in einem Videospiel. Jede gespeicherte Änderung (ein sogenannter **Commit**) bleibt für immer erhalten, sodass man jederzeit sehen kann, wer was wann geändert hat, und notfalls auch zu einem älteren Stand zurückkehren kann. **GitHub** wiederum ist die Webseite, auf der eine Online-Kopie dieser Git-Historie liegt – dort tauschen sich Manuel und Jörg über den aktuellen Stand der Webseite aus.

Die gute Nachricht: Man muss dafür keine Git-Befehle auswendig lernen oder in einer schwarzen Konsole eintippen. In dieser Anleitung passiert das alles über Buttons und Menüs in VS Code – und wie im nächsten Abschnitt beschrieben, kann sogar Copilot Chat diese Schritte auf Zuruf übernehmen.

### 1. Voraussetzungen installieren

- **Git for Windows**: [git-scm.com](https://git-scm.com/download/win) herunterladen und mit den Standardoptionen installieren. Wird von VS Code für alle Git-Funktionen benötigt.
- **Visual Studio Code**: [code.visualstudio.com](https://code.visualstudio.com/) herunterladen. Beim Installer den **"System Installer"** wählen (nicht "User Installer"), damit VS Code für alle Benutzer des PCs verfügbar ist. Haken bei "Zu PATH hinzufügen" setzen.

### 2. VS Code Extensions installieren

In VS Code über die Extensions-Ansicht (`Strg+Shift+X`) installieren:

- **GitHub Pull Requests** (`GitHub.vscode-pull-request-github`) – zum Erstellen und Verwalten von Pull Requests direkt in VS Code, ohne zusätzliche Software wie GitHub Desktop.
- **Git Graph** (`mhutchie.git-graph`) – visualisiert die Commit-Historie und Branches.
- **Material Icon Theme** (`PKief.material-icon-theme`) – übersichtliche Datei-Icons im Explorer.
- **GitHub Copilot** (`GitHub.copilot`) und **GitHub Copilot Chat** (`GitHub.copilot-chat`) – KI-Unterstützung beim Programmieren, falls noch nicht vorhanden.

### 3. Bei GitHub anmelden & Copilot Pro abonnieren

- Falls noch kein GitHub-Account existiert: einen kostenlosen Account unter [github.com/join](https://github.com/join) anlegen.
- In VS Code unten links auf das Account-Icon klicken und mit dem eigenen GitHub-Account anmelden.
- Für die Nutzung von Copilot Chat wird ein **GitHub Copilot Pro** Abo (ca. 10 USD/Monat) benötigt, abschließbar unter [github.com/settings/copilot](https://github.com/settings/copilot).

### 4. Copilot Chat öffnen

- Das Chat-Fenster öffnet sich über das Copilot-Symbol oben rechts in der VS Code Titelleiste, über das Symbol in der linken Seitenleiste oder per Tastenkombination `Strg+Alt+I`.
- Beim allerersten Öffnen erscheint eventuell eine Meldung, dass sich VS Code bei GitHub anmelden möchte ("Sign in with GitHub"). Auf **"Anmelden"** bzw. **"Allow"** klicken – es öffnet sich der Browser, in dem der Zugriff für VS Code bestätigt werden muss. Anschließend zurück zu VS Code wechseln, das Chat-Fenster ist danach einsatzbereit.
- Ist man bereits wie in Schritt 3 beschrieben mit dem GitHub-Account angemeldet, öffnet sich der Chat direkt ohne weitere Anmeldung.

### 5. Das richtige KI-Modell auswählen

Im Chat-Fenster gibt es oben bzw. unten im Eingabefeld eine Dropdown-Auswahl für das **Modell**. Dort stehen unter anderem verschiedene Claude-Modelle zur Verfügung:

- **Claude Haiku**: schnell und sparsam im Verbrauch, gut geeignet für einfache, klar umrissene Aufgaben wie kleine Textänderungen, kurze Fragen oder simple Korrekturen.
- **Claude Sonnet**: etwas langsamer, dafür deutlich gründlicher und besser im Verstehen komplexerer Zusammenhänge – die richtige Wahl bei größeren Änderungen, mehreren betroffenen Dateien oder wenn Copilot selbstständig mehrere Schritte (z. B. Branch erstellen, Änderungen machen, committen, pushen, Pull Request erstellen) hintereinander ausführen soll.

**Faustregel:** Im Zweifel **Claude Sonnet** auswählen – es liefert die zuverlässigeren Ergebnisse. Nur bei ganz kleinen, schnellen Anliegen (z. B. "Was bedeutet dieser Begriff?") lohnt sich der Wechsel zu Claude Haiku.

### 6. Repository klonen

1. Befehlspalette öffnen (`Strg+Shift+P`) → **"Git: Clone"** eingeben und auswählen.
2. Die URL dieses Repositorys einfügen: `https://github.com/Huettengemeinde/familie-im-aufbruch.github.io`
3. Zielordner auf der Festplatte wählen (z. B. ein neuer Ordner "Projekte" im Explorer).
4. Im Dialog auf **"Open"** klicken, um das geklonte Repository zu öffnen.

Damit liegt die komplette Webseite jetzt als Kopie auf dem eigenen PC und kann in VS Code bearbeitet werden. Ein Klonen ist nur einmal nötig – danach reicht es, den Ordner bei Bedarf einfach wieder in VS Code zu öffnen (**Datei → Ordner öffnen…**).

### 7. Wo befinden sich die Inhalte der Webseite?

- **`docs/index.html`** – der eigentliche Text und Aufbau der Webseite.
- **`docs/main.css`** – das gesamte Design (Farben, Schriften, Abstände). Styles gehören immer hierher, nie direkt in die HTML-Datei.
- **`docs/img/`** – alle Bilder der Webseite.

Auf JavaScript wird bewusst verzichtet, die Seite bleibt reines, statisches HTML. Wer mit GitHub Copilot Chat arbeitet, muss sich darum aber nicht selbst kümmern – einfach beschreiben, was geändert werden soll (z. B. *"Ändere die Überschrift auf der Startseite in ..."* oder *"Füge ein neues Bild im Abschnitt Über uns ein"*), Copilot hält sich automatisch an diese Regeln.

### 8. Lokale Vorschau der Webseite ansehen

Damit man Änderungen sofort im Browser sehen kann, ohne etwas zu veröffentlichen:

1. Im Explorer von VS Code (linke Seitenleiste) mit der rechten Maustaste auf **`docs/index.html`** klicken.
2. **"Reveal in File Explorer"** (Windows-Explorer) auswählen.
3. Im geöffneten Windows-Explorer die Datei **`index.html`** doppelklicken – sie öffnet sich im Standard-Browser (z. B. Chrome oder Edge).
4. Nach jeder Änderung im Browser einfach **F5** drücken, um die Seite neu zu laden und die Änderung zu sehen.

**Entwicklertools zum Testen:** Im Browser mit **F12** die Entwicklertools öffnen. Dort gibt es ein Symbol für ein Handy/Tablet (meist oben links in den Entwicklertools, "Responsive Design Mode" bzw. "Device Toolbar"). Damit lässt sich sehen, wie die Webseite auf unterschiedlichen Geräten aussieht – z. B. Laptop, Tablet und Smartphone – ohne die Geräte tatsächlich zu besitzen.

### 9. Neuen Branch erstellen, bevor man Änderungen macht

Bevor Änderungen vorgenommen werden, sollte immer ein eigener Branch angelegt werden (das ist wie eine eigene Arbeitskopie, die den Hauptstand der Seite nicht durcheinanderbringt):

1. Unten links in der Statusleiste von VS Code auf den Branch-Namen (z. B. "main") klicken.
2. **"Create new branch..."** auswählen.
3. Einen kurzen, beschreibenden Namen eingeben, z. B. `manuel/neuer-text-startseite`.

> 💡 **Einfacher geht's mit Copilot:** Diesen Schritt muss man nicht selbst über die Menüs klicken. Es reicht, Copilot Chat zu schreiben: *"Erstelle einen neuen Branch für meine Änderung an der Startseite"* – Copilot führt den nötigen Git-Befehl automatisch im Hintergrund aus.

### 10. Änderungen vornehmen

Änderungen können direkt selbst im Editor gemacht werden, oder man lässt sich von **GitHub Copilot Chat** helfen: Chat öffnen (wie in Schritt 4 beschrieben), beschreiben was geändert werden soll, und die Änderungen von Copilot direkt in den Dateien übernehmen lassen. Mit der Live-Vorschau aus Schritt 8 lässt sich das Ergebnis sofort kontrollieren.

**Nicht vergessen:** Geänderte Dateien vor dem nächsten Schritt speichern (`Strg+S`). Ein kleiner Punkt statt eines Kreuzes im Tab-Reiter oben zeigt an, dass eine Datei noch ungespeichert ist. Wenn Copilot die Änderungen vornimmt, speichert es normalerweise automatisch mit ab.

### 11. Änderungen speichern (Commit) und hochladen (Push)

1. Auf das Source-Control-Symbol in der linken Seitenleiste klicken (oder `Strg+Shift+G`).
2. Oben ein kurzes Textfeld ausfüllen, das beschreibt, was geändert wurde (z. B. "Text auf Startseite angepasst").
3. Auf den Haken **"Commit"** klicken, um die Änderung lokal zu speichern.
4. Anschließend auf **"Sync Changes"** bzw. **"Publish Branch"** klicken, um die Änderungen zu GitHub hochzuladen.

> 💡 **Einfacher geht's mit Copilot:** Auch Commit und Push müssen nicht manuell angeklickt werden. Einfach in Copilot Chat schreiben: *"Committe meine Änderungen mit einer passenden Nachricht und lade sie hoch"* – Copilot formuliert die Commit-Nachricht und führt Commit sowie Push selbstständig aus.

### 12. Pull Request erstellen

Ein Pull Request ist die Anfrage, die eigenen Änderungen in die eigentliche Webseite zu übernehmen:

1. Extension **GitHub Pull Requests** verwenden: Symbol in der linken Seitenleiste öffnen.
2. Auf **"Create Pull Request"** klicken.
3. Titel und kurze Beschreibung eingeben, dann auf **"Create"** klicken.

Jörg bekommt den Pull Request danach automatisch zur Prüfung und kümmert sich um die Veröffentlichung. Ein Login auf der GitHub-Webseite ist für diesen kompletten Ablauf nicht nötig – alles funktioniert direkt aus VS Code heraus.

> 💡 **Einfacher geht's mit Copilot:** Auch den Pull Request muss man nicht über die Menüs erstellen. Einfach in Copilot Chat schreiben: *"Erstelle einen Pull Request für meine Änderungen"* – Copilot legt ihn inklusive Titel und Beschreibung an.

### 13. Bei Fragen einfach Copilot Chat fragen

Egal ob "Wie erstelle ich einen neuen Branch?", "Wie füge ich ein Bild ein?" oder "Warum funktioniert etwas nicht?" – GitHub Copilot Chat in VS Code kann jederzeit auf Deutsch gefragt werden und hilft direkt im Editor weiter.

**Wichtig zu wissen:** Man muss sich keinen einzigen Git-Befehl merken oder wissen, in welchem Menü etwas zu finden ist. Branch erstellen, Commit, Push und Pull Request – **alle** diese Schritte aus dieser Anleitung kann man stattdessen einfach in normalen deutschen Sätzen von Copilot Chat erledigen lassen, z. B. *"Speichere meine Änderungen, lade sie hoch und erstelle einen Pull Request"* macht Copilot in einem Rutsch komplett selbstständig.

### 14. Bereit für die nächste Änderung

Sobald Jörg den Pull Request geprüft und übernommen ("gemerged") hat, ist die Änderung offiziell auf der Webseite. Für die nächste Änderung:

1. Unten links in der Statusleiste auf den aktuellen Branch-Namen klicken und zurück zu **"main"** wechseln.
2. Auf **"Sync Changes"** klicken, damit der neueste Stand von GitHub geladen wird.
3. Wieder bei Schritt 9 (neuen Branch erstellen) starten.

Auch das lässt sich komplett Copilot überlassen: einfach schreiben *"Wechsle zurück zu main, hole den neuesten Stand und erstelle einen neuen Branch für ..."*.

