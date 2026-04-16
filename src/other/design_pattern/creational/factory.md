## **Factory-Method-Pattern**

### Klassifizierung:**
[[creational_pattern_main|Erzeugungsmuster (Creational Pattern)]]

---

### **Zweck:**

Das Factory-Method-Pattern kapselt die Objekterstellung. Dabei wird die Verantwortung zur Instanziierung von Objekten an Unterklassen delegiert, ohne dass der aufrufende Code die genaue Klasse kennen muss.

---

### **Anwendbarkeit:**

Verwende das Factory-Method-Pattern, wenn:

- Eine Klasse die Instanziierung ihrer Objekte delegieren soll.
    
- Der Code offen für Erweiterung, aber geschlossen für Modifikation sein soll (Open/Closed-Prinzip).
    
- Objekte einer gemeinsamen Schnittstelle erzeugt werden sollen, jedoch mit verschiedenen konkreten Implementierungen.
    

---

### **Struktur (UML-Komponenten):**

- **Product:** Abstrakte Oberklasse oder Interface für Produkte.
    
- **ConcreteProduct:** Konkrete Implementierung des Produkts.
    
- **Creator:** Abstrakte Klasse mit der Factory-Methode.
    
- **ConcreteCreator:** Implementiert die Factory-Methode und erzeugt konkrete Produkte.
    

---

### **Was muss beachtet werden?**

- Die Struktur sollte sorgfältig geplant werden.
    
- Das Pattern ist nur sinnvoll, wenn sich Produktklassen unterscheiden und leicht erweiterbar sein sollen.
    
- Übermäßiger Einsatz kann zu unnötiger Komplexität führen.
    

---

### **Vor- und Nachteile**

| Vorteil                     | Nachteil                              |
| --------------------------- | ------------------------------------- |
| Fördert Modularität         | Höhere Komplexität                    |
| Erleichtert Erweiterbarkeit | Mehr Klassen nötig                    |
| Unterstützt Unit Testing    | Schwierig zu verstehen für Einsteiger |

---

### **Beispiel in Python**

```python
from abc import ABC, abstractmethod

# Product
class Button(ABC):
    @abstractmethod
    def render(self) -> str:
        pass

# Concrete Products
class WindowsButton(Button):
    def render(self) -> str:
        return "Rendering a Windows Button"

class MacButton(Button):
    def render(self) -> str:
        return "Rendering a Mac Button"

# Creator
class Dialog(ABC):
    def render_dialog(self):
        button = self.create_button()
        return button.render()

    @abstractmethod
    def create_button(self) -> Button:
        pass

# Concrete Creators
class WindowsDialog(Dialog):
    def create_button(self) -> Button:
        return WindowsButton()

class MacDialog(Dialog):
    def create_button(self) -> Button:
        return MacButton()

# Anwendung
def client_code(dialog: Dialog):
    print(dialog.render_dialog())

# Test
if __name__ == "__main__":
    os_type = "Windows"  # Eingabe könnte z. B. vom Betriebssystem kommen

    if os_type == "Windows":
        dialog = WindowsDialog()
    else:
        dialog = MacDialog()

    client_code(dialog)

```



# **KOMPLETT CHATGPT GENERIERT**


Das **Factory Pattern** ist ein weiteres **Erzeugungsmuster** (Creational Pattern), das verwendet wird, um Objekte zu erstellen, ohne dass der genaue Typ des zu erstellenden Objekts in der Client-Klasse bekannt sein muss. Stattdessen wird die Objekterstellung an eine Factory-Klasse delegiert. Das Factory Pattern hilft dabei, den Code flexibler und wartungsfreundlicher zu machen, da der Code zur Erstellung von Objekten in einer zentralen Factory-Klasse kapsuliert wird.

### Klassendiagramm

Das Klassendiagramm für das Factory Pattern sieht in der Regel so aus:

```
      +-------------------+
      |     Creator       |<----------------------------------+
      +-------------------+                                   |
      | +factoryMethod()   |                                   |
      +-------------------+                                   |
                ^                                             |
                |                                             |
      +-------------------+       1       *      +----------------------+
      |  ConcreteCreator  |-------------------->|   Product             |
      +-------------------+                      +----------------------+
      | +factoryMethod()   |                      | +operation()          |
      +-------------------+                      +----------------------+
                                                    ^ 
                                                    |
                                          +------------------------+
                                          | ConcreteProductA       |
                                          +------------------------+
                                          | +operation()           |
                                          +------------------------+
                                          +------------------------+
                                          | ConcreteProductB       |
                                          +------------------------+
                                          | +operation()           |
                                          +------------------------+
```

- **Creator**: Definiert eine Methode (`factoryMethod()`), die für die Erstellung eines Produkts zuständig ist.
    
- **ConcreteCreator**: Eine konkrete Implementierung der `Creator`-Klasse, die die `factoryMethod()` überschreibt, um spezifische Produkte zu erzeugen.
    
- **Product**: Ein Interface oder eine abstrakte Klasse, die das Produkt definiert, das erzeugt werden soll.
    
- **ConcreteProduct**: Eine konkrete Implementierung des Produkts.
    

### Beispielcode

Hier ist ein einfaches Beispiel in Java, um das Factory Pattern zu demonstrieren:

```java
// Product Interface
interface Product {
    void operation();
}

// ConcreteProductA
class ConcreteProductA implements Product {
    @Override
    public void operation() {
        System.out.println("Operation von ConcreteProductA");
    }
}

// ConcreteProductB
class ConcreteProductB implements Product {
    @Override
    public void operation() {
        System.out.println("Operation von ConcreteProductB");
    }
}

// Creator (Factory)
abstract class Creator {
    public abstract Product factoryMethod();
}

// ConcreteCreatorA
class ConcreteCreatorA extends Creator {
    @Override
    public Product factoryMethod() {
        return new ConcreteProductA();  // Gibt ConcreteProductA zurück
    }
}

// ConcreteCreatorB
class ConcreteCreatorB extends Creator {
    @Override
    public Product factoryMethod() {
        return new ConcreteProductB();  // Gibt ConcreteProductB zurück
    }
}

// Main Program
public class FactoryPatternDemo {
    public static void main(String[] args) {
        // Verwenden von ConcreteCreatorA
        Creator creatorA = new ConcreteCreatorA();
        Product productA = creatorA.factoryMethod();
        productA.operation();

        // Verwenden von ConcreteCreatorB
        Creator creatorB = new ConcreteCreatorB();
        Product productB = creatorB.factoryMethod();
        productB.operation();
    }
}
```

### Erklärung des Codes:

1. **Product**: Ein Interface, das eine Methode `operation()` definiert, die von allen konkreten Produkten implementiert wird.
    
2. **ConcreteProductA und ConcreteProductB**: Zwei konkrete Implementierungen des `Product`-Interfaces. Jede Implementierung führt die `operation()`-Methode auf ihre eigene Weise aus.
    
3. **Creator**: Eine abstrakte Klasse, die eine abstrakte Methode `factoryMethod()` definiert, die für die Erstellung von Produkten verantwortlich ist.
    
4. **ConcreteCreatorA und ConcreteCreatorB**: Konkrete Implementierungen der `Creator`-Klasse. Jede Factory-Methode erzeugt ein spezifisches Produkt (entweder `ConcreteProductA` oder `ConcreteProductB`).
    
5. **Main Program**: Demonstriert die Verwendung des Factory Patterns. Je nach Bedarf wird entweder `ConcreteCreatorA` oder `ConcreteCreatorB` verwendet, um das entsprechende Produkt zu erstellen.
    

### Ablauf:

1. Der Client (im `Main Program`) weiß nur von der `Creator`-Klasse und deren Methode `factoryMethod()`, nicht aber vom genauen Typ des Produkts.
    
2. Der Client ruft die Factory-Methode der konkreten Creator-Klasse auf, um das Produkt zu erhalten.
    
3. Die Factory-Klasse erstellt das konkrete Produkt (entweder `ConcreteProductA` oder `ConcreteProductB`), ohne dass der Client den konkreten Typ kennt.
    

### Vorteile des Factory Patterns:

- **Entkopplung**: Der Client muss nicht wissen, welche konkrete Produktklasse instanziiert wird. Dadurch wird die Flexibilität erhöht und der Code einfacher zu warten.
    
- **Erweiterbarkeit**: Neue Produkttypen können hinzugefügt werden, ohne den Code des Clients zu verändern. Es müssen nur neue konkrete Creator-Klassen hinzugefügt werden.
    
- **Verborgene Logik**: Komplexe Instanziierungslogik kann in der Factory versteckt werden, sodass der Client nur eine einfache Schnittstelle nutzt.
    

### Beispiel für eine Erweiterung:

Wenn später ein weiteres Produkt, z. B. `ConcreteProductC`, benötigt wird, kann einfach eine neue `ConcreteCreatorC`-Klasse hinzugefügt werden, ohne die bestehenden Klassen zu ändern. Das ist besonders nützlich, wenn das System wächst.

Hoffentlich hilft dir das weiter! Falls du noch Fragen hast oder mehr Details brauchst, lass es mich wissen!