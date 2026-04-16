# **KOMPLETT CHATGPT GENERIERT**

HTTP-Statuscodes sind standardisierte **numerische Codes**, die ein Webserver als Antwort auf eine HTTP-Anfrage (z. B. beim Laden einer Website) an den Client (z. B. einen Browser) zurückgibt. Sie informieren darüber, ob eine Anfrage erfolgreich war, einen Fehler hatte oder weitergeleitet wurde.

Hier ist eine kurze Übersicht über die **Hauptkategorien**:

### 1xx – **Information**

> Die Anfrage wird fortgesetzt.

- **100 Continue** – Der Client soll mit der Anfrage fortfahren.
    

### 2xx – **Erfolg**

> Die Anfrage war erfolgreich.

- **200 OK** – Alles in Ordnung.
    
- **201 Created** – Eine Ressource wurde erfolgreich erstellt.
    

### 3xx – **Umleitung**

> Weitere Schritte sind erforderlich (z. B. Weiterleitung).

- **301 Moved Permanently** – Dauerhafte Weiterleitung.
    
- **302 Found** – Temporäre Weiterleitung.
    

### 4xx – **Clientfehler**

> Fehler auf Seiten des Clients (z. B. Browser).

- **400 Bad Request** – Ungültige Anfrage.
    
- **401 Unauthorized** – Nicht autorisiert.
    
- **403 Forbidden** – Zugriff verweigert.
    
- **404 Not Found** – Seite nicht gefunden.
    

### 5xx – **Serverfehler**

> Der Server konnte die Anfrage nicht erfüllen.

- **500 Internal Server Error** – Allgemeiner Serverfehler.
    
- **502 Bad Gateway** – Fehlerhafte Antwort vom Upstream-Server.
    
- **503 Service Unavailable** – Server derzeit nicht verfügbar.
    