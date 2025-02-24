# Excel EK – Grundlagen & Funktionen

## ✨ Überblick

Diese Notiz bietet eine kompakte Übersicht über essenzielle Excel-Funktionen und Formatierungsoptionen. Sie richtet sich an Anwender, die ihre Kenntnisse vertiefen und ihre Effizienz steigern möchten.

---

## 🔧 Formatierung

### **Allgemeine Zellformatierung**

> [!info] **Zellen formatieren**
> 
> - **Markieren** der zu formatierenden Zellen
> - **Rechtsklick** > "Zellen formatieren"
> - Alternativ: **Start** > "Zahl" > **Knubbelmenü**

**Wichtiger Hinweis:** Text in Zahlenformaten muss in **""** gesetzt werden. Beispiel: `0 "Kg"` ergibt **0 Kg**.

### **Drucken auf DIN A4**

> [!tip] **Seitenlayout anpassen**
> 
> 1. **Seitenlayout**
> 2. "An Format anpassen"
> 3. **Breite: 1 Seite**, **Höhe: 1 Seite**

### **Gitternetzlinien anzeigen**

> [!example] **Aktivieren der Gitternetzlinien**
> 
> - **Ansicht** > "Anzeigen" > **Gitternetzlinien**

---

## 📊 Diagramme erstellen

> [!info] **Schritt-für-Schritt Anleitung**
> 
> 1. **Achse markieren**
> 2. **Datenreihen wählen**
> 3. **Einfügen** > Diagrammtyp auswählen
> 4. Diagramm anpassen über:
>     - **Rechtes Menü**
>     - **Reiter "Diagrammentwurf"**

---

## 🔎 Suchen & Ersetzen

> [!tip] **Falsche Eingaben korrigieren**
> 
> - **Start** > "Suchen & Ersetzen"
> - Erweiterte Optionen: ">>Erweitern" zum Format-Ändern
> - **Tipp:** Auf exakte Schreibweise achten!

---

## 🛠️ Bedingte Formatierung

> [!warning] **Dynamische Formatierung aktivieren**
> 
> - **Start** > "Formatvorlagen" > "Bedingte Formatierung"
> - **Neue Regel** anlegen, z. B.:
>     - **Kleinste/größte Werte hervorheben**
>     - **Werte farblich unterscheiden**

---

## ⚙️ Wichtige Excel-Funktionen

|Funktion|Beschreibung|
|---|---|
|`RUNDEN(Zahl; Stellen)`|Rundet auf X Dezimalstellen|
|`ABRUNDEN(Zahl; Stellen)`|Rundet immer ab|
|`AUFRUNDEN(Zahl; Stellen)`|Rundet immer auf|
|`GANZZAHL(Zahl)`|Gibt die nächstkleinere ganze Zahl zurück|
|`SUMME(Bereich)`|Addiert Werte in einem Bereich|
|`MAX(Bereich)`|Gibt den größten Wert zurück|
|`MITTELWERT(Bereich)`|Berechnet den Durchschnitt|
|`WENN(Bedingung; Wahr; Falsch)`|Logische Bedingungsprüfung|
|`UND(Bed1; Bed2)`|Prüft, ob **alle** Bedingungen wahr sind|
|`ODER(Bed1; Bed2)`|Prüft, ob **eine** Bedingung wahr ist|
|`ABS(Zahl)`|Gibt den absoluten Wert zurück|
|`WENNNV(Wert; Ersatz)`|Ersetzt **#NV** durch einen definierten Wert|
|`WENNFEHLER(Wert; Ersatz)`|Ersetzt Fehler durch definierten Wert|
|`RANG.GLEICH(Zahl; Bezug; Ordnung)`|Gibt den Rang einer Zahl zurück|

---

## 💡 Erweiterte Funktionen

### **Datenvalidierung (Dropdown-Listen)**

> [!tip] **Erstellung einer Dropdown-Liste**
> 
> - **Zelle markieren**
> - **Daten** > "Datenüberprüfung"
> - **Kriterium: Liste** definieren
> - Werte manuell eingeben oder Zellbereich referenzieren

### **Zählen & Summieren mit Bedingungen**

|Funktion|Beschreibung|
|---|---|
|`ZÄHLENWENN(Bereich; Kriterium)`|Zählt Zellen nach Kriterium|
|`SUMMEWENN(Bereich; Kriterium; Summe_Bereich)`|Summiert Werte nach Kriterium|

### **SVERWEIS** (Vertikaler Verweis)

> [!example] **Syntax:** `SVERWEIS(Suchwert; Tabelle; Spaltenindex; [WAHR/FALSCH])`
> 
> - **Suchwert**: Der zu findende Wert
> - **Tabelle**: Der Zellbereich, in dem gesucht wird
> - **Spaltenindex**: Die Spalte, aus der der Wert zurückgegeben wird
> - **WAHR** = ungefähre Übereinstimmung, **FALSCH** = exakte Übereinstimmung

### **Fehlerabfrage mit WENNFEHLER**

```excel
=WENNFEHLER(SVERWEIS(A1; Tabelle; 2; FALSCH); "Nicht gefunden")
```

> [!warning] **Vermeidung von Fehlerwerten** Falls der SVERWEIS fehlschlägt, gibt die Funktion stattdessen "Nicht gefunden" zurück.

---

## 📍 Verknüpfte Notizen

- [[Excel Fortgeschrittene Funktionen]]
- [[Pivot-Tabellen in Excel]]
- [[Datenvisualisierung in Excel]]

---

## 🔄 Fazit & Nächste Schritte

Diese Notiz bietet eine schnelle Referenz für grundlegende und erweiterte Excel-Funktionen. Für eine tiefere Einarbeitung empfiehlt es sich, spezifische Anwendungsfälle in [[Excel Fortgeschrittene Funktionen]] nachzuschlagen oder durch praktische Übungen zu vertiefen.

**Nächste Schritte:**

- Teste die beschriebenen Funktionen an eigenen Daten
- Erstelle eigene Vorlagen für wiederkehrende Berechnungen
- Erkunde fortgeschrittene Excel-Funktionen wie Power Query & VBA

---

> [!success] **Excel meistern!** Mit diesen Grundlagen kannst du Excel effizient nutzen und deine Arbeitsprozesse optimieren!