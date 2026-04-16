# **KOMPLETT CHATGPT GENERIERT**

**JSON** steht für **JavaScript Object Notation** und ist ein **leichtgewichtiges [[data_format|Datenformat]]**, das verwendet wird, um Daten **strukturiert** und **lesbar für Menschen und Maschinen** darzustellen. Es ist besonders beliebt beim **Datenaustausch zwischen Server und Client**, z. B. in Webanwendungen oder [[api_main|APIs]].

---

### **Grundstruktur von JSON**

JSON besteht aus **Schlüssel-Wert-Paaren** und ist aufgebaut wie ein Objekt in JavaScript:

```json
{
  "name": "Anna",
  "alter": 30,
  "verheiratet": false,
  "hobbys": ["lesen", "wandern"],
  "adresse": {
    "stadt": "Berlin",
    "plz": "10115"
  }
}
```

---

### **Datentypen in JSON**

- **Strings** (Text): `"Anna"`
    
- **Zahlen**: `30`
    
- **Booleans**: `true`, `false`
    
- **Arrays** (Listen): `["lesen", "wandern"]`
    
- **Objekte** (verschachtelte Daten): wie `"adresse"`
    
- **null**: `null` (leerer Wert)
    

---

### Wichtige Regeln

- Doppelte Anführungszeichen `"` müssen für **Strings und Schlüssel** verwendet werden.
    
- Kein Komma **nach dem letzten Element** in einem Objekt oder Array.
    
- Keine Kommentare erlaubt (anders als in JavaScript).
    

---

### JSON wird verwendet für:

- API-Antworten (z. B. von einer REST API)
    
- Konfigurationsdateien (z. B. `package.json` in Node.js)
    
- Speichern strukturierter Daten (z. B. in NoSQL-Datenbanken wie MongoDB)
    