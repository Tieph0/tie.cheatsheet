# 📘 IT-Systemelektroniker: Python Survival Kit (IT-05)

**Version:** 1.0  
**Fokus:** Lernfeld 5 (Grundlagen der Programmierung)  
**Status:** 1. & 2. Lehrjahr (Ohne Arrays)

Dieses Dokument dient als Nachschlagewerk (Cheat Sheet) für die absoluten Grundlagen der prozeduralen Programmierung mit Python.

---

## ⚡ 1. Die Goldenen Regeln (Syntax)

Python ist sehr strikt, was die Form angeht. Wenn du diese drei Regeln brichst, läuft nichts.

1.  **Einrückung ist Pflicht:** Python nutzt keine Klammern `{}` für Code-Blöcke. Alles, was zu einer Bedingung oder Schleife gehört, muss **eingerückt** sein (Taste `Tab` oder 4 Leertasten).
2.  **Der Doppelpunkt:** Am Ende von Zeilen mit `if`, `else`, `elif`, `while`, `for`, `def` steht immer ein Doppelpunkt `:`.
3.  **Groß-/Kleinschreibung:** `print` ist nicht `Print`. `True` ist nicht `true`.

---

## 📦 2. Variablen & Datentypen

Variablen sind Speicherplätze ("Kartons"). In Python musst du den Typ nicht extra ansagen, Python erkennt ihn automatisch.

| Datentyp | Kürzel | Beschreibung | Beispiel-Code | Wichtiger Hinweis |
| :--- | :--- | :--- | :--- | :--- |
| **String** | `str` | Textzeichenkette | `name = "Admin"` | Muss in `" "` oder `' '` stehen. |
| **Integer** | `int` | Ganze Zahl | `spannung = 230` | Keine Anführungszeichen! |
| **Float** | `float` | Gleitkommazahl | `strom = 0.5` | **Punkt** statt Komma nutzen! |
| **Boolean** | `bool` | Wahrheitswert | `ist_aktiv = True` | Nur `True` oder `False`. |

### 🛠 Typ-Umwandlung (Casting)
Oft hast du den falschen Typ (z.B. Text aus einer Eingabe), brauchst aber eine Zahl zum Rechnen.

```python
x = "10"          # Das ist Text (String)
y = int(x)        # Umwandlung in Ganzzahl (Rechnen möglich)
z = float("5.5")  # Umwandlung in Kommazahl
s = str(100)      # Umwandlung von Zahl zurück in Text
