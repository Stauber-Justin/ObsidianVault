# **SVERWEIS (VLOOKUP) in Excel – Umfassende Erklärung**

Der **SVERWEIS (engl. VLOOKUP)** ist eine der am häufigsten verwendeten Funktionen in Excel, um Werte aus einer Tabelle zu suchen und zurückzugeben. Diese Funktion gehört zu den Nachschlage- und Verweisfunktionen und ist besonders nützlich für Datenanalysen, Berichte oder Dashboards.

---

## **1. Syntax und Argumente von SVERWEIS**

Die grundlegende Schreibweise von SVERWEIS lautet:

```excel
=SVERWEIS(Suchkriterium; Matrix; Spaltenindex; [Bereich_Verweis])
```

**Erklärung der Argumente:**

- **Suchkriterium:** Der Wert, nach dem in der ersten Spalte der Matrix gesucht wird.
- **Matrix:** Der Bereich, in dem gesucht wird (erste Spalte = Suchspalte).
- **Spaltenindex:** Die Spalte in der Matrix, aus der der Wert zurückgegeben wird (beginnend bei 1).
- **[Bereich_Verweis] (optional):**
    - `WAHR` oder `1` → Ungefähre Übereinstimmung (Standardwert, falls weggelassen).
    - `FALSCH` oder `0` → Exakte Übereinstimmung.

---

## **2. Praxisbeispiel: SVERWEIS in einer Tabelle**

Angenommen, wir haben eine Tabelle mit Produktpreisen:

```
| Artikel-Nr. | Produkt | Preis (€) |
|------------|---------|-----------|
| 101        | Apfel   | 1,20      |
| 102        | Banane  | 0,90      |
| 103        | Orange  | 1,50      |
| 104        | Birne   | 1,10      |
```

Nun möchten wir mit der Artikel-Nr. den Preis abrufen:

```excel
=SVERWEIS(102; A2:C5; 3; FALSCH)
```

➡ **Ergebnis:** `0,90` (Preis der Banane)

---

## **3. Einsatzgebiete von SVERWEIS**

✅ **Häufige Anwendungsfälle:**

- Produktsuche (z. B. Preise abrufen).
- Mitarbeiterinformationen nach ID suchen.
- Kunden- oder Rechnungsdaten schnell abrufen.
- Automatisierung von Berichten oder Dashboards.

⚠ **Einschränkungen von SVERWEIS:**

- ❌ **Keine Links-Suche:** Kann nur nach rechts suchen.
- ❌ **Statische Spaltenindex-Nummer:** Ändert sich die Spaltenanordnung, bricht die Funktion.
- ❌ **Langsame Performance bei großen Datenmengen.**
- ❌ **Fehlende Fehlerbehandlung bei nicht vorhandenen Werten.**

---

## **4. Best Practices für SVERWEIS**

### **Dynamische Bereichsangabe mit Tabellen**

Statt `A2:C5` besser `Tabelle1[Produkte]` nutzen.

```excel
=SVERWEIS(102; Tabelle1[Produkte]; 3; FALSCH)
```

### **Fehlertolerante SVERWEIS-Funktion**

```excel
=WENNFEHLER(SVERWEIS(102; A2:C5; 3; FALSCH); "Nicht gefunden")
```

Verhindert `#NV`-Fehler, falls der Wert nicht existiert.

### **SVERWEIS mit mehreren Kriterien (Array-Formel)**

Falls zwei Werte abgeglichen werden sollen (z. B. Name + Datum), kann eine Hilfsspalte genutzt werden:

```excel
=SVERWEIS(A1&B1; A2:A5&B2:B5; 3; FALSCH)
```

**Hinweis:** **STRG + UMSCHALT + ENTER** für eine Array-Formel drücken.

---

## **5. SVERWEIS mit Error-Handling**

SVERWEIS kann fehlschlagen, wenn:

- Der gesuchte Wert nicht existiert (`#NV`-Fehler).
- Der Spaltenindex ungültig ist (`#WERT!`-Fehler).
- Der Bereichsverweis ungültig ist (`#NAME?`-Fehler).

### **Lösung: Verbesserte Fehlertoleranz**

#### **WENNFEHLER**

```excel
=WENNFEHLER(SVERWEIS(102; A2:C5; 3; FALSCH); "Nicht gefunden")
```

#### **WENNNV (speziell für #NV)**

```excel
=WENNNV(SVERWEIS(102; A2:C5; 3; FALSCH); "Nicht in der Liste")
```

---

## **6. Spezielle Vorteile & Nachteile von SVERWEIS**

### ✅ **Vorteile**

✔ Einfach und leicht verständlich.  
✔ Gut für kleine bis mittelgroße Datensätze.  
✔ Kompatibel mit allen Excel-Versionen.

### ❌ **Nachteile**

⛔ Kann nicht nach links suchen.  
⛔ Spaltennummer macht die Funktion fehleranfällig.  
⛔ Performance-Probleme bei sehr großen Tabellen.  
⛔ XVERWEIS ist in Excel 365 flexibler und leistungsfähiger.

---

## **7. Fazit & Empfehlung**

SVERWEIS ist eine solide Wahl für einfache Suchen, aber für bessere Effizienz und Flexibilität empfehle ich:

1. **XVERWEIS für moderne Excel-Versionen.**
2. **INDEX & VERGLEICH für ältere Versionen.**
3. **Dynamische Tabellen & Fehlerbehandlung nutzen.**