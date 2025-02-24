## ✅ **Teil 1: Hyper-V unter Windows 11 aktivieren**

### 🔒 **1. Systemvoraussetzungen prüfen**

Bevor du Hyper-V aktivierst, vergewissere dich, dass dein System es unterstützt:

1. **Task-Manager öffnen:**
    
    - Drücke `Strg` + `Shift` + `Esc` oder
    - Rechtsklick auf die Taskleiste → `Task-Manager`
2. Gehe auf den Reiter **"Leistung"** → Wähle links **"CPU"** aus.
    
3. Überprüfe unten rechts unter **"Virtualisierung"**, ob dort **"Aktiviert"** steht.
    
    - Falls **"Deaktiviert"**: Gehe ins BIOS/UEFI und aktiviere dort die Virtualisierung (meist unter "Advanced" → "Intel Virtualization Technology (VT-x)" oder "AMD-V").

---

### 🔧 **2. Hyper-V aktivieren**

1. **Einstellungen öffnen:**
    
    - Drücke `Windows` + `I` → Wähle links **"Apps"** → Klicke rechts auf **"Optionale Features"**.
2. Scrolle nach unten und klicke auf **"Weitere Windows-Features"**.
    
3. Setze ein Häkchen bei:
    
    - **Hyper-V**
        - Darunter auch die beiden Unterpunkte aktivieren:
            - **Hyper-V-Plattform**
            - **Hyper-V-Verwaltungstools**
4. Klicke auf **"OK"** und lasse Windows die benötigten Dateien installieren.
    
5. Nach der Installation: **Neustart** erforderlich.
    

---

### 🖥️ **3. Hyper-V-Manager öffnen**

Nach dem Neustart:

1. Drücke `Windows` + `S` → Tippe **"Hyper-V-Manager"** → Klicke auf die App.
    
2. Falls du eine Meldung bekommst, dass keine Hyper-V-Verbindung besteht:
    
    - Wähle **"Lokaler Computer"** → Klicke auf **"OK"**.

---

## ✅ **Teil 2: Eine Windows 11 VM unter Hyper-V erstellen**

### 📦 **1. ISO-Datei von Windows 11 besorgen**

1. Gehe zur offiziellen Microsoft-Seite für Windows 11:  
    [https://www.microsoft.com/de-de/software-download/windows11](https://www.microsoft.com/de-de/software-download/windows11)
    
2. Lade eine ISO-Datei herunter.
    
    - Wähle **"Windows 11 (Multi-Edition ISO)"** und folge den Anweisungen.

---

### 🏗️ **2. Neue virtuelle Maschine erstellen**

1. **Hyper-V-Manager öffnen**
    
    - Rechts im Fenster auf **"Neu"** → **"Virtuelle Maschine..."** klicken.
2. Im **"Neuen virtuellen Computer-Assistenten"**:
    
    - Klicke auf **"Weiter"**.
3. **Name und Speicherort**:
    
    - Gib der VM einen Namen, z.B. **"Windows 11 Testumgebung"**.
    - Optional: Haken setzen bei **"Speicherort angeben"** und Pfad wählen.
    - Klicke auf **"Weiter"**.
4. **Generation wählen**:
    
    - Wähle **"Generation 2"** (empfohlen für Windows 11).
    - Klicke auf **"Weiter"**.
5. **Arbeitsspeicher zuweisen**:
    
    - Empfohlen: mindestens **4096 MB** (4 GB) für flüssiges Arbeiten.
    - Deaktiviere **"Dynamischen Arbeitsspeicher verwenden"** für bessere Performance.
    - Klicke auf **"Weiter"**.
6. **Netzwerkkonfiguration**:
    
    - Wähle **"Standard-Switch"** für Internetzugriff.
    - Klicke auf **"Weiter"**.
7. **Virtuelle Festplatte konfigurieren**:
    
    - Erstelle eine neue Festplatte, z.B. **64 GB**.
    - Klicke auf **"Weiter"**.
8. **Installationsoptionen festlegen**:
    
    - Wähle **"Betriebssystem von einer startfähigen CD/DVD installieren"**.
    - Klicke auf **"Durchsuchen"** und wähle die heruntergeladene ISO-Datei aus.
    - Klicke auf **"Weiter"**.
9. **Zusammenfassung** prüfen → **"Fertig stellen"**.
    

---

### 🚀 **3. Windows 11 auf der VM installieren**

1. Im Hyper-V-Manager → Rechtsklick auf die neue VM → **"Verbinden..."** → Dann auf **"Start"** klicken.
    
2. Windows 11 Setup wird geladen:
    
    - Sprache, Zeit, Tastatur → **"Weiter"**
    - **"Jetzt installieren"** drücken.
3. Produktschlüssel:
    
    - Falls du keinen hast, wähle **"Ich habe keinen Product Key"**.
4. Edition auswählen:
    
    - Wähle z.B. **"Windows 11 Pro"** → **"Weiter"**.
        
    - Windows Pro oder Enterprise empfohlen
        
        (dann muss man nicht zwingend auf den IT-User zurück später)
        
5. Lizenz Bedingungen akzeptieren → **"Weiter"**.
    
6. Installationsart wählen:
    
    - **"Benutzerdefiniert: Nur Windows installieren (fortgeschritten)"**
7. Festplatte auswählen:
    
    - Die vorhin erstellte virtuelle Festplatte → **"Weiter"**.
8. Warte, bis die Installation abgeschlossen ist → PC neu starten lassen.
    

---

### 🎛️ **4. Windows 11 konfigurieren**

1. Richte Windows 11 ein wie gewohnt (Region, Sprache, Benutzerkonto).
    
2. **Integrationsdienste aktivieren** (für bessere Leistung):
    
    - Im Hyper-V-Manager → Rechtsklick auf die VM → **"Einstellungen..."** → Unter **"Integrationsdienste"** alle Optionen aktivieren.
3. Bildschirmauflösung anpassen:
    
    - Rechtsklick auf Desktop → **"Anzeigeeinstellungen"** → Auflösung einstellen.

---

## ✅ **Teil 3: Nützliche Einstellungen für die VM**

1. **Arbeitsspeicher anpassen**:
    
    - Hyper-V-Manager → Rechtsklick → **"Einstellungen..."** → Unter **"Arbeitsspeicher"** kann RAM angepasst werden.
2. **Prozessoranzahl erhöhen** (für bessere Leistung):
    
    - Gehe zu **"Prozessor"** → Erhöhe die **"Anzahl der virtuellen Prozessoren"**.
3. **Automatisches Starten aktivieren**:
    
    - **"Automatischer Start"** → Setze Häkchen bei **"Diese virtuelle Maschine automatisch starten, wenn der Dienst gestartet wird"**.

---

## ✅ **Teil 4: Netzwerkzugang für die VM einrichten**

1. **Virtuellen Switch erstellen**:
    
    - Hyper-V-Manager → Rechts im Fenster auf **"Virtueller Switch-Manager..."** klicken.
    - Wähle **"Neuer virtueller Netzwerk-Switch"** → **"Extern"** → Klicke auf **"Erstellen"**.
    - Name vergeben, z.B. **"Internet-Switch"** → Dein Netzwerkadapter auswählen → **"OK"**.
2. In den VM-Einstellungen den neuen Switch unter **"Netzwerkadapter"** auswählen.
    

---

## 🎯 **Fertig!**

Jetzt hast du Hyper-V aktiviert, eine Windows 11 VM installiert und korrekt konfiguriert. 

Wenn du irgendwo Probleme hast, melde dich im Discord! 🚀