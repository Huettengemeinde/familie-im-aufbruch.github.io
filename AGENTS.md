# AGENTS.md – Familie im Aufbruch

## Team

Dieses Repository wird gemeinschaftlich gepflegt:

- **Manuel Schick** (manu.schick85@googlemail.com)  
  GitHub: [@manu6006-ai](https://github.com/manu6006-ai)

## Git Workflow & Code Review

Manuel arbeitet hauptsächlich an diesem Repository und erledigt alles automatisiert mit Codex. Er ist kein Softwareentwickler und kennt sich technisch nicht aus – er interessiert sich ausschließlich für Content und UX. Du musst ihn dabei maximal unterstützen und alle Git-Operationen automatisch ausführen.

Für jede von Manuel beauftragte Änderung erstellt Codex automatisch einen Feature-Branch nach dem Muster `feature/*`. Sobald dieser Branch in `main` gemergt wurde, löscht Codex ihn sowohl lokal als auch remote auf `origin`.

Da Manuel mit Git und Versionsverwaltung nicht vertraut ist, verwendet er möglicherweise Begriffe wie "Branch" oder "Zweig" nicht. Achte deshalb auch auf Formulierungen wie "neue Änderung" (eine Änderung beginnen) und "veröffentlichen" (den fertigen Feature-Branch in `main` mergen und `main` zu `origin` pushen).

---

## Code-Konventionen

- **Kein inline CSS**: Styles gehören immer in separate CSS-Dateien (z. B. `main.css`), nicht in `style`-Attribute oder `<style>`-Blöcke innerhalb von HTML-Dateien.
- **Kein JavaScript**: Die Seite bleibt reines, statisches HTML. Auf JavaScript wird bewusst verzichtet.

---

