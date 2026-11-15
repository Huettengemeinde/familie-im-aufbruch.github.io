# familie-im-aufbruch.github.io

Dieses Repository enthält die Webseite für Familie im Aufbruch, erreichbar unter [familie-im-aufbruch.de](https://familie-im-aufbruch.de).

## Erste Schritte (Windows)

Diese Anleitung richtet sich an neue Mitwirkende unter Windows und führt von der Installation bis zur Veröffentlichung von Änderungen.

### Was ist Git und wozu wird es gebraucht?

**Git** ist ein Programm, das jede Änderung an den Dateien dieser Webseite nachvollziehbar speichert – vergleichbar mit einer sehr ausführlichen "Änderungshistorie" bzw. einem "Speicherstand" wie in einem Videospiel. Jede gespeicherte Änderung (ein sogenannter **Commit**) bleibt für immer erhalten, sodass man jederzeit sehen kann, wer was wann geändert hat, und notfalls auch zu einem älteren Stand zurückkehren kann. **GitHub** wiederum ist die Webseite, auf der eine Online-Kopie dieser Git-Historie liegt.

Die gute Nachricht: Man muss dafür keine Git-Befehle auswendig lernen oder in einer schwarzen Konsole eintippen. In dieser Anleitung passiert das alles über Buttons und Menüs in VS Code – und wie im nächsten Abschnitt beschrieben, kann sogar Codex diese Schritte auf Zuruf übernehmen.

### 1. Voraussetzungen installieren

- **Git for Windows**: [git-scm.com](https://git-scm.com/download/win) herunterladen und mit den Standardoptionen installieren. Wird von VS Code für alle Git-Funktionen benötigt.
- **Visual Studio Code**: [code.visualstudio.com](https://code.visualstudio.com/) herunterladen. Beim Installer den **"System Installer"** wählen (nicht "User Installer"), damit VS Code für alle Benutzer des PCs verfügbar ist. Haken bei "Zu PATH hinzufügen" setzen.

### 2. VS Code Extensions installieren

In VS Code über die Extensions-Ansicht (`Strg+Shift+X`) installieren:

- **Git Graph** (`mhutchie.git-graph`) – visualisiert die Commit-Historie und Branches.
- **Material Icon Theme** (`PKief.material-icon-theme`) – übersichtliche Datei-Icons im Explorer.
- **Codex** (`openai.chatgpt`) – KI-Unterstützung beim Programmieren.

### 3. Bei Codex anmelden

- Die Codex-Erweiterung öffnen und den Anweisungen zur Anmeldung mit dem eigenen OpenAI- bzw. ChatGPT-Konto folgen.

### 4. Codex öffnen

- Das Codex-Fenster über das Codex-Symbol in der Seitenleiste öffnen. Falls das Symbol nicht sichtbar ist, die Befehlspalette mit `Strg+Shift+P` öffnen und **"Codex: Open Codex Sidebar"** ausführen.

### 5. Codex verwenden

Codex kann Fragen beantworten, Dateien bearbeiten und bei Git-Aufgaben helfen. Änderungen und angeforderte Befehle vor dem Bestätigen prüfen.

### 6. Das richtige KI-Modell auswählen

Im Codex-Fenster gibt es eine Auswahl für das **Modell**. Wähle dort bevorzugt **GPT-6 Luna Medium** mit einem **272K-Kontextfenster** aus.

Prüfe vor jeder Anfrage, dass dieses Modell ausgewählt ist.

### 7. Repository klonen

1. Befehlspalette öffnen (`Strg+Shift+P`) → **"Git: Clone"** eingeben und auswählen.
2. Die URL dieses Repositorys einfügen: `https://github.com/Huettengemeinde/familie-im-aufbruch.github.io`
3. Zielordner auf der Festplatte wählen (z. B. ein neuer Ordner "Projekte" im Explorer).
4. Im Dialog auf **"Open"** klicken, um das geklonte Repository zu öffnen.

Damit liegt die komplette Webseite jetzt als Kopie auf dem eigenen PC und kann in VS Code bearbeitet werden. Ein Klonen ist nur einmal nötig – danach reicht es, den Ordner bei Bedarf einfach wieder in VS Code zu öffnen (**Datei → Ordner öffnen…**).

### 8. Wo befinden sich die Inhalte der Webseite?

- **`docs/index.html`** – der eigentliche Text und Aufbau der Webseite.
- **`docs/main.css`** – das gesamte Design (Farben, Schriften, Abstände). Styles gehören immer hierher, nie direkt in die HTML-Datei.
- **`docs/img/`** – alle Bilder der Webseite.

Auf JavaScript wird bewusst verzichtet, die Seite bleibt reines, statisches HTML. Wer mit Codex arbeitet, muss sich darum aber nicht selbst kümmern – einfach beschreiben, was geändert werden soll (z. B. *"Ändere die Überschrift auf der Startseite in ..."* oder *"Füge ein neues Bild im Abschnitt Über uns ein"*), Codex hält sich automatisch an diese Regeln.

### 9. Lokale Vorschau der Webseite ansehen

Damit man Änderungen sofort im Browser sehen kann, ohne etwas zu veröffentlichen:

1. Im Explorer von VS Code (linke Seitenleiste) mit der rechten Maustaste auf **`docs/index.html`** klicken.
2. **"Reveal in File Explorer"** (Windows-Explorer) auswählen.
3. Im geöffneten Windows-Explorer die Datei **`index.html`** doppelklicken – sie öffnet sich im Standard-Browser (z. B. Chrome oder Edge).
4. Nach jeder Änderung im Browser einfach **F5** drücken, um die Seite neu zu laden und die Änderung zu sehen.

**Entwicklertools zum Testen:** Im Browser mit **F12** die Entwicklertools öffnen. Dort gibt es ein Symbol für ein Handy/Tablet (meist oben links in den Entwicklertools, "Responsive Design Mode" bzw. "Device Toolbar"). Damit lässt sich sehen, wie die Webseite auf unterschiedlichen Geräten aussieht – z. B. Laptop, Tablet und Smartphone – ohne die Geräte tatsächlich zu besitzen.

### 10. Neuen Branch erstellen, bevor man Änderungen macht

Bevor Änderungen vorgenommen werden, sollte immer ein eigener Branch angelegt werden (das ist wie eine eigene Arbeitskopie, die den Hauptstand der Seite nicht durcheinanderbringt):

1. Unten links in der Statusleiste von VS Code auf den Branch-Namen (z. B. "main") klicken.
2. **"Create new branch..."** auswählen.
3. Einen kurzen, beschreibenden Namen eingeben, z. B. `manuel/neuer-text-startseite`.

> 💡 **Einfacher geht's mit Codex:** Diesen Schritt muss man nicht selbst über die Menüs klicken. Es reicht, Codex zu schreiben: *"Erstelle einen neuen Branch für meine Änderung an der Startseite"* – Codex führt den nötigen Git-Befehl aus.

### 11. Änderungen vornehmen

Änderungen können direkt selbst im Editor gemacht werden, oder man lässt sich von **Codex** helfen: Codex öffnen (wie in Schritt 4 beschrieben), beschreiben was geändert werden soll, und die vorgeschlagenen Änderungen prüfen und übernehmen. Mit der Live-Vorschau aus Schritt 9 lässt sich das Ergebnis sofort kontrollieren.

**Nicht vergessen:** Geänderte Dateien vor dem nächsten Schritt speichern (`Strg+S`). Ein kleiner Punkt statt eines Kreuzes im Tab-Reiter oben zeigt an, dass eine Datei noch ungespeichert ist. Wenn Codex die Änderungen vornimmt, speichert es normalerweise automatisch mit ab.

### 12. Änderungen speichern (Commit) und hochladen (Push)

1. Auf das Source-Control-Symbol in der linken Seitenleiste klicken (oder `Strg+Shift+G`).
2. Oben ein kurzes Textfeld ausfüllen, das beschreibt, was geändert wurde (z. B. "Text auf Startseite angepasst").
3. Auf den Haken **"Commit"** klicken, um die Änderung lokal zu speichern.
4. Anschließend auf **"Sync Changes"** bzw. **"Publish Branch"** klicken, um die Änderungen zu GitHub hochzuladen.

> 💡 **Einfacher geht's mit Codex:** Auch Commit und Push des Feature-Branches müssen nicht manuell angeklickt werden. Einfach Codex schreiben: *"Committe meine Änderungen mit einer passenden Nachricht und lade meinen Feature-Branch hoch"* – Codex formuliert die Commit-Nachricht und führt Commit sowie Push aus.

### 13. Änderungen veröffentlichen

Es werden keine Pull Requests erstellt. Wenn die Änderungen fertig sind und veröffentlicht werden sollen, bitte Codex, den Feature-Branch direkt in `main` zu mergen und `main` zu GitHub zu pushen. Zum Beispiel: *"Veröffentliche meine Änderungen: Committe sie, merge meinen Feature-Branch in main und pushe main."*

### 14. Bei Fragen einfach Codex fragen

Egal ob "Wie erstelle ich einen neuen Branch?", "Wie füge ich ein Bild ein?" oder "Warum funktioniert etwas nicht?" – Codex in VS Code kann jederzeit auf Deutsch gefragt werden und hilft direkt im Editor weiter.

**Wichtig zu wissen:** Man muss sich keinen einzigen Git-Befehl merken oder wissen, in welchem Menü etwas zu finden ist. Branch erstellen, Commit, Push und Veröffentlichung – **alle** diese Schritte aus dieser Anleitung kann man stattdessen einfach in normalen deutschen Sätzen von Codex erledigen lassen, z. B. *"Veröffentliche meine Änderungen"* weist Codex an, den Feature-Branch in `main` zu mergen und `main` zu pushen.

### 15. Bereit für die nächste Änderung

Sobald Codex den Feature-Branch in `main` gemerged und `main` gepusht hat, ist die Änderung offiziell auf der Webseite. Für die nächste Änderung:

1. Unten links in der Statusleiste auf den aktuellen Branch-Namen klicken und zurück zu **"main"** wechseln.
2. Auf **"Sync Changes"** klicken, damit der neueste Stand von GitHub geladen wird.
3. Wieder bei Schritt 10 (neuen Branch erstellen) starten.

Auch das lässt sich komplett Codex überlassen: einfach schreiben *"Wechsle zurück zu main, hole den neuesten Stand und erstelle einen neuen Branch für ..."*.

