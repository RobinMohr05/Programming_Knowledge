SQL Abkürzung für Structured Query Language. Es dient in Datenbanksystemen zur Definierung von Daten und zur Informationsgewinnung. SQL wird oft in Verbindung mit [[relational_database_main|relationalen Datenbanken]] genannt.  sql hat nichts damit zu tun, wie die Datenbank technisch realisiert ist, sondern ist die sprache um mit datenbanken zu arbeiten.
Grundprinzip: Daten werden in form von Tabellen gespeichert, welche logisch miteinander verknüpft sein können (siehe [[relationales_datenbank_modell|Logisches Modell]]).

Der SQL-Syntax wird von verschiedenen Datenbanksystemen verwendet.
**Beispielsysteme:**
- [[My_SQL]]
- MsSQL
- SQlite
- Oracle
- usw...
**Keine vollständige Liste!!! - Leichte Unterschiede im Syntax mögl.**

SQL gliedert sich in verschiedene Teilbereiche auf, in denen die Befehle unterteilt werden.

| Teilgebiet                         | Erklärung                                                 | Beispiel                       |
| ---------------------------------- | --------------------------------------------------------- | ------------------------------ |
| DDL (Data Definition Language)     | Definiert und verändert Datenbankobjekte                  | CREATE, ALTER, DROP, TRUNCATE  |
| DML (Data Manipulation Language)   | Bearbeitet Daten in Tabellen                              | SELECT, INSERT, UPDATE, DELETE |
| DCL (Data Control Language)        | Steuert Zugriffsrechte                                    | GRANT, REVOKE                  |
| TCL (Transaction Control Language) | Steuert Transaktionen (z. B. speichern oder zurücksetzen) | COMMIT, ROLLBACK               |

