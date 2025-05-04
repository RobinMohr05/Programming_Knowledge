**NoSQL** steht für "**Not only SQL**" und bezeichnet Datenbanksysteme, die **nicht dem klassischen relationalen Modell folgen** und **nicht zwingend SQL** verwenden.

### Kurz erklärt:

- **NoSQL-Datenbanken** sind für **hohe Flexibilität, Skalierbarkeit** und **große Datenmengen** optimiert.
    
- Statt Tabellen mit festen Schemata nutzen sie **dynamischere Strukturen** wie:
    
    - 🔸 **Dokumente** (z. B. JSON) → _[[mongo_DB|MongoDB]]_
        
    - 🔸 **Key-Value-Paare** → _Redis_
        
    - 🔸 **Spaltenorientierte Datenbanken** → _Cassandra_
        
    - 🔸 **Graphenmodelle** → _Neo4j_
        

### Merkmale:

- Kein festes Schema (Schema-frei)
    
- Horizontal gut skalierbar (gut für verteilte Systeme)
    
- Für unstrukturierte oder sich schnell ändernde Daten geeignet
    
- Oft schneller bei großen Datenmengen oder speziellen Anwendungsfällen
    

---

**Vergleich zu SQL:**

| Merkmal      | SQL (relational)                 | NoSQL                                      |
| ------------ | -------------------------------- | ------------------------------------------ |
| Struktur     | Tabellen mit festen Schemata     | Flexibel, schemafrei                       |
| Sprache      | SQL                              | Unterschiedlich (abhängig vom System)      |
| Beziehungen  | Explizit mit Fremdschlüsseln     | Schwächer oder anders umgesetzt            |
| Skalierung   | Vertikal                         | Horizontal                                 |
| Geeignet für | Konsistente, strukturierte Daten | Flexible, große oder verteilte Datenmengen |
