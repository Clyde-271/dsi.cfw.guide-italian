---
title: Installazione di Sudokuhax
layout: single
sidebar:
  nav: "side"
---

Attalmente questa guida supporta solo console di regione USA.
{: .notice--info}

Assicurati di avere almeno 30 blocchi liberi sulla memoria interna della tua console, altrimenti **causeresti un brick**!
{: .notice--danger}

sudokuhax è un exploit del gioco DSiWare "Sudoku", consentendo di avviare l'Homebrew Launcher pochi secondi dopo aver avviato l'applicazione.

Per usare il link magnet [magnet](https://en.wikipedia.org/wiki/Magnet_URI_scheme) in questa pagina, avrai bisogno di un client torrent come [Deluge](https://dev.deluge-torrent.org/wiki/Download).

## Requisiti
- <i class="fa fa-magnet" aria-hidden="true" title="Questo è un link magnet. È necessario un client torrent per scaricare questo file."></i> -  [sudokuhax](magnet:?xt=urn:btih:fd4dcb2f954f48adb2af96326609f9c3f3ae2a7a&dn=sudokuhax.zip&tr=http%3a%2f%2ftracker.tfile.me%2fannounce&tr=udp%3a%2f%2f9.rarbg.com%3a2710%2fannounce&tr=udp%3a%2f%2fexplodie.org%3a6969%2fannounce&tr=udp%3a%2f%2ftorrent.gresille.org%3a80%2fannounce&tr=udp%3a%2f%2ftracker.yoshi210.com%3a6969%2fannounce&tr=http%3a%2f%2fexplodie.org%3a6969%2fannounce&tr=http%3a%2f%2ftracker1.wasabii.com.tw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=udp%3a%2f%2fp4p.arenabg.com%3a1337%2fannounce&tr=http%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.tiny-vps.com%3a6969%2fannounce&tr=http%3a%2f%2ftorrent.gresille.org%2fannounce&tr=udp%3a%2f%2ftracker.filetracker.pl%3a8089%2fannounce&tr=http%3a%2f%2ftracker.aletorrenty.pl%3a2710%2fannounce&tr=udp%3a%2f%2fzer0day.ch%3a1337%2fannounce&tr=http%3a%2f%2fp4p.arenabg.com%3a1337%2fannounce&tr=http%3a%2f%2ftracker.baravik.org%3a6970%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.aletorrenty.pl%3a2710%2fannounce&tr=udp%3a%2f%2ftracker.leechers-paradise.org%3a6969%2fannounce)

## Preparazione

1. Inserisci la scheda SD nel computer
2. Copia il contenuto del file `.zip` di sudokuhax nella root della scheda SD
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

## Installazione di sudokuhax
1. Se viene chieso in twlnf, premi **A** per creare un backup della NAND
  - Il processo impiegerà qualche minuto
  - Salva questo backup in una posizione sicura, in quanto si tratta di un backup estremamente importante
2. Premi **X** per momtare la NAND direttamente
  - twlnf non visualizza questa opzione tra le operazioni possibili
3. Apri la cartella `sudoku/content`
4. Seleziona il file `title.tmd`
5. Premi **A** per installare l'applicazione nella NAND
6. Una volta finito, premi **Select** per uscire da twlnf
7. Premi **A** per confermare
  - La console si spegnerà

## Avvio di sudokuhax

1. Accendi la console
2. Premi sul pacco regalo nel Menù Home per "scartare" Sudoku
3. Apri l'applicazione
4. Attendere il passaggio delle schermate ESRB ed EA
5. Quando ti viene chiesto, premi sul touch screen per avviare l'entrypoint

Adesso sudokuhax caricherà qualsiasi homebrew sulla scheda SD salvato come `boot.nds`
