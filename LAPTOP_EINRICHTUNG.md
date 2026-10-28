# Laptop einrichten (einmalig)

Voraussetzung: Git ist installiert, du bist bei GitHub angemeldet (beim ersten Clone erscheint das Anmeldefenster).

1. Repo holen:
   `git clone https://github.com/marcuswiertz/CodingMemo.git C:\CodingMemo`
2. Diesen Block ans Ende von `C:\Users\<Name>\.claude\CLAUDE.md` UND in `C:\Users\<Name>\.codex\AGENTS.md` einfügen (Dateien anlegen, falls nicht vorhanden):

```
## Gemeinsames Coding-Memo (Claude und Codex)
Liegt in `C:\CodingMemo` (privates Git-Repo, Remote GitHub). Bei jedem Projekt-Chat: `git -C C:\CodingMemo pull`, dann `INDEX.md` und die Projektdatei lesen. Nach Code-Änderungen und vor Chat-Ende Projektdatei und `INDEX.md` aktualisieren, dann `git -C C:\CodingMemo add -A`, `commit`, `push`. Immer mit `-C C:\CodingMemo`, damit nie das Projekt-Repo (Gitea/Coolify) getroffen wird. Regeln: `C:\CodingMemo\README.md`. Keine Geheimnisse eintragen.
```
3. Test: In einem neuen Chat fragen „Was steht im Coding-Memo zu LIBERO?“. Die Antwort muss aus `INDEX.md` kommen.

## Alltag
- Vor der Arbeit: der Assistent zieht selbst (`pull`). Du kannst es auch von Hand tun: `git -C C:\CodingMemo pull`.
- Nach der Arbeit: der Assistent pusht selbst. Vor dem Wechsel zum anderen Rechner prüfen: `git -C C:\CodingMemo status` zeigt „up to date“ und nichts Offenes.
- Bei Merge-Konflikt: nichts überschreiben, beide Stände behalten und Claude oder Codex den Konflikt zeigen.

## Hinweise
- Projektpfade in `INDEX.md` gelten für den PC. Am Laptop können sie abweichen; dann beim Eintrag den Laptop-Pfad ergänzen.
- Das Memo-Repo hat nichts mit deinen Projekt-Repos zu tun und darf nie in einem Projektordner liegen.
