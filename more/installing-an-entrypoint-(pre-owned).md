---
title: Installazione di un entrypoint (titolo già acquistato)
layout: single
sidebar:
  nav: "side"
---

Attalmente questa guida supporta solo console di regione USA.
{: .notice--info}

Adessi utilizzeremo degli script già esistenti per semplificare l'installazione di un entrypoint homebrew. Questi entrypoint permettono di avviare homebrew pochi secondi dopo l'avvio dell'applicazione.

4swordshax permette nsolamente di utilizzare emulatori e applicazioni homebrew. Se si vogliono eseguire ROM retail usand SRLoader, si consiglia di installare [sudokuhax](/guide/installing-sudokuhax) instead of 4swordshax.

## Requisiti

*Il [packetto d'installazione di entrypoint per twlnf](/assets/files/twlnf-entrypoint-pack.zip)

## Preparazione

1. Inserisci la scheda SD nel computer
2. Copia il contenuto del file `.zip` dell'installazione dell'entrypoint per twlnf nella root della scheda SD
3. Scollega la scheda SD e inseriscila nel DSi

## Avvio di twlnf

1. Apri Flipnote Studio
  - Assicurati che *Apri calendario all'avvio* sia disabilitato nelle impostazioni di Flipnote Studio
2. Seleziona **Visualizza > Scheda SD > Seleziona cartella > Utente > ugopwn**
3. Clicca sul Flipnote per metà rosso
4. Seleziona "Modifica"
5. Clicca sull'icona della rana in basso a sinistra
6. Clicca sull'icona della pellicola
7. Seleziona **Copia > Indietro > Esci"
8. Clicca sul secondo Flipnote
9. Clicca sull'icona della rana in basso a sinistra
10. Clicca sull'icona della pellicola
11. Clicca sul tasto con una sola freccia a destra (accanto all'ultimo tasto con due freccie) due volte
  - Verrà creato un nuovo foglio
12. Clicca  il tasto "Incolla" esattamente 122 volte
13. Clicca "Cancella" e poi "Incolla"
  - Ciò dovrebbe avviare twlnf

## Installazione dell'entrypoint

1. Se viene chieso in twlnf, premi **A** per creare un backup della NAND
  - Il processo impiegerà qualche minuto
  - Salva questo backup in una posizione sicura, in quanto si tratta di un backup estremamente importante
2. Premi **X** per momtare la NAND direttamente
  - twlnf non visualizza questa opzione tra le operazioni possibili
3. Seleziona lo script in formato .nfs corrispondente al DSiWare installato sulla console
  - Fieldrunners - `install_fieldrunhax_usa.nfs`
  - Legends of Exidia - `install_exidiahax_usa.nfs`
  - Guitar Rock Tour - `install_grtpwn_usa.nfs`
  -  The Legend of Zelda: Four Swords Anniversary - `install_4swordshax_usa.nfs`
4. Premi **A** per eseguire lo script
  - Se viene visualizzato un errore, non hai installato il DSiWare corrispondente
5. Premi **A** per installare l'applicazione nella NAND
6. Una volta finito, premi **Select** per uscire da twlnf
7. Premi **A** per confermare
  - La console si spegnerà

## Avvio dell'entrypoint

1. Accendi la console
2. Open your exploited application
3. Esegui uno dei seguenti passaggi:
  - Fieldrunners - Attendi il caricamento del gioco, poi seleziona **Scores** nel menù principale
  - Legends of Exidia - Attendi il passaggio delle due schermate d'avvio, seleziona il primo salvataggio e premi **Continue**
  - Guitar Rock Tour - Scendi giù, poi premi **High Scores** > **Drums** > **Easy**
  -  The Legend of Zelda: Four Swords Anniversary - JBasta avviare il gioco, 4swordshax non richiede nessuna interazione 

Adesso l'entrypoint caricherà qualsiasi homebrew sulla scheda SD salvato come `boot.nds`.