[[bubble_sort|Bubble Sort]]
Sortieralgorithmen sind Verfahren in der Informatik, mit denen Elemente (meist Zahlen oder Zeichenketten) in eine bestimmte Reihenfolge gebracht werden, typischerweise aufsteigend oder absteigend.

Zu den wichtigsten Sortieralgorithmen gehören:
- [[bubble_sort|Bubble Sort]]
- [[sort_algorithms_main#**Insertion Sort** (gut für kleine Datenmengen) GPT|Insertion Sort]]
- [[sort_algorithms_main#**Merge Sort** (effizient & stabil, rekursiv) GPT|Merge Sort]]
- [[sort_algorithms_main#**Quick Sort** (schnell, aber nicht stabil) GPT|Quick Sort]]


### **Insertion Sort** (gut für kleine Datenmengen) #GPT

**Idee:** Gehe von links nach rechts durch das Array und „füge“ jedes neue Element an der richtigen Stelle im sortierten Teil ein.

**Beispiel:**  
`[5, 3, 4]`  
→ `[3, 5, 4]`  
→ `[3, 4, 5]`

**Komplexität:**
- Beste Fall: O(n)
- Schlechtester Fall: O(n²)

### **Merge Sort** (effizient & stabil, rekursiv) #GPT

**Idee:** Teile das Array in zwei Hälften, sortiere sie rekursiv, und füge sie dann zusammen (merge).

**Beispiel:**  
`[5, 3, 4] → [5], [3, 4] → [3, 4], [5] → [3, 4, 5]`

**Komplexität:**

- Immer: O(n log n)

### **Quick Sort** (schnell, aber nicht stabil) #GPT

**Idee:** Wähle ein "Pivot"-Element, teile das Array in kleinere/gleich/größere Elemente, sortiere die Teile rekursiv.

**Beispiel:**  
Pivot = 4 → `[3] + [4] + [5]` → `[3, 4, 5]`

**Komplexität:**
- Durchschnitt: O(n log n)
- Schlechtester Fall: O(n²) (wenn Pivot schlecht gewählt)




