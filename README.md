# 🐍 Python Survival Kit & Scripting Toolbox

**Zweck:** All-in-One Cheat Sheet für IT-Systemelektroniker (Ausbildung & Praxis)
**Inhalt:** IT-05 Grundlagen + Real World Automation Tools
**Version:** 3.0 (Complete Edition)

---

## ⚡ 1. Die "Heilige Dreifaltigkeit" der Syntax

Wenn du diese Regeln brichst, startet das Skript nicht.

1.  **Einrückung (Indentation):** Python nutzt keine `{}` Klammern. Alles, was zu einer Schleife, Funktion oder If-Abfrage gehört, **muss eingerückt sein** (Tab oder 4 Leerzeichen).
2.  **Der Doppelpunkt (`:`):** Am Ende von Zeilen mit `if`, `else`, `elif`, `for`, `while`, `def`, `try` steht immer ein Doppelpunkt.
3.  **Case Sensitivity:** `True` ist nicht `true`. `Print` gibt es nicht, nur `print`.

---

## 📦 2. Variablen & Datentypen

Python erkennt Typen automatisch.

| Typ | Kürzel | Beschreibung | Beispiel | Wichtig |
| :--- | :--- | :--- | :--- | :--- |
| **String** | `str` | Text | `x = "Hallo"` | Immer in `" "` oder `' '` |
| **Integer** | `int` | Ganze Zahl | `x = 10` | Keine Anführungszeichen |
| **Float** | `float` | Kommazahl | `x = 10.5` | **Punkt** statt Komma! |
| **Boolean** | `bool` | Wahr/Falsch | `x = True` | Großschreibung beachten |

### Typ-Umwandlung (Casting)
Essenziell, da `input()` immer Text liefert.
```python
x = int("5")       # Text zu Ganzzahl (zum Rechnen)
y = str(10)        # Zahl zu Text (zum Zusammenfügen)
z = float("3.5")   # Text zu Kommazahl
```

---

## 💬 3. Input & Output

### F-Strings (Der Standard für Ausgaben)
Vergiss das Zusammenkleben mit `+`. Nutze `f""`.
```python
user = "Admin"
id = 42
# Variablen werden direkt in den geschweiften Klammern eingesetzt/berechnet
print(f"User: {user} (ID: {id + 100})") 
```

### Eingabe
```python
# Achtung: input gibt IMMER einen String zurück!
eingabe = input("Gib eine Zahl ein: ")
zahl = int(eingabe) # Sofort umwandeln, wenn du rechnen willst!
```

---

## 🛠 4. String-Manipulation (Text-Werkzeuge)

Wichtig für Dateinamen und User-Eingaben.

```python
text = "  Bild.JPG  "

# 1. Säubern
sauber = text.strip()  # Entfernt Leerzeichen außen -> "Bild.JPG"

# 2. Vergleichen (Alles klein machen)
if sauber.lower() == "bild.jpg":
    print("Gefunden!")

# 3. Suchen / Prüfen
datei = "rechnung_2023.pdf"

if datei.endswith(".pdf"):
    print("Ist ein Dokument.")

if datei.startswith("rechnung"):
    print("Ist eine Rechnung.")

if "2023" in datei:
    print("Ist aus diesem Jahr.")

# 4. Ersetzen
neu = datei.replace("rechnung", "invoice") # -> "invoice_2023.pdf"
```

---

## 🧳 5. Listen (Container)

Dein Sammelbehälter für Daten (z.B. Dateilisten).

```python
# Erstellen
dateien = ["setup.exe", "bild.png", "doku.txt"]

# Zugriff (Index startet bei 0!)
erste = dateien[0]     # "setup.exe"
letzte = dateien[-1]   # "-1" holt immer das allerletzte Element

# Bearbeiten
dateien.append("neu.pdf")    # Hinzufügen am Ende
dateien.remove("setup.exe")  # Löschen eines Elements

# Checken
if "virus.exe" not in dateien:
    print("Liste ist sauber.")

# Anzahl messen
anzahl = len(dateien)  # Gibt 3 zurück
```

---

## 🧮 6. Operatoren & Logik

### Mathe
| Symbol | Funktion | Beispiel |
| :--- | :--- | :--- |
| `+` `-` `*` `/` | Grundrechenarten | `10 * 5` |
| `%` | **Modulo** (Restwert) | `10 % 3` ergibt `1` (Wichtig für "gerade/ungerade") |
| `**` | Potenz (Hoch) | `2 ** 3` ist 8 |
| `+=` | Schnell-Addieren | `x += 1` (statt `x = x + 1`) |

### Vergleich & Logik
| Symbol | Bedeutung |
| :--- | :--- |
| `==` | Ist gleich? (Doppeltes Zeichen!) |
| `!=` | Ist Ungleich? |
| `and` | UND (Beides muss wahr sein) |
| `or` | ODER (Eins muss wahr sein) |
| `not` | NICHT (Dreht Wahr zu Falsch) |

---

## 🔀 7. Kontrollstrukturen (If / Else)

```python
status = "Admin"
level = 2

if status == "Admin" and level > 1:
    print("Voller Zugriff")
elif status == "User":
    print("Eingeschränkter Zugriff") # Nur wenn das erste IF falsch war
else:
    print("Zugriff verweigert")      # Wenn gar nichts zutraf
```

---

## 🔄 8. Schleifen (Loops)

### For-Schleife (Listen oder feste Anzahl)
```python
# Variante A: Liste durchgehen
items = ["A", "B", "C"]
for ding in items:
    print(f"Verarbeite: {ding}")

# Variante B: Zahlenreihe (Start, Ende_Exklusive)
for i in range(1, 4):
    print(f"Nr. {i}") # Druckt 1, 2, 3
```

### While-Schleife (Solange Bedingung wahr)
```python
# Achtung: Endlosschleife vermeiden!
batterie = 10
while batterie > 0:
    print("Läuft...")
    batterie -= 1  # Zustand ändern!
```

### Steuerung
* `break`: Bricht die Schleife sofort komplett ab.
* `continue`: Springt sofort zum nächsten Durchlauf (überspringt den Rest unten).

---

## ⚙️ 9. Funktionen

Code wiederverwenden statt kopieren.

```python
# Definition (Bauplan)
def berechne_watt(volt, ampere):
    return volt * ampere

# Aufruf (Benutzung)
leistung = berechne_watt(230, 16)
print(f"Ergebnis: {leistung} Watt")
```

---

## 💻 10. System & Dateien (OS Modul)

**Das Herzstück für IT-Elektroniker-Skripte.**

```python
import os
import shutil
import time

# Wo bin ich?
cwd = os.getcwd()

# Was ist im Ordner "Downloads"? (Gibt Liste zurück)
dateien = os.listdir("C:/Users/Name/Downloads")

# Existiert eine Datei/Ordner?
if os.path.exists("C:/WichtigeDatei.txt"):
    print("Gefunden!")

# Ordner erstellen (exist_ok=True verhindert Crash, wenn Ordner schon da ist)
os.makedirs("C:/Backups/NeuerOrdner", exist_ok=True)

# Datei verschieben
# shutil.move("Quelle", "Ziel")
# shutil.move("bild.jpg", "C:/Bilder/bild.jpg")

# Warten
time.sleep(5) # 5 Sekunden Pause
```

---

## 📝 11. Dateien Lesen & Schreiben

Nutze `with open(...)`, damit Python die Datei danach automatisch schließt.

```python
# Schreiben ("w" = überschreiben, "a" = anhängen)
with open("log.txt", "a") as f:
    f.write("Systemstart erfolgreich.\n") # \n = Neue Zeile

# Lesen ("r" = read)
with open("log.txt", "r") as f:
    inhalt = f.read()
    print(inhalt)
```

---

## 🛡️ 12. Fehlerbehandlung (Try / Except)

Verhindert Programmabstürze.

```python
try:
    zahl = int(input("Teiler: "))
    print(100 / zahl)
except ValueError:
    print("Keine Zahl eingegeben!")
except ZeroDivisionError:
    print("Nicht durch Null teilen!")
except Exception as e:
    print(f"Unbekannter Fehler: {e}")
```

---

## ✅ Debugging-Checkliste

Wenn der Code rot leuchtet oder nicht geht:

1.  [ ] **Doppelpunkte** (`:`) am Zeilenende vergessen?
2.  [ ] **Einrückung** (Tab vs. Space) vermischt oder falsch?
3.  [ ] `input()` vergessen in `int()` umzuwandeln?
4.  [ ] Variable falsch geschrieben (Tippfehler)?
5.  [ ] String vergessen zu schließen (`"Hallo`)?
6.  [ ] Vergleich mit `=` statt `==` gemacht?
