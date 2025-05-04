Die **binäre Suche** ist ein effizienter [[search_algorithms_main|Suchalgorithmus]], der verwendet wird, um ein bestimmtes Element in einer bereits **sortierten** Liste zu finden. Der Algorithmus basiert auf dem Prinzip **„Teile und herrsche“**.

Dabei wird zunächst das mittlere Element der Liste betrachtet:

- Ist der gesuchte Wert **gleich** dem mittleren Element, ist die Suche erfolgreich und die position des Wertes wird zurückgegeben.

- Ist der gesuchte Wert **größer** als das mittlere Element, wird die Suche in der **oberen Hälfte** der Liste fortgesetzt.

- Ist der gesuchte Wert **kleiner**, wird die Suche in der **unteren Hälfte** fortgesetzt.

Dieser Vorgang wird so lange wiederholt, bis das gesuchte Element gefunden wurde oder der Suchbereich leer ist → -1 zurück gegeben wird.

Dank dieses Vorgehens reduziert sich die Anzahl der zu prüfenden Elemente mit jedem Schritt um die Hälfte, was die binäre Suche besonders schnell macht. Dadurch hat sie hat eine **logarithmische Laufzeit** von **O(log n)**.


Beispiel in einem [[activity_diagramm|Aktivitätsdiagramm]]:

![[Pasted image 20250504153832.png]]


Beispiel in [[python_main|Python]] code:

```python
def binaere_suche(liste, ziel):
    links, rechts = 0, len(liste) - 1
    while links <= rechts:
        mitte = (links + rechts) // 2
        if liste[mitte] == ziel:
            return mitte  # Das Element wurde gefunden
        elif liste[mitte] < ziel:
            links = mitte + 1
        else:
            rechts = mitte - 1
    return -1  # Element nicht gefunden
```