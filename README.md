# L’utente clicca su un bottone che genererà una griglia di gioco quadrata. Ogni cella ha un numero progressivo, da 1 a 100. Ci saranno quindi 10 caselle per ognuna delle 10 righe. Quando l’utente clicca su ogni cella, la cella cliccata si colora di azzurro ed emetto un messaggio in console con il numero della cella cliccata.

## Realizziamo il layout statico prima sull'HTML aggiungendo lo stile con il nostro foglio di stile in CSS.
  - Realizziamo un header iniziale.
  - All'interno dell'header inseriamo uno span con il nome del gioco ed un button che ci servirà per azionare il gioco.
  - Realizziamo una section.
  - All'interno della section inseriamo un div con la classe container, che avrà lo scopo di contenere un altro div con la classe grid (la nostra griglia effettiva.). Dentro il div con la classe grid inseriremo tanti div con classe box quanti sono desiderati.

- Stilizziamo il tutto tramite CSS per avere un'idea del layout creato in CSS.

## Passiamo alla parte di JS per creare la griglia in automatico al click sul bottone.

- Creare la griglia 10 x 10 al click sul bottone.
- Incapsulare la creazione di questa griglia all'interno di una funzione.
- Al click sul pulsante invocare la funzione per creare la griglia.
  - Recuperare dal DOM la griglia tramite il querySelector e dichiararlo dentro una variabile gridELement.
  - Creare un ciclo FOR con 100 interazioni.
  - Inizializzare il valore dell'innerhtml della griglia a stringa vuota, che sarà il suo valore iniziale.
  - Ad ogni interazione del ciclo FOR dobbiamo andare ad aggiungere un box nella griglia.
    - Tramite template leteral scrivere il codice inerente al box che contenga anche la variabile dell'indice di riferimento di ogni box (n) e dichiararlo in una variabile htmlBox.
    - Assegnare all'inner.html dell'elemento griglia del DOM ad ogni interazione del ciclo il nuovo valore che si andrà ogni volta a sommare alla variabile htmlBox.
  - Creare un eventListner di tipo click sul bottone.
     - Traslare all'interno dell'eventListner la sezione precedentemente creata inerente al ciclo FOR.

### Quando l’utente clicca su ogni cella, la cella cliccata si colora di azzurro ed emetto un messaggio in console con il numero della cella cliccata.
  - Creiamo intanto nel nostro foglio di stile CSS una classe bg-light-blue che assegnerà il colore del box.
  - Creiamo un eventListner per ogni box della griglia dove al click ci permetterà di aggiungere la classe inerente al colore.
   - Recuperiamo dal DOM tramite il querySelectorAll tutti gli elementi contenenti la classe box.
   - Facciamo un console.log per vedere se sono stati recuperati.
   - Data la nostra nodelist facciamo un ciclo FOR per aggiungere ad ogni box un eventListner.
     - Dichiariamo una variabile currentBoxElement per memorizzarci l'indice corrente del box.
     - Aggiungiamo un eventListner di tipo click al currentBoxElement.
        - Aggiungiamo la classe creata precedentemente in CSS.
        - Prendiamo il currentBoxElement e tramite classList.add aggiungiamo la classe.
        - Facciamo un console.log dove stamperemo il numero del box cliccato, che apparirà a questo punto del colore azzurro.