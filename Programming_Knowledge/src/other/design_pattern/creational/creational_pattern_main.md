
# **KOMPLETT CHATGPT GENERIERT**

## Was sind Erzeugungsmuster?

**Erzeugungsmuster** (englisch _Creational Patterns_) gehören zur Gruppe der **[[design_pattern_main|Design Pattern]]** und beschäftigen sich mit der **Erstellung von Objekten**. Sie kapseln den Erstellungsprozess, um die Abhängigkeit vom konkreten Typ zu reduzieren. Dadurch wird der Code flexibler, leichter wartbar und besser testbar.

---

## Ziele von Erzeugungsmustern

- **Flexibilität:** Objekterstellung ist nicht fest an bestimmte Klassen gebunden.
    
- **Wartbarkeit:** Änderungen an der Art der Objekterstellung erfordern keine Änderungen im Anwendungscode.
    
- **Wiederverwendbarkeit:** Die gleiche Logik kann verschiedene Objekttypen erzeugen.
    
- **Reduktion von Duplikation:** Die Erzeugung ähnlicher Objekte wird zentral gesteuert.
    

---

## Wichtige Erzeugungsmuster (GoF – Gang of Four)

| Muster                           | Beschreibung                                                                                    |
| -------------------------------- | ----------------------------------------------------------------------------------------------- |
| **[[factory\|Factory Pattern]]** | Lässt Unterklassen entscheiden, welches Objekt instanziiert wird.                               |
| **Abstract Factory**             | Erzeugt Familien verwandter Objekte, ohne deren konkrete Klassen zu kennen.                     |
| **[[singleton\|Singleton]]**     | Stellt sicher, dass eine Klasse genau eine Instanz besitzt, und bietet globalen Zugriff darauf. |
| **Builder**                      | Trennt die Konstruktion eines komplexen Objekts von seiner Darstellung.                         |
| **Prototype**                    | Erzeugt neue Objekte durch das Kopieren eines bestehenden Objekts.                              |
| **Singleton**                    | Stellt sicher, dass eine Klasse genau eine Instanz besitzt, und bietet globalen Zugriff darauf. |

---

## Einfaches Beispiel zur Verdeutlichung

Statt ein Objekt direkt zu erzeugen:

```python
lion = Lion()
```

wird über eine Factory gearbeitet:

```python
animal = AnimalFactory.create_animal("lion")
```

Vorteil: Der Code bleibt offen für neue Tierarten, ohne dass er geändert werden muss.

---

Möchtest du zu jedem dieser Muster ein kleines Beispiel oder eine Vergleichstabelle der Vor- und Nachteile?