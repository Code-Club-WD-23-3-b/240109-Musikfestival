# 240109-Musikfestival

#### Hintergrund:
Du bist beauftragt, eine Backend-Anwendung für ein Musikfestival mit Express und Mongoose zu entwickeln. Die Anwendung soll Informationen über Künstler, Bühnen und Auftritte verwalten. Nutzer der Anwendung sollen in der Lage sein, Informationen über Künstler, die Bühnen, auf denen sie auftreten, und den Zeitplan der Auftritte abzufragen.

#### Anforderungen:
1. **Datenbankschema-Design**:
   - **Künstler-Schema**: Enthält Felder für den Namen des Künstlers, das Genre und eine Liste der Auftritte (referenziert).
   - **Bühnen-Schema**: Enthält Felder für den Namen und den Standort der Bühne.
   - **Auftritts-Schema**: Enthält Felder für die Bühne (referenziert), den Künstler (referenziert), Datum und Uhrzeit.

2. **API-Endpunkte**:
   - Ein Endpunkt zum Hinzufügen neuer Künstler, Bühnen und Auftritte.
   - Ein Endpunkt zum Abrufen aller Auftritte mit ausgefüllten Künstler- und Bühnendetails.
   - Ein Endpunkt zum Abrufen aller Auftritte eines bestimmten Künstlers.
   - Ein Endpunkt zum Abrufen aller Künstler, die auf einer bestimmten Bühne auftreten.

3. **Bonus**:
   - Implementiere die Möglichkeit, bestimmte Felder in den Antworten auszuwählen (z.B. nur den Namen und das Genre des Künstlers abrufen).
   - Füge eine Funktion hinzu, um Auftritte nach Datum zu filtern.

#### Übungsschritte:

1. **Einrichten von Express und Mongoose**: Initialisiere ein neues Express-Projekt und richte Mongoose ein, um eine Verbindung zu einer MongoDB-Datenbank herzustellen.

2. **Definiere Schemas und Modelle**: Basierend auf den Anforderungen, definiere die drei Schemas (`Künstler`, `Bühne`, `Auftritt`) und erstelle Mongoose-Modelle für sie.

3. **Implementiere API-Endpunkte**:
   - Erstelle Routen und Controller zum Hinzufügen neuer Künstler, Bühnen und Auftritte.
   - Implementiere die Logik zum Abrufen von Auftritten mit Details über den Künstler und die Bühne. Verwende Mongoose's `populate()`-Methode, um verwandte Daten einzubeziehen.
   - Erstelle Routen zum Abrufen von Auftritten eines bestimmten Künstlers und auf einer bestimmten Bühne.

4. **Implementiere Bonus Abfragen**:
   - Erweitere die Endpunkte, um den Clients zu ermöglichen, anzugeben, welche Felder sie in der Antwort haben möchten, indem du die `select()`-Methode verwendest.
   - Füge eine Funktion zum Filtern von Auftritten nach Datum hinzu.

5. **Testen**:
   - Teste die API-Endpunkte mit einem Tool wie Postman oder einem HTTP-Client deiner Wahl. Überprüfe, ob die Daten korrekt ausgefüllt werden und ob das Filtern und die Feldauswahl wie erwartet funktionieren.
