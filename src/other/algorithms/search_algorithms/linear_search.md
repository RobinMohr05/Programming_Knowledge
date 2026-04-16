Die lineare Suche ist ein [[search_algorithms_main|Suchalgorithmus]], der versucht ein Element in einer Liste oder einem Array mit **n** Elementen zu finden, indem er die Liste Element für Element durchgeht, bis man es gefunden hat.

**Funktionsweise**:

- Beginne beim ersten Element und vergleiche es mit dem gesuchten Wert.
	
- Wenn es nicht übereinstimmt, gehe zum nächsten Element und wiederhole den Vorgang.
	
- Dies wird fortgesetzt, bis das Element gefunden wird oder das Ende der Liste erreicht ist.

**Vorteil**: Einfach zu implementieren und funktioniert auch mit unsortierten Listen.

**Nachteil**: Der Algorithmus hat eine [[linear|Lineare Laufzeit]] von O(n), was bedeutet, dass er in einer Liste mit **n** Elementen im schlimmsten Fall alle Elemente durchsuchen muss.

Beispiel in einem [[activity_diagramm|Aktivitätsdiagramm]]:
![[Pasted image 20250504152214.png]]

Beispiel in [[python_main|Python]] code:
```python
def lineare_suche(liste, ziel):
    for i in range(len(liste)):
        if liste[i] == ziel:
            return i  # Das Element wurde gefunden
    return -1  # Element nicht gefunden
```