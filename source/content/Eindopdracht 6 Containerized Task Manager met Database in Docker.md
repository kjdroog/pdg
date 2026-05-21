---
created: 2025-09-03T20:08
updated: 2025-09-03T20:10
---
**Niveau:** C  
**Duur:** 180 minuten  
**Doel:**  
Het team leert een eenvoudige webapplicatie te ontwikkelen die draait in Docker, verbonden is met een database (MySQL of PostgreSQL) in een aparte container, en toegankelijk is via een webbrowser.

---

### Opdrachtomschrijving

Ontwikkel in teams van vier een **“Task Manager”** applicatie waarmee gebruikers taken kunnen aanmaken, bekijken en verwijderen. De applicatie moet draaien in Docker, waarbij zowel de webapplicatie als de database in **gescheiden containers** draaien en met elkaar communiceren via een Docker-netwerk.

---

### Functionele eisen

1. **Takenbeheer:**
    - Gebruikers kunnen een taak toevoegen (titel + korte beschrijving).
    - Taken kunnen worden weergegeven in een lijst.
    - Taken kunnen worden verwijderd.
2. **Database:**
    - De taken worden opgeslagen in een database (MySQL of PostgreSQL).
    - De database draait in een **aparte container**.
3. **Webinterface:**
    - De applicatie moet een eenvoudige webinterface hebben (HTML/CSS/JavaScript toegestaan).
    - De backend kan in **Python (Flask)** of **C# (ASP.NET Core)** worden gebouwd.
4. **Docker Setup:**
    - Eén container voor de webapplicatie.
    - Eén container voor de database.
    - Containers communiceren via een Docker-netwerk.
    - Gebruik een `docker-compose.yml` om de containers eenvoudig te starten.

---

### Technische eisen

1. **Projectstructuur:**
    
    - Map met de backend-code.
        
    - Map met database-init scripts (SQL-bestanden).
        
    - Dockerfile voor de webapplicatie.
        
    - `docker-compose.yml` voor het opzetten van de containers.
        
2. **Database-init:**
    
    - Zorg dat de database bij het opstarten een tabel `tasks` heeft met minimaal de kolommen:
        
        - `id` (PRIMARY KEY, AUTO_INCREMENT)
            
        - `title` (VARCHAR)
            
        - `description` (TEXT)
            
3. **Documentatie:**
    
    - Voeg een korte README toe waarin staat:
        
        - Hoe de applicatie gestart kan worden met Docker.
            
        - Welke containers er zijn en hun rollen.
            
        - Hoe de database is ingericht.
            

---

### Stappenplan

1. **Backend bouwen:**
    
    - Bouw een eenvoudige API met endpoints:
        
        - `GET /tasks` → lijst alle taken
            
        - `POST /tasks` → voeg een taak toe
            
        - `DELETE /tasks/:id` → verwijder een taak
            
2. **Database toevoegen:**
    
    - Voeg SQL-scripts toe om de `tasks`-tabel te maken.
        
3. **Dockerfile maken:**
    
    - Schrijf een Dockerfile voor de webapplicatie.
        
4. **docker-compose.yml maken:**
    
    - Voeg services toe voor:
        
        - `app` (de webapplicatie)
            
        - `db` (de database)
            
    - Definieer netwerken en volumes.
        
5. **Testen:**
    
    - Start de containers met `docker-compose up`.
        
    - Controleer of de applicatie via de browser werkt.
        
6. **Presentatie:**
    
    - Geef een korte demo aan de docent: taken toevoegen, bekijken, verwijderen.
        

---

### Uitvoering/Controle

- De applicatie draait volledig in Docker.
    
- Er zijn minimaal **2 containers** (webapp en database).
    
- Taken worden daadwerkelijk in de database opgeslagen.
    
- Er is documentatie aanwezig voor installatie en gebruik.
    
- Het team kan uitleggen hoe de containers samenwerken en waarom Docker handig is.