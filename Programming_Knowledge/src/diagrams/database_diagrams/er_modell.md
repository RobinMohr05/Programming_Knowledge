Das Entity Relationship Modell (ER-Modell) ist ein Modell zum Darstellen von Datenstrukturen in einer [[relational_database_main|Relationalen Datenbank]]. Es zeigt an wie Informationen in einer Datenbank gespeichert sind und wie diese zueinander in einer Beziehung stehen.
![[ER_Modell_Cheatsheet.svg]]
**Entität**  
Eine Entität ist ein eindeutig identifizierbares Objekt aus der realen Welt, wie Produkte, Bestellungen oder Kunden. Es gibt zwei Arten:

- **Starke Entitätstypen** existieren unabhängig (z. B. ein Buch).
- **Schwache Entitätstypen** sind auf andere Entitäten angewiesen (z. B. Seiten eines Buchs).  
	Im **ER-Diagramm**:
- Starke Entitäten = einfaches Rechteck
- Schwache Entitäten = doppeltes Rechteck

**Attribute & Schlüssel**  
Attribute beschreiben Eigenschaften von Entitäten (z. B. Name, Alter).

- **Primärschlüssel**: Eindeutiges Attribut zur Identifizierung (z. B. Kundennummer).
- **Fremdschlüssel**: Verweist auf den Primärschlüssel einer anderen Entität (z. B. Kundennummer in Bestellungen).  
	**Referenzintegrität**: Jeder Fremdschlüssel muss auf einen gültigen Primärschlüssel zeigen.

**Beziehung (Relationship)**  
Verbindungen zwischen Entitäten, dargestellt als **Raute** im ER-Diagramm.  
Beispiel: „Student“ belegt „Seminar“.

**Kardinalität**  
Beschreibt, wie viele Entitäten miteinander verknüpft sind:

- **1:1** – z. B. Mitarbeiter ↔ Mitarbeiterausweis
- **1:n** – z. B. Kunde ↔ Bestellungen
- **n:m** – z. B. Lieferant ↔ Produkte

**ER-Modell-Typen**  
Es gibt verschiedene Arten von ER-Diagrammen mit teils unterschiedlichen Symbolen, aber ähnlichem Aufbau.