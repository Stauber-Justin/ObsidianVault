# 📄 .gitignore & .gitkeep Cheat Sheet

## 🎯 **Grundlagen der .gitignore**

Die `.gitignore`-Datei wird verwendet, um bestimmte Dateien oder Ordner vom Git-Tracking auszuschließen. Dies ist nützlich für temporäre Dateien, sensible Daten oder Build-Outputs.

**Syntax:**

- `/` am Anfang: Ignoriert Pfade vom Root-Verzeichnis aus.
- `*`: Platzhalter für beliebige Zeichen.
- `**`: Platzhalter für beliebige Zeichen über mehrere Verzeichnisebenen.
- `!`: Nimmt eine Datei oder einen Ordner wieder auf, der vorher ausgeschlossen wurde.

**Beispiele:**

```gitignore
# Ignoriere alle .log-Dateien
*.log

# Ignoriere den node_modules-Ordner
/node_modules/

# Ignoriere alle Dateien in einem Ordner, außer eine bestimmte Datei
/config/*
!/config/settings.json

# Ignoriere alle .env-Dateien, außer die Vorlage
*.env
!example.env
```

---

## 📁 **.gitkeep für leere Ordner**

Git trackt standardmäßig keine leeren Ordner. Um dennoch einen leeren Ordner im Repository zu behalten, kann eine `.gitkeep`-Datei erstellt werden.

**Verwendung:**

1. Erstelle eine leere Datei namens `.gitkeep` in dem entsprechenden Ordner.
2. Füge sie dem Repository hinzu:

```bash
touch path/to/empty_folder/.gitkeep
git add path/to/empty_folder/.gitkeep
git commit -m "Keep empty folder tracked"
```

**Wichtig:** Die `.gitkeep`-Datei ist eine Konvention, keine offizielle Git-Funktion. Sie wird lediglich als Platzhalter verwendet.

---
## 🔑 **Wichtige Tipps für die Arbeit mit .gitignore**

1. **Reihenfolge zählt:** Git liest die `.gitignore`-Datei von oben nach unten.
2. **Spezifität schlägt Allgemeinheit:** Je spezifischer ein Eintrag, desto höher seine Priorität.
3. **Globale .gitignore:** Für alle Projekte auf deinem System kannst du eine globale `.gitignore` definieren:

```bash
git config --global core.excludesfile ~/.gitignore_global
```

1. **Überprüfen, was ignoriert wird:**

```bash
git check-ignore -v filename
```

1. **Bereits getrackte Dateien entfernen:** Falls du Änderungen an der `.gitignore` machst, entferne bestehende Dateien aus dem Tracking:

```bash
git rm --cached -r .
```

1. **Nur bestimmte Dateitypen ausschließen:**

```gitignore
# Alle PNG-Dateien ausschließen
*.png

# PNGs aus einem bestimmten Verzeichnis nicht ausschließen
!/images/logo.png
```

---

## 🛠️ **Weitere hilfreiche Muster**

```gitignore
# MacOS-Systemdateien
.DS_Store

# Windows-Systemdateien
Thumbs.db

# IDEs
.vscode/
.idea/

# Backup-Dateien
*.bak
*.tmp

# Log-Dateien
logs/
*.log

# Build-Ordner
/dist/
/build/
```

---

## 📝 **Nützliche Befehle für .gitignore**

|Befehl|Beschreibung|
|---|---|
|`git status`|Zeigt den Status der Arbeitskopie|
|`git check-ignore -v filename`|Prüft, warum eine Datei ignoriert wird|
|`git rm --cached filename`|Entfernt Datei aus dem Tracking|
|`git add .`|Fügt alle Änderungen zum Commit hinzu|
|`git commit -m "Message"`|Erstellt einen neuen Commit|

---

Mit dieser Anleitung solltest du für die Arbeit mit `.gitignore` und `.gitkeep` bestens vorbereitet sein! 🚀