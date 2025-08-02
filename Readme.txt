=======================================
  Secure Password Generator (SPG)
=======================================

Un generatore di password avanzato che funziona interamente nel tuo browser, garantendo che nessun dato lasci il tuo computer.


VERSIONI
--------

* SPGonline.html:
  - DESCRIZIONE: Versione standard che richiede una connessione internet per scaricare una libreria esterna (CryptoJS).
  - USO: Ideale per un uso rapido e conveniente.

* SPGoffline.html:
  - DESCRIZIONE: Versione di massima sicurezza che include la libreria localmente e non richiede connessione internet.
  - USO: Consigliata per la massima privacy e per l'uso in ambienti senza rete.


CARATTERISTICHE TECNICHE
------------------------
*   Entropia del Mouse: La casualità viene generata dai movimenti del mouse.
*   Hashing Robusto: Il seed viene processato 10.000 volte con l'algoritmo SHA-512 per renderlo più sicuro.
*   Doppia Fonte di Casualità: Combina l'entropia del mouse con l'API crittografica nativa del browser (crypto.getRandomValues).
*   Libreria Utilizzata: CryptoJS versione 4.1.1.
*   100% Client-Side: Nessuna comunicazione con server esterni.


COME USARE
----------

1.  SPGonline.html:
    Apri il file in un qualsiasi browser moderno con una connessione a internet.

2.  SPGoffline.html:
    Assicurati che la cartella "js" (contenente il file "crypto-js.min.js") si trovi nella stessa directory del file HTML. Apri il file nel browser; funzionerà anche senza internet.


AVVERTENZA DI SICUREZZA
-----------------------
Il "seed" visualizzabile è la chiave master per rigenerare la password. Trattalo con la massima riservatezza. Non salvarlo in luoghi non sicuri.