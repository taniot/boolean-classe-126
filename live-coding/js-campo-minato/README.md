# Campo Minato

## Prima parte

L'utente clicca su un bottone che genererà una griglia di gioco quadrata.
Ogni cella ha un numero progressivo, da 1 a 100.
Ci saranno quindi 10 caselle per ognuna delle 10 righe.
Quando l'utente clicca su ogni cella, la cella cliccata si colora di azzurro ed emetto un messaggio in console con il numero della cella cliccata.

Per rendere il gioco più interessante, aggiungere una select accanto al bottone di generazione, che fornisca una scelta tra tre diversi livelli di difficoltà:

- con difficoltà 1 => 100 caselle, con un numero compreso tra 1 e 100, divise in 10 caselle per 10 righe;
- con difficoltà 2 => 81 caselle, con un numero compreso tra 1 e 81, divise in 9 caselle per 9 righe;
- con difficoltà 3 => 49 caselle, con un numero compreso tra 1 e 49, divise in 7 caselle per 7 righe;

### ipotesi soluzione uno

a) creare HTML statico di base e CSS di base
-- probabilmente la griglia di gioco non sarà presente in pagina al caricamento - solo il contenitore (board)
-- sicuramente bottone (opzione: select livello)

--utente clicca su bottone
--- generare la griglia di gioco (opzionale: in base al livello scelto o con un livello predefinito)
-- logica del gioco
-- Quando l'utente clicca su ogni cella, la cella cliccata si colora di azzurro ed emetto un messaggio in console con il numero della cella cliccata.

--campo minato (si avvia se clicco su bottone)
--- genero griglia (portabile)
--- logica del gioco (bingo)

-- bingo (si avvia se clicco su bottone)
---- genero griglia (portabile)
---- logica gioco (bingo)

## Seconda parte

Il computer deve generare 16 numeri casuali nello stesso range della difficoltà prescelta: le bombe.

- array di bombe (16) -> devo prevedere un numero di bombe e un numero range max di bombe ->

es. 100 caselle -> 16 bombe uniche con valori compresi tra 1 e 100
es. 81 caselle -> 16 bombe uniche con valori compresi tra 1 e 81
es. 49 caselle -> 16 bombe uniche con valori compresi tra 1 e 49

Attenzione: nella stessa cella può essere posizionata al massimo una bomba, perciò nell’array delle bombe non potranno esserci due numeri uguali.

In seguito l'utente clicca su una cella:

se il numero è presente nella lista dei numeri generati - abbiamo calpestato una bomba - la cella si colora di rosso e la partita termina. Altrimenti la cella cliccata si colora di azzurro e l'utente può continuare a cliccare sulle altre celle.

La partita termina quando il giocatore clicca su una bomba o quando raggiunge il numero massimo possibile di numeri consentiti (ovvero quando ha rivelato tutte le celle che non sono bombe).

Al termine della partita il software deve comunicare il punteggio, cioè il numero di volte che l’utente ha cliccato su una cella che non era una bomba.
