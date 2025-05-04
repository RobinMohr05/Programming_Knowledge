
# **KOMPLETT CHATGPT GENERIERT**

In der Informatik beschreibt die **Laufzeit** (oder auch Zeitkomplexität) den **zeitlichen Aufwand**, den ein Algorithmus benötigt, um ein Problem in Abhängigkeit von der Eingabemenge zu lösen. Man analysiert also, **wie schnell oder langsam ein Algorithmus wächst**, wenn die Eingabe größer wird.

---

### 1. **Was ist die Laufzeit eines Algorithmus?**

Die Laufzeit ist ein Maß dafür, **wie viele Schritte oder Operationen** ein Algorithmus im schlimmsten, besten oder durchschnittlichen Fall benötigt.

---

### 2. **Komplexitätsklassen (mit Beispielen)**

| Bezeichnung            | Schreibweise | Beispielhafte Laufzeit bei n=1000n = 1000 | Erklärung                                   |
| ---------------------- | ------------ | ----------------------------------------- | ------------------------------------------- |
| **Konstant**           | O(1)         | 1 Schritt                                 | Immer gleich, egal wie groß die Eingabe ist |
| **Logarithmisch**      | O(log⁡n)     | ~10 Schritte                              | Typisch für binäre Suche                    |
| **[[linear\|Linear]]** | O(n)         | 1000 Schritte                             | Z.B. eine Schleife über alle Elemente       |
| **Linear-log.**        | O(nlog⁡n)    | ~10.000 Schritte                          | Z.B. Mergesort oder Heapsort                |
| **Quadratisch**        | O(n2)        | 1.000.000 Schritte                        | Z.B. doppelte Schleifen (Bubble Sort)       |
| **Kubisch**            | O(n3)        | 1 Milliarde Schritte                      | Z.B. 3-fach geschachtelte Schleifen         |
| **Exponential**        | O(2n)        | gigantisch bei n=100n = 100               | Z.B. Brute-Force-Lösungen                   |
| **Fakultativ**         | O(n!)        | noch schlimmer als exponentiell           | Z.B. das Traveling Salesman Problem (TSP)   |

---

### 3. **Best Case, Worst Case, Average Case**

- **Best Case**: Günstigste Laufzeit bei optimaler Eingabe.
    
- **Worst Case**: Schlechtester Fall, auf den man sich verlassen muss.
    
- **Average Case**: Erwarteter Aufwand bei zufälliger Eingabe.
    

---

### 4. **Warum ist das wichtig?**

Die Analyse hilft, **effiziente Algorithmen** zu finden, **Skalierbarkeit zu beurteilen**, und Systeme zu planen, die auch bei großen Datenmengen noch performant arbeiten.

