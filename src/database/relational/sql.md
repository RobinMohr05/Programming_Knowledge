SQL (Structured Query Language) ist eine Sprache zur Definition, Abfrage und Bearbeitung von Daten in Datenbanksystemen. Sie wird häufig im Zusammenhang mit [[relational_database_main|relationalen Datenbanken]] verwendet, ist jedoch unabhängig von deren technischer Umsetzung. SQL dient ausschließlich der Kommunikation mit der Datenbank, nicht deren interner Realisierung.

**Grundprinzip:**  
Daten werden in **Tabellen** organisiert gespeichert. Diese Tabellen können logisch miteinander verknüpft sein (siehe [[relationales_datenbank_modell|Logisches Modell]]).

Der SQL-Syntax wird von vielen Datenbanksystemen verwendet. Dabei kann es zu **leichten Unterschieden** in der Syntax und dem Funktionsumfang kommen.

**Beispiele für SQL-basierte Datenbanksysteme:**
- [[My_SQL]]
- Microsoft SQL Server (MS SQL)
- SQLite
- Oracle
- u. v. m.

_Hinweis: Diese Liste ist nicht vollständig!_

### Teilbereiche von SQL

SQL-Befehle werden in verschiedene Teilgebiete unterteilt:

| **Teilbereich**                        | **Beschreibung**                                           | **Beispiele**                          |
| -------------------------------------- | ---------------------------------------------------------- | -------------------------------------- |
| **DDL** (Data Definition Language)     | Definition und Änderung von Datenbankobjekten              | `CREATE`, `ALTER`, `DROP`, `TRUNCATE`  |
| **DML** (Data Manipulation Language)   | Bearbeitung der in Tabellen gespeicherten Daten            | `SELECT`, `INSERT`, `UPDATE`, `DELETE` |
| **DCL** (Data Control Language)        | Steuerung von Zugriffsrechten                              | `GRANT`, `REVOKE`                      |
| **TCL** (Transaction Control Language) | Verwaltung von Transaktionen (z. B. Speichern, Rücksetzen) | `COMMIT`, `ROLLBACK`                   |
