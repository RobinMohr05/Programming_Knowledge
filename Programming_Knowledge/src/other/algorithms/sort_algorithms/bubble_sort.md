**Bubble Sort** ist ein einfacher [[sort_algorithms_main|Sortieralgorithmus]], der eine Liste sortiert, indem er wiederholt benachbarte Elemente von links nach rechts vergleicht und vertauscht, falls das linke Element größer ist als das rechte.  
Dieser Vorgang wird so oft wiederholt, bis die Liste vollständig sortiert ist.  
Mit jedem Durchlauf wandert das jeweils größte verbleibende Element an seine endgültige Position, sodass am Ende jeder Runde ein Element weniger betrachtet werden muss.

Beispiel in einem [[activity_diagramm|Aktivitätsdiagramm]]:

![[bubblesort_ad.png]]

Beispiel in [[python_main|Python]] Code:
```python
def bubble_sort(liste):
    n = len(liste)
    for i in range(n):
        # Letztes i-Element ist bereits sortiert
        for j in range(0, n - i - 1):
            if liste[j] > liste[j + 1]:
                # Vertausche die Elemente, wenn sie in der falschen Reihenfolge sind
                liste[j], liste[j + 1] = liste[j + 1], liste[j]
    return liste
    
liste = [5, 3, 8, 4, 2]
liste = bubble_sort(liste)
print("Sortierte Liste:", liste)
```

Beispiel **rekursiv** in [[python_main|Python]] Code:

```python
def bubble_sort_recursive(arr, n=None):
    if n is None:
        n = len(arr)
    
    # Basisfall: Wenn nur noch ein Element übrig ist, ist die Liste sortiert
    if n == 1:
        return

    # Ein Durchgang der Bubble-Sort-Schleife
    for i in range(n - 1):
        if arr[i] > arr[i + 1]:
            # Tausche benachbarte Elemente, wenn sie in falscher Reihenfolge sind
            arr[i], arr[i + 1] = arr[i + 1], arr[i]
    
    # Rekursiver Aufruf für die unsortierten ersten n-1 Elemente
    bubble_sort_recursive(arr, n - 1)

# Beispiel
liste = [5, 3, 8, 4, 2]
liste = bubble_sort_recursive(liste)
print("Sortierte Liste:", liste)

```
### Beispiel:

Nehmen wir an, wir haben eine unsortierte Liste:

`[5, 3, 8, 4, 2]`

1. Im ersten Durchgang vergleichen wir 5 und 3, 5 ist größer, also tauschen wir sie:  
    `[3, 5, 8, 4, 2]`
    
    Dann vergleichen wir 5 und 8, keine Änderung, und schließlich 8 und 4, tauschen:  
    `[3, 5, 4, 8, 2]`
    
    Schließlich vergleichen wir 8 und 2, tauschen:  
    `[3, 5, 4, 2, 8]`
    
    Am Ende des ersten Durchgangs ist das größte Element (8) an seinem richtigen Platz.
    
2. Im zweiten Durchgang vergleichen wir wieder benachbarte Elemente:  
    `[3, 5, 4, 2]` → `[3, 4, 5, 2]` → `[3, 4, 2, 5]` → `[3, 2, 4, 5]`
    
    Jetzt ist 5 an seinem richtigen Platz.
    
3. Der dritte Durchgang wird ähnlich fortgesetzt, und nach mehreren Durchgängen ist die Liste vollständig sortiert:  
    `[2, 3, 4, 5, 8]`
    
### Vor- und Nachteile:

**Vorteile:**

- Einfach zu implementieren.
    
- Stabile Sortierung: Die Reihenfolge von gleichwertigen Elementen bleibt erhalten.
    

**Nachteile:**

- Ineffizient bei großen Listen, da die Zeitkomplexität im schlimmsten Fall quadratisch ist.
    
- Nicht der schnellste Algorithmus im Vergleich zu anderen Sortieralgorithmen wie Quick Sort oder Merge Sort.

**Bubble Sort** ist ein einfacher [[sort_algorithms_main|Sortieralgorithmus]], der eine Liste sortiert, indem er wiederholt benachbarte Elemente von links nach rechts vergleicht und vertauscht, falls das linke Element größer ist als das rechte.  
Dieser Vorgang wird so oft wiederholt, bis die Liste vollständig sortiert ist.  
Mit jedem Durchlauf wandert das jeweils größte noch nicht sortierte Element an seine endgültige Position, sodass am Ende jeder Runde ein Element weniger betrachtet werden muss.

Beispiel in einem [[activity_diagramm|Aktivitätsdiagramm]]:

![[bubblesort_ad.png]]

### Beispiel in [[python_main|Python]]:

```python
def bubble_sort(liste):
    n = len(liste)
    for i in range(n):
        # Das letzte i-Element ist bereits sortiert
        for j in range(0, n - i - 1):
            if liste[j] > liste[j + 1]:
                # Vertausche Elemente, wenn sie in der falschen Reihenfolge sind
                liste[j], liste[j + 1] = liste[j + 1], liste[j]
    return liste

liste = [5, 3, 8, 4, 2]
liste = bubble_sort(liste)
print("Sortierte Liste:", liste)
```

### Rekursive Variante in [[python_main|Python]]:

```python
def bubble_sort_recursive(arr, n=None):
    if n is None:
        n = len(arr)

    # Basisfall: Liste mit nur einem Element ist sortiert
    if n == 1:
        return

    # Ein Durchgang der Bubble-Sort-Schleife
    for i in range(n - 1):
        if arr[i] > arr[i + 1]:
            arr[i], arr[i + 1] = arr[i + 1], arr[i]

    # Rekursiver Aufruf für die restlichen Elemente
    bubble_sort_recursive(arr, n - 1)

# Beispiel
liste = [5, 3, 8, 4, 2]
liste = bubble_sort_recursive(liste)
print("Sortierte Liste:", liste)
```

### Beispiel – Schrittweise Erklärung:

Gegeben sei die unsortierte Liste:  
`[5, 3, 8, 4, 2]`

1. **Erster Durchgang:**  
    `[5, 3] → [3, 5]`  
    `[5, 8] → bleibt`  
    `[8, 4] → [4, 8]`  
    `[8, 2] → [2, 8]`  
    Ergebnis: `[3, 5, 4, 2, 8]`
    
2. **Zweiter Durchgang:**  
    `[3, 5] → bleibt`  
    `[5, 4] → [4, 5]`  
    `[5, 2] → [2, 5]`  
    Ergebnis: `[3, 4, 2, 5, 8]`
    
3. Weitere Durchgänge folgen, bis die Liste vollständig sortiert ist:  
    `[2, 3, 4, 5, 8]`
    

### Vor- und Nachteile:

**Vorteile:**
- Einfach zu verstehen und zu implementieren
- **Stabile Sortierung**: Die Reihenfolge gleichwertiger Elemente bleibt erhalten

**Nachteile:**
- Sehr ineffizient bei großen Datenmengen ([[runtimes_main|Laufzeit: O(n²)]])
- Wird in der Praxis selten verwendet, da leistungsfähigere Algorithmen existieren (z. B. Quick Sort, Merge Sort)