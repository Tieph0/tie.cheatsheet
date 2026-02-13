# 🧰 IT-05 Python Survival Kit (Sachsen)

Dieses Cheat Sheet deckt die Grundlagen für das Lernfeld **IT-05 (Software zur Verwaltung von Daten anpassen)** ab. Es ist optimiert für den Einstieg (1. & 2. Lehrjahr) und fokussiert sich auf Logik, Syntax und Fehlervermeidung.

---

## ⚠️ Die Goldenen Syntax-Regeln

1.  **Einrückung ist Gesetz:** Python nutzt keine geschweiften Klammern `{}`. Alles, was zu einer Schleife oder Funktion gehört, muss eingerückt sein (Tab oder 4 Leerzeichen).
2.  **Der Doppelpunkt:** Nach `if`, `else`, `elif`, `for`, `while` und `def` muss **immer** ein Doppelpunkt (`:`) stehen.
3.  **Groß-/Kleinschreibung:** `True` ist nicht das Gleiche wie `true`. Python unterscheidet genau!

---

## 📦 1. Variablen & Datentypen

| Typ | Fachbegriff | Syntax-Beispiel | Wichtiges |
| :--- | :--- | :--- | :--- |
| **Text** | `String` (str) | `name = "Max"` | Immer in `" "` oder `' '` setzen. |
| **Ganzzahl** | `Integer` (int) | `alter = 18` | Keine Anführungszeichen. |
| **Kommazahl** | `Float` | `preis = 9.99` | **Punkt** statt Komma nutzen! |
| **Logisch** | `Boolean` | `status = True` | Großschreibung beachten (`True`/`False`). |

### Typ-Umwandlung (Casting)
```python
x = int("5")    # Macht aus Text "5" die Zahl 5 (zum Rechnen)
y = str(5)      # Macht aus Zahl 5 den Text "5" (zum Anzeigen)
z = float("3.5") # Umwandlung in Kommazahl
