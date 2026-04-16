MongoDB ist eine dokumentenorientierte NoSQL-Datenbank, die Daten in **BSON** (binäres JSON)-Format speichert. Sie bietet eine hohe **Flexibilität**, da keine festen Schemata erforderlich sind, was die Speicherung von unstrukturierten und semi-strukturierten Daten erleichtert.

### Wesentliche Merkmale:

- **Dokumentenorientiert**: Daten werden als Dokumente (ähnlich JSON) gespeichert, was flexible Datenstrukturen ermöglicht.
    
- **Schemalosigkeit**: Du musst das Datenmodell nicht im Voraus definieren; Dokumente können unterschiedlich strukturiert sein.
    
- **Horizontale Skalierbarkeit**: Einfaches Skalieren auf mehrere Server (Sharding), was MongoDB besonders für große, verteilte Systeme geeignet macht.
    
- **Replikation**: Daten werden auf mehreren Servern gespeichert, was Ausfallsicherheit garantiert.
    
- **Aggregation**: Komplexe Abfragen und Berechnungen sind über das Aggregation-Framework möglich.
    

### Vorteile:

- **Flexibilität** bei der Speicherung von Daten.
    
- **Hohe Leistung** bei großen Datenmengen und schnellem Datenzugriff.
    
- **Einfache Skalierbarkeit** durch horizontale Sharding.
    

### Nachteile:

- **Keine JOINs**: Verhältnisse zwischen Daten müssen oft denormalisiert werden.
    
- **Konsistenz**: In verteilten Systemen kann die Konsistenz zugunsten von Verfügbarkeit und Partitionstoleranz geopfert werden (CAP-Theorem).
    

### Anwendungsfälle:

- Echtzeit-Datenverarbeitung, IoT, Webanwendungen und Big Data-Projekte.