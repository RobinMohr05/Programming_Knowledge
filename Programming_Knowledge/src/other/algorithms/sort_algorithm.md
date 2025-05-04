buble sort

# **KOMPLETT CHATGPT GENERIERT**

**Bubble Sort** ist ein einfacher Sortieralgorithmus, der wiederholt benachbarte Elemente in einer Liste vergleicht und vertauscht, falls sie in der falschen Reihenfolge stehen. Dies geschieht, bis die Liste vollständig sortiert ist.

### Funktionsweise von Bubble Sort:

1. **Vergleiche benachbarte Elemente**: Beginne beim ersten Element der Liste und vergleiche es mit dem nächsten Element.
    
2. **Vertauschen, wenn notwendig**: Wenn das erste Element größer als das zweite ist, tausche sie.
    
3. **Wiederhole den Vorgang**: Fahre mit den benachbarten Elementen fort, bis das Ende der Liste erreicht ist.
    
4. **Wiederhole den gesamten Prozess**: Wiederhole diesen Vorgang für die gesamte Liste, jedoch bei jedem Durchlauf das "größte" Element nach hinten verschiebend. Dadurch wird die Liste nach und nach sortiert.
    

Der Algorithmus "blubbert" sozusagen das größte Element am Ende der Liste nach oben, was ihm seinen Namen gibt.

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
    

### Pseudocode für Bubble Sort:

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
```

### Komplexität:

- **Worst-Case (unsortierte Liste)**: O(n2)O(n^2), weil wir in jedem Durchgang alle nn Elemente vergleichen müssen und das für nn Durchgänge.
    
- **Best-Case (bereits sortierte Liste)**: O(n)O(n), da der Algorithmus durch eine zusätzliche Optimierung (z. B. "Flagge", die überprüft, ob im Durchgang keine Vertauschungen vorgenommen wurden) erkennen kann, dass die Liste bereits sortiert ist.
    
- **Durchschnittlicher Fall**: O(n2)O(n^2).
    

### Vor- und Nachteile:

**Vorteile:**

- Einfach zu implementieren.
    
- Stabile Sortierung: Die Reihenfolge von gleichwertigen Elementen bleibt erhalten.
    

**Nachteile:**

- Ineffizient bei großen Listen, da die Zeitkomplexität im schlimmsten Fall quadratisch ist.
    
- Nicht der schnellste Algorithmus im Vergleich zu anderen Sortieralgorithmen wie Quick Sort oder Merge Sort.
    

**Wann sollte man Bubble Sort verwenden?**

- Für kleine Listen oder wenn die Einfachheit des Algorithmus wichtiger ist als die Effizienz.
    
- In der Praxis wird Bubble Sort selten verwendet, da er für größere Datenmengen sehr langsam ist.