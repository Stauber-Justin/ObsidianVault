Eine **globale `.gitignore`-Datei** hilft dabei, unerwünschte Dateien und Ordner in all deinen Git-Repositories zu ignorieren, insbesondere solche, die von deinem Betriebssystem oder deinen Entwicklungswerkzeugen erzeugt werden. Hier ist, wie du eine solche Datei einrichtest und welche Best Practices du beachten solltest:

### Einrichtung einer globalen `.gitignore`-Datei

1. **Globale `.gitignore`-Datei erstellen:**
    
    - **macOS/Linux:** Erstelle eine Datei namens `.gitignore_global` in deinem Home-Verzeichnis:
        
        ```bash
        touch ~/.gitignore_global
        ```
        
    - **Windows:** Erstelle die Datei `.gitignore_global` in deinem Benutzerverzeichnis:
        
        ```bash
        echo. > %USERPROFILE%\.gitignore_global
        ```
        
2. **Git konfigurieren, diese Datei zu verwenden:**
    
    - **macOS/Linux:**
        
        ```bash
        git config --global core.excludesfile ~/.gitignore_global
        ```
        
    - **Windows:**
        
        ```bash
        git config --global core.excludesfile "%USERPROFILE%\.gitignore_global"
        ```
        

### Inhalt der globalen `.gitignore`-Datei

In die globale `.gitignore`-Datei sollten Dateien und Ordner aufgenommen werden, die von deinem Betriebssystem oder deinen Entwicklungswerkzeugen generiert werden und nicht versionsverwaltet werden sollten. Hier einige Beispiele:

- **macOS:**

```
  # macOS-spezifische Dateien
  .DS_Store
```

- **Windows:**

```
  # Windows-spezifische Dateien
  Thumbs.db
```

- **Allgemein:**

```
  # Logdateien
  *.log

  # Temporäre Dateien
  *.tmp
  *.swp

  # Verzeichnisse für lokale Umgebungen
  .vscode/
  .idea/
```

### Best Practices

- **Projektspezifische Ausschlüsse:** Verwende die projektbezogene `.gitignore`-Datei für Dateien und Ordner, die spezifisch für dieses Projekt sind, wie z.B. Build-Ordner oder Abhängigkeitsverzeichnisse.
    
- **Globale Ausschlüsse:** Nutze die globale `.gitignore` für Dateien und Ordner, die in allen Projekten ignoriert werden sollen, wie z.B. Editor- oder Betriebssystemdateien.
    
- **Vermeide persönliche Einstellungen im Projekt:** Teile keine persönlichen Editor- oder IDE-Einstellungen in der projektspezifischen `.gitignore`. Diese sollten in der globalen `.gitignore` stehen, um Konflikte mit anderen Entwicklern zu vermeiden.
    
- **Überprüfung der Ignorierregeln:** Falls du unsicher bist, warum eine Datei ignoriert wird, kannst du den folgenden Befehl verwenden:
    

```bash
  git check-ignore -v <dateiname>
```

Dieser zeigt dir, welche Regel in welcher `.gitignore`-Datei für das Ignorieren verantwortlich ist.

Durch die Beachtung dieser Richtlinien stellst du sicher, dass deine Git-Repositories sauber bleiben und keine unnötigen oder persönlichen Dateien enthalten.