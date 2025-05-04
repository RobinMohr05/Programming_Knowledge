Eine **relationale Datenbank** ist eine Art von Datenbank, die Daten in **Tabellen** organisiert. Jede Tabelle besteht aus **Zeilen** und **Spalten**, wobei jede Zeile ein Datensatz und jede Spalte ein bestimmtes Attribut dieses Datensatzes darstellt. Relationale Datenbanken verwenden **relationale Modelle**, um Daten zu speichern und zu organisieren.

**Hauptmerkmale einer Relationalen Datenbank:**
1. **Tabellenstruktur:** Daten werden in Tabellen (auch **Relationen** genannt) abgelegt, die miteinander durch **Beziehungen** verknüpft sind.

2. **Schlüssel:**
    - **Primärschlüssel:** Ein Attribut oder eine Kombination von Attributen, die jede Zeile eindeutig identifizieren (z. B. Kundennummer).
		
    - **Fremdschlüssel:** Ein Attribut, das auf den **Primärschlüssel** einer anderen Tabelle verweist, um Beziehungen herzustellen (z. B. Kundennummer in der Bestelltabelle, um zu zeigen, welcher Kunde welche Bestellung gemacht hat).

3. Relationale Datenbanken werden mit **[[sql|SQL]]** abgefragt.

4. **Datenintegrität:** Relationale Datenbanken stellen sicher, dass die Daten konsistent bleiben. Sie erlauben das Setzen von **Constraints** (Bedingungen), z. B. dass in einem bestimmten Feld nur Zahlen oder gültige Datenwerte gespeichert werden können.

### Vorteile:
- **Strukturierte Daten:** Geeignet für Daten, die eine klare Struktur haben (z. B. Kunden, Bestellungen, Produkte).

- **Flexibilität bei Abfragen:** SQL ermöglicht komplexe Abfragen, um Daten aus verschiedenen Tabellen zu kombinieren.

- **Datenintegrität:** Starke Mechanismen zur Sicherstellung der Datenkonsistenz.

### Beispiel:

- **Kundentabelle:**

| Kundennummer | Name         | Adresse          |
| ------------ | ------------ | ---------------- |
| 1            | Max Müller   | Beispielstraße 1 |
| 2            | Anna Schmidt | Beispielstraße 2 |

- **Bestellungstabelle:**

| Bestellnummer | Kundennummer | Betrag |
| ------------- | ------------ | ------ |
| 1001          | 1            | 50,00  |
| 1002          | 2            | 30,00  |
| 1003          | 1            | 30,00  |

Durch den **Fremdschlüssel** (`Kundennummer`) in der Bestelltabelle lässt sich abfragen, welche Bestellungen welcher Kunde getätigt hat.

Relationale Datenbanken sind also besonders dann hilfreich, wenn du strukturierte Daten hast, die in Beziehungen zueinander stehen.