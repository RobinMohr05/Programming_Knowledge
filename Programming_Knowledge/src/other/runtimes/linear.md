
# **KOMPLETT CHATGPT GENERIERT**

**Lineare Laufzeit** (in der Informatik mit **O(n)** bezeichnet) beschreibt, wie die **Laufzeit** eines Algorithmus **proportional zur Größe der Eingabe** wächst.

---

### Was bedeutet das genau?

Wenn ein Algorithmus eine lineare Laufzeit hat, dann gilt:

> **Wenn du doppelt so viele Elemente hast, brauchst du ungefähr doppelt so lange.**

---

### Beispiel:

Nehmen wir an, du hast eine Liste mit 10 Zahlen und suchst eine bestimmte Zahl mithilfe **linearer Suche**:

```python
def lineare_suche(liste, ziel):
    for zahl in liste:
        if zahl == ziel:
            return True
    return False
```

- Wenn die Liste **10 Elemente** hat, dauert es im schlimmsten Fall **10 Vergleiche**.
    
- Hat die Liste **1.000 Elemente**, sind es im schlimmsten Fall **1.000 Vergleiche**.
    

Daher: Die Laufzeit wächst **direkt proportional** mit der Eingabelänge — das ist **lineare Laufzeit**.

---

### Mathematisch:

- nn = Anzahl der Elemente (Eingabegröße)
    
- Aufwand = c⋅nc \cdot n (für irgendeine Konstante cc)  
    → Daraus wird in der Landau-Notation: **O(n)O(n)**
    

---

### Vergleich zu anderen Laufzeiten:

|Laufzeit|Beschreibung|Beispielalgorithmus|
|---|---|---|
|O(1)O(1)|Konstante Laufzeit (unabhängig von nn)|Zugriff auf Array-Element|
|O(n)O(n)|Linear – wächst direkt mit nn|Lineare Suche|
|O(n2)O(n^2)|Quadratisch – sehr viel langsamer bei großem nn|Bubble Sort|
|O(log⁡n)O(\log n)|Logarithmisch – sehr effizient|Binäre Suche|

