**Datenhaltung und Datenaustausch: Formate für strukturierte Daten**

Damit Computer Daten effizient speichern, verarbeiten und austauschen können, müssen diese in einer Form vorliegen, die maschinenlesbar ist. Dazu verwendet man sogenannte **strukturierte Datenformate**. Diese Formate organisieren Informationen nach klar definierten Regeln, sodass Programme sie leicht analysieren und weiterverarbeiten können.

**Beispiele für strukturierte Datenformate:**

|                    | JSON                                                                       | CSV                                                                     | XML                                                             | YAML                                                       |
| ------------------ | -------------------------------------------------------------------------- | ----------------------------------------------------------------------- | --------------------------------------------------------------- | ---------------------------------------------------------- |
| Erläuterung        | _JavaScript Object Notation_, leichtgewichtiges, textbasiertes Datenformat | _Comma-Separated Values_, einfache Textdarstellung tabellarischer Daten | _eXtensible Markup Language_, erweiterbares Auszeichnungssystem | _YAML Ain’t Markup Language_, menschenlesbares Datenformat |
| Aufbau des Formats | `{ "name": "Anna", "alter": 25 }`                                          | `Anna,25`                                                               | `<person><name>Anna</name><alter>25</alter></person>`           | `name: Anna \nalter: 25`                                   |
| Einsatzgebiete     | Web-APIs, Konfigurationsdateien, Datenübertragung                          | Tabellenkalkulationen, einfache Datenexporte (z. B. Excel)              | Datenaustausch zwischen Systemen, Konfigurationsdateien         | DevOps, Konfigurationsdateien (z. B. Docker, Kubernetes)   |
