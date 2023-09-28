# Where Next - Web Application for the planning of social, cultural, and sports events

Progetto per il laboratorio di Architetture Software e Sicurezza Informatica - Sapienza Università di Roma 

## Collaboratori
Caterina Borzillo, Michela Capasso, Riccardo Casciotti, Francesco Cermaria
## Funzionalità
L’obiettivo del progetto software Where Next è quello di realizzare un sistema che sia in grado di offrire a tutti gli utenti iscritti alla piattaforma la possibilità di organizzare un incontro tra amici in modo tale da scoprire, in base alle preferenze espresse da ciascuno, nuovi locali, esercizi pubblici, cinema o altri eventi sociali, culturali o sportivi di comune interesse.  In particolare, dal punto di vista degli utenti, una volta iscritti al sito, si aggiungono i propri amici (iscritti anche loro alla piattaforma) e si selezionano le categorie preferite (ad esempio pizzerie, ristoranti, cocktail bar, cinema, concerti, biblioteche, centri sportivi) con l’obiettivo di organizzare un incontro: si scelgono la data e gli amici e il sistema software in base alle preferenze espresse, seleziona i locali o gli eventi comuni tra gli utenti selezionati e formula un elenco di proposte compatibili. Vi è anche la possibilità che un utente possa iscriversi alla piattaforma con il ruolo di “proprietario di un locale” ovvero “organizzatore di un evento” in modo tale da poter aggiungere il proprio locale, attività commerciale o il proprio evento nel database del sito

 Da un punto di vista più generale, l’approccio al progetto Where Next consente di accogliere non solo quegli utenti che intendano pianificare ad esempio, una spassosa serata con amici o una partita di tennis in un centro sportivo, ma permette di venire incontro anche alle esigenze dei proprietari/gestori di ristoranti, pizzerie, bar o degli organizzatori di eventi al fine di far conoscere il proprio locale o l’evento stesso ad un insieme sempre più vasto di clienti.

## Dettagli di implementazione
### LINGUAGGIO
Ruby on Rails

### RUOLI
-	Utente registrato come ‘user’: può organizzare un’uscita,visualizzare quelle passate e future e può aggiungere degli amici. Può inoltre selezionare delle categorie per aggiungerle alle sue preferenze. Può visualizzare la lista dei locali ed aggiungere o rimuovere un locale ai preferiti. 
-	Utente registrato come ‘admin’: è l’unico a poter modificare aggiungere o eliminare le categorie ed approvare i locali che sono stati aggiunti dagli owner. Può inoltre bannare gli utenti dal sito. 
-	Utente registrato come ‘owner’: può aggiungere locali al sito e questi rimarranno in attesa di approvazione da parte dell’admin. Può inoltre visualizzare i locali da lui aggiunti, modificarli o eventualmente eliminarli. 
-	Utente non registrato: può vedere la homepage con una breve descrizione del sito, può registrarsi o fare il login 

### INTERAZIONE CON SERVIZI ESTERNI 
Come servizio esterno abbiamo utilizzato l’API di OpenStreetMap per ottenere longitudine e latitudine della posizione di una via del locale inserito; con Leaflet verrà mostrato il locale su una mappa 
 
### AUTENTICAZIONE  
 Sono previste due modalità di accesso al sito:  
•	Locale -> l’utente può registrarsi direttamente sul sito inserendo i propri dati  
•	OAuth -> l’utente può accedere al sito direttamente tramite il proprio account Facebook 

### USER STORIES 
https://drive.google.com/file/d/1uJqrTNuNn1bJtIJ-yYr0Wx79WRUG76wE/view?usp=sharing

### MOCKUPS
https://drive.google.com/file/d/1ciFfJlpCUgHsp3cDsygXvqy2dDLv7g3h/view?usp=sharing

### PIANO DEI TEST: 

-  Test di unita':
    1. Modello Location 
    2. Modello Category 
  
-  Test funzionali:
    1. Controller Location 
    2. Controller Category 
    3. Controller Gathering
  
-  Test di integrazione: 
    1. Accettazione/Rifiuto di un locale (da parte di un Admin) 
    2. Scelta categorie preferite (da parte di uno user)
    3. Aggiungi locale ai preferiti (da parte di uno user)
    4. Matching locations (da parte di uno user)
