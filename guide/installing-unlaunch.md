---
title: Installazione di Unlaunch
layout: single
sidebar:
  nav: "side"
---

Se si possiede una console di regione non USA, è necessario avere un exploit DSiWare già installato per continuare.
{: .notice--info}

Unlaunch è attualmente in beta. Procedere con attenzione.
{: .notice--info}

Unlaunch è un exploit bootcode DSi che ti consentirà di installare HiyaCFW, un Custom Firmware per DSi, sulla tua console.

## Downloads
- L'ultima versione di [Unlaunch](http://problemkaputt.de/unlaunch.zip)
- L'ultima versione di [HBMenu](https://github.com/devkitPro/nds-hb-menu/releases/){:target="_blank"}
- L'ultima versione di [ugopwn](/assets/files/ugopwn.zip)
  - Solo per console di regione USA
- L'ultima versione di [twlnf](https://github.com/Jimmy-Z/twlnf/releases){:target="_blank"}
- L'ultima versione di [Python 3](https://www.python.org/downloads/){:target="_blank"}
- L'ultima versione di [DSi SRL Extractor](/assets/files/dsi_srl_extract.zip)

## Preparazione della Scheda SD

1. Installa Python 3 sul tuo computer
2. Apri l'applicazione Impostazioni
3. Seleziona **Gestione Dati > Console > Flipnote Studio > Copia > Sì**
	- Se Gestione Dati non appare, apri il DSi Shop, chiudilo e riprova
4. Una volta finito, spegni il dispositivo
5. Togli la Scheda SD dalla console e inseriscila nel Computer
6. Copia il contenuto del file `.zip` di ugopwn nella root della tua Scheda SD
  - Solo per console di regione USA
7. Copia il contenuto del file `.7z` di twlnf nella root della tua Scheda SD, e rinomina `twlnf.nds` a `boot.nds`
8. Copia il contenuto del file `.zip` di DSi SRL Extractor in una cartella sul tuo Desktop
9. Apri la Scheda SD sul tuo computer
10. Naviga a /Private/DS/Title/
11. Copia il file `.bin` nella cartella di DSi SRL Extractor
12. Esegui il file console_id `.py` dentro la cartella
  - Questo script richiede [WINE](https://www.winehq.org/){:target="_blank"} su sistemi Mac/Linux/*nix
13. Quando richiesto, premi Invio
14. Copia il nuovo file console_id `.txt` nella root della Scheda SD
15. Espelli la Scheda SD e inseriscila nuovamente nel DSi

## Creazione di un backup della NAND

1. Apri l'applicazione Flipnote Studio
  - Assicurati che l'opzione *Apri calendario all'avvio* sia disabilitata nelle impostazioni di Flipnote Studio
  - Se hai già un exploit DSiWare installato, apri quello e salta al Passo 14
2. Seleziona **Visualizza > Scheda SD > Seleziona Cartella > User > ugopwn**
3. Clicca sul Flipnote per metà rosso
4. Seleziona "Modifica"
5. Clicca sull'icona della rana in basso a sinistra
6. Clicca sull'icona del rullino
7. Seleziona **Copia > Indietro > Esci**
8. Clicca sul seondo flipnote.
9. Clicca sull'icona della rana in basso a sinistra
10. Clicca sull'icona del rullino.
11. Clicca sul tasto con una sola freccia a destra (accanto all'ultimo tasto con due freccie) due volte
  - Verrà creato un nuovo foglio
12. Clicca il tasto incolla esattamente 122 volte.
13. Seleziona "Cancella" e poi "Incolla"
  - Ciò dovrebbe avviare twlnf
14. Quando richiesto, premi **A** per creare un backup della NAND
  - Questo richiederà qualche minuto
  - Mantieni questo Backuo della NAND in un luogo sicuro, è un backup critico e ci servirà dopo per installare HiyaCFW
15. Premi **B** per uscire da twlnf
  - La console si spegnerà

## Installazione

1. Inserisci la Scheda SD nel tuo Computer
2. Copia `BOOT.NDS` dalla cartella `hbmenu` nel file `.tar.bz2` di HBMenu nella root della Scheda SD
  - twlnf è attualmente il tuo `boot.nds`; per ora, rinominalo in `boot.bak` oppure `twlnf.nds`
3. Copia `UNLAUNCH.DSI` dal file `.zip` di Unlaunch nella root della Scheda SD
4. Rinomina `UNLAUNCH.DSI` a `unlaunch.nds`
5. Rimuovi la Scheda SD e inseriscila nel DSi
6. Accendi il tuo DSi, e ripeti i passi da 1 fino a 13 in **Creazione di un backup della NAND**
  - HBMenu dovrebbe apparire
7. Naviga a `unlaunch.nds`, e premi **A**
  - L'installer di Unlaunch dovrebbe apparire
8. Naviga a `INSTALL NOW` e premi **A**
  - Se Unlaunch si blocca a `LOADING FAT`, leggi il nostro [FAQ](/help/faq)
9. Una volta fatto, naviga a `POWER DOWN` e premi **A**
  - Il DSi si spegnerà
10. Accendi la console per verificare che Unlaunch sia stato installato correttamente
  - Dovresti vedere brevemente la schermata di Unlaunch, e avviarti in una versione del menu DSi senza suoni

Con Unlaunch installato, il tuo sistema ha una protezione dai brick di base, a meno che il file TMD del launcher non venga distrutto. Unlaunch ha protezioni che dovrebbero impedire questo dal succedere, e HiyaCFW usa la tua Scheda SD come NAND del DSi, facendo così il sistema teoricamente non brickabile.

[Installazione di HiyaCFW](/guide/installing-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}
