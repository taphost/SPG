========================================
    Secure Password Generator (SPG) 
========================================

Un generatore di password avanzato che funziona interamente nel tuo browser,
garantendo che nessun dato lasci il tuo computer. Questa versione introduce
fonti di entropia multiple per una sicurezza ancora maggiore.


VERSIONI
--------

* SPGonline.html:
  - DESCRIZIONE: Versione standard che richiede una connessione internet per
    scaricare una libreria esterna (CryptoJS).
  - USO: Ideale per un uso rapido e conveniente.

* SPGoffline.html:
  - DESCRIZIONE: Versione di massima sicurezza che include la libreria
    localmente e non richiede connessione internet.
  - USO: Consigliata per la massima privacy e per l'uso in ambienti senza rete.


CARATTERISTICHE TECNICHE
------------------------

*   ENTROPIA FISICA E TEMPORALE: La casualità non è più basata solo sui
    movimenti del mouse, ma viene raccolta da molteplici fonti, tra cui:
        - Coordinate del mouse e degli eventi touch (compatibile con
          smartphone e tablet).
        - Intervalli di tempo (delta) tra ogni singolo movimento o tocco.
        - Tempo totale trascorso dal caricamento della pagina al momento
          della generazione della password.

*   HASHING ROBUSTO: Il seed grezzo viene processato 10.000 volte con
    l'algoritmo SHA-512 per massimizzare la resistenza agli attacchi.

*   MOLTEPLICI FONTI DI CASUALITA': Il sistema combina l'entropia generata
    dall'utente (fisica e temporale) con la casualità crittografica fornita
    dall'API nativa del browser (crypto.getRandomValues) per un risultato
    finale imprevedibile.

*   LIBRERIA UTILIZZATA: CryptoJS versione 4.1.1.

*   100% CLIENT-SIDE: Tutta l'elaborazione avviene localmente nel tuo
    browser. Nessun dato, password o seed viene mai inviato a un server
    esterno.


COME USARE
----------

1.  APRI IL FILE:
    - SPGonline.html: Apri il file in un qualsiasi browser moderno con una
      connessione a internet.
    - SPGoffline.html: Assicurati che la cartella "js" si trovi nella stessa
      directory del file HTML. Funzionerà anche offline.

2.  RACCOGLI ENTROPIA: Muovi il mouse in modo casuale all'interno della
    finestra del browser o, se sei su un dispositivo touch, tocca e scorri
    ripetutamente sullo schermo. DEVI CONTINUARE FINCHE' L'INDICATORE NON
    RAGGIUNGE 1000/1000 PUNTI. La generazione della password non sarà
    possibile prima del completamento di questo passaggio.

3.  CONFIGURA LA PASSWORD: Scegli la lunghezza desiderata e i set di
    caratteri (maiuscole, minuscole, numeri, simboli).

4.  GENERA: Clicca sul pulsante "Genera Password". La password apparirà
    nell'apposito riquadro.


AVVERTENZE DI SICUREZZA
-----------------------

*   GESTIONE DEL SEED: Il "seed" visualizzabile (opzionale) è la chiave
    master per rigenerare la stessa password. Non salvarlo mai in luoghi
    non sicuri e trattalo con la massima riservatezza.

*   RISCHIO DEL SALVATAGGIO IN .TXT: Salvare una password in un file di
    testo semplice (.txt) è ALTAMENTE SCONSIGLIATO poiché il file non è
    crittografato e può essere letto da chiunque abbia accesso al tuo
    dispositivo. L'applicazione mostrerà un avviso prima di consentire il
    download. Usa questa funzione solo temporaneamente e cancella il file
    non appena hai trasferito la password in un gestore di password sicuro.
