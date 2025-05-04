Die Normalisierung von relationalen Datenbanken ist **ein Vorgehen**, bei dem die **Ausgangstabelle in mehrere kleine Tabellen** zerlegt wird. Dann werden sie über Fremdschlüssel in Beziehung gesetzt.

**Ziel** einer solchen Normalisierung ist das Erschaffen einer **redundanzfreien Datenspeicherung**, die **Vermeidung von Anomalien**, sowie die Erstellung eines **klar strukturierten Datenbankmodells**.
### 1. Normalform
**_Die 1. Normalform ist dann gegeben, wenn alle Attribute in einer Tabelle Atomar vorliegen._**
### 2. Normalform
_**Die 2. Normalform ist dann gegeben, wenn:**_
- _**Die 1. Normalform gegeben ist und**_
- _**Jedes nicht dem Primärschlüssel zugehörige Attribut funktional vom Primärschlüssel abhängig ist, jedoch nicht von einzelnen Teilen des Primärschlüssels abhängt.**_
### 3. Normalform
_**Die 3. Normalform ist gegeben, wenn**_
- **_Sich die Relation in der 2. Normalform befindet (und damit auch in der 1. NF) und_**
- **_Keine Nicht-Schlüsselattribute funktional voneinander abhängig sind._**

#### Anomalien
**Einfüge-Anomalie:** Bei dieser Form handelt es sich darum, dass ein Datensatz nur eingefügt werden kann, wenn ein anderer Datensatz auch hinzugefügt wird.

**Lösch-Anomalie:** Bei einer Lösch-Anomalie handelt es sich um Datensätze, die aus Versehen mitgelöscht werden.

**Änderungs-Anomalie:** Hier müssen bei einer Änderung immer mehrere Datensätze geändert werden. Das kann zu schnelleren Tippfehlern oder übersehen von Datensätzen führen.


