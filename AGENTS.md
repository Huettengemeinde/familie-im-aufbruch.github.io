# AGENTS.md – Familie im Aufbruch

## Team

Dieses Repository wird gepflegt von:

- **Manuel Schick** (manu.schick85@googlemail.com)  
  GitHub: [@manu6006-ai](https://github.com/manu6006-ai)

## Git-Workflow

Manuel arbeitet hauptsächlich an diesem Repository und erledigt alles automatisiert mit einem Agenten. Er ist kein Softwareentwickler und kennt sich technisch nicht aus – er interessiert sich ausschließlich für Content und UX. Du musst ihn dabei maximal unterstützen und alle Git-Operationen automatisch ausführen.

Sobald Manuel eine neue Änderung beauftragt, erstellt der Agent automatisch einen Feature-Branch nach dem Muster `feature/*`. Nach jedem Commit pusht der Agent den aktuellen Branch zu `origin`. Es werden keine Pull Requests erstellt. Wenn Manuel eine Änderung veröffentlichen möchte, merged der Agent den Feature-Branch direkt in `main`, pusht `main` zu `origin` und löscht den Feature-Branch lokal und auf `origin`.

Manuel verwendet möglicherweise keine Git-Begriffe. Interpretiere daher auch „neue Änderung“ als Aufforderung, einen Feature-Branch anzulegen, und „veröffentlichen“ als Aufforderung, direkt nach `main` zu mergen und `main` zu pushen.

---

## Code-Konventionen

- **Kein inline CSS**: Styles gehören immer in separate CSS-Dateien (z. B. `main.css`), nicht in `style`-Attribute oder `<style>`-Blöcke innerhalb von HTML-Dateien.
- **Kein JavaScript**: Die Seite bleibt reines, statisches HTML. Auf JavaScript wird bewusst verzichtet.

---

