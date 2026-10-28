# CodingMemo

Gemeinsames Gedächtnis für Claude Code und Codex, auf PC und Laptop. Privates Git-Repo.
Keine Geheimnisse (Schlüssel, Tokens, Passwörter, Kundendaten) in diesen Dateien.

- `INDEX.md`: alle Projekte, Zusammenhänge, Stand in einer Zeile.
- `projekte/<name>.md`: Detailstand je Projekt (Vorlage: `projekte/_VORLAGE.md`).

## Regeln für Claude und Codex
0. Git-Befehle für das Memo immer mit `git -C C:\CodingMemo ...`, nie im Projektordner (dort hängt ein anderes Remote, z. B. Gitea/Coolify).
1. **Start:** `git -C C:\CodingMemo pull`, dann `INDEX.md` und die Datei des betroffenen Projekts lesen.
2. **Ende** (nach Code-Änderungen, vor Chat-Ende): Projektdatei und Zeile in `INDEX.md` aktualisieren, dann
   `git add -A && git commit -m "<projekt>: <kurz>" && git push`.
3. Nur Überprüfbares als Fakt eintragen; Vermutungen kennzeichnen. Details mit Pfad verweisen, nicht kopieren.
4. Bei Merge-Konflikt: beide Stände behalten und Marcus melden, nie blind überschreiben.
5. Jeder Eintrag nennt Autor (Claude/Codex), Datum und Rechner (PC/Laptop).
