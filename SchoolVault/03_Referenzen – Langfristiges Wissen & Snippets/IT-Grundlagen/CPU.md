# 📌 CPU (Central Processing Unit) – Lernnotiz

#ChatGPT #Hardware #Informatik #CPU #Computerarchitektur

## Überblick

Die **Central Processing Unit (CPU)**, häufig auch als **Prozessor** bezeichnet, ist das **zentrale Rechenwerk** eines Computers. Sie wird oft als das **„Gehirn“** des Computers bezeichnet, da sie sämtliche grundlegenden Operationen durchführt, die für die Ausführung von Programmen notwendig sind.

Ihre Hauptaufgaben umfassen:

> [!info] **Kernfunktionen der CPU**
> 
> - **Ausführen von Anweisungen** im [[03_Referenzen – Langfristiges Wissen & Snippets/IT-Fachwissen/Maschinensprache|Maschinencode]]
> - **Verarbeitung von Daten**
> - **Treffen von Entscheidungen** basierend auf Programmlogik
> - **Liefern von Ergebnissen**

Die CPU arbeitet in einem zyklischen Ablauf:

1. **Fetch**: Abrufen einer Anweisung aus dem Speicher.
2. **Decode**: Übersetzen der Anweisung in maschinenlesbare Signale.
3. **Execute**: Ausführung der Anweisung.

## Details & Analyse

### 🔍 Wichtige Merkmale der CPU

- **Taktfrequenz (Clock Speed):** Gibt an, wie viele Zyklen pro Sekunde die CPU ausführen kann (gemessen in **Gigahertz (GHz)**). Eine höhere Frequenz bedeutet eine theoretisch schnellere Verarbeitung.
    
- **Kerne (Cores):** Moderne Prozessoren verfügen über mehrere **Kerne** (z. B. **Dual(2)-, Quad(4)-, Octa(8)-Core**), die gleichzeitig verschiedene Aufgaben ausführen können (**Parallelverarbeitung**).
    
- **Threads:** Ein **Thread** ist eine Abfolge von Befehlen, die eine CPU verarbeiten kann. Dank Technologien wie **Hyper-Threading** können mehrere Threads pro Kern verarbeitet werden.
    
- **Cache:** Ein schneller Zwischenspeicher, der häufig benötigte Daten speichert, um den Zugriff auf den Arbeitsspeicher zu reduzieren.
    
- **Instruction Set Architecture (ISA):** Definiert die Befehlssätze, die die CPU versteht, z. B. **x86**, **ARM** oder **RISC-V**.
    
- **Arithmetic Logic Unit (ALU):** Führt mathematische und logische Operationen aus.
    
- **Control Unit (CU):** Steuert den Datenfluss innerhalb der CPU und koordiniert die Ausführung von Befehlen.
    

### 📖 Relevante Theorien & Modelle

> [!tip] **Architekturmodelle**

- **Von-Neumann-Architektur:**
    
    - Gemeinsamer Speicher für Daten und Programme.
    - Besteht aus Steuerwerk, Rechenwerk, Speicher und Ein-/Ausgabegeräten.
    - Standardmodell moderner Prozessoren.
- **Harvard-Architektur:**
    
    - Trennung von Befehls- und Datenspeicher.
    - Erlaubt parallelen Zugriff auf Anweisungen und Daten.

> [!info] **Gesetzmäßigkeit der technologischen Entwicklung**
> 
> - **Moore’s Law:**
>     - Prognostiziert, dass sich die Anzahl der Transistoren auf einem Mikrochip etwa alle zwei Jahre verdoppelt.
>     - Dies führt zu einer stetigen Steigerung der Rechenleistung.

## Anwendung & Beispiele

- **Alltägliche Anwendungen:**
    
    - Steuerung von Funktionen in **Smartphones**, **Computern** und **Tablets** (z. B. App-Start, Datenverarbeitung).
- **Gaming:**
    
    - Hochleistungsfähige CPUs sorgen für flüssige Bildraten und bessere Performance.
- **Künstliche Intelligenz:**
    
    - Einsatz moderner CPUs in Kombination mit **GPUs** oder **TPUs** zur Beschleunigung von **maschinellem Lernen** und **Datenanalysen**.
- **Server & Cloud-Computing:**
    
    - Leistungsstarke Multi-Core-CPUs verarbeiten große Datenmengen in Rechenzentren für Webdienste.

## Verknüpfte Notizen

- [[Von-Neumann-Architektur]]
- [[Harvard-Architektur]]
- [[Parallelverarbeitung]]
- [[Moore's Law]]

## Fazit & nächste Schritte

Die **CPU** ist das Herzstück eines jeden Computers, das alle wichtigen Rechenoperationen steuert. Ihre Leistungsfähigkeit wird durch mehrere Faktoren beeinflusst, darunter die **Anzahl der Kerne**, die **Taktfrequenz**, der **Cache** sowie die zugrunde liegende **Architektur**.

> [!summary] **Wichtige Erkenntnisse**
> 
> - Die CPU ist für die Ausführung von Programmen essenziell.
> - Moderne CPUs nutzen Parallelverarbeitung, um effizienter zu arbeiten.
> - Architekturen wie die **Von-Neumann-** oder **Harvard-Architektur** bestimmen, wie effizient Befehle verarbeitet werden.

**Nächste Schritte:**

- Weiterführende Notizen zu spezifischen CPU-Architekturen erstellen.
- Leistungskennzahlen von CPUs in verschiedenen Anwendungsbereichen vergleichen.