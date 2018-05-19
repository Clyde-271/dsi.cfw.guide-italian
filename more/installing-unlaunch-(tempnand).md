---
title: Installazione Unlaunch (TempNAND)
layout: single
toc: true
sidebar:
  nav: "side"
---

Se non hai già un exploit DSiWare installato, devi avere una console di regione USA con Flipnote Studio installato, o una modifica hardware capace di installare DSiWare.
{: .notice--info}

Questo metodo **degrada gravemente** la NAND e dev'essere usato come **ultima risorsa**.
{: .notice--danger}

## Requisiti

- L'ultima versione di [Unlaunch](http://problemkaputt.de/unlaunch.zip)
- L'ultima versione di [ugopwn](/assets/files/ugopwn.zip)
  - Solo per console di regione USA
- L'ultima versione di [fwTool](/assets/files/fwTool_1.6.zip)
- L'ultima versione di [TempNAND](https://github.com/ThisIsDaAccount/TempNand/releases/latest){:target="_blank"}
- L'ultima versione di [Java](https://java.com/en/download/){:target="_blank"}
- L'ultima versione di [Python 3](https://www.python.org/downloads/){:target="_blank"}
- L'ultima versione di [DSi SRL Extractor](/assets/files/dsi_srl_extract.zip)
- L'ultima versione di [No$GBA](http://problemkaputt.de/gba.htm){:target="_blank"}
- Un file rom `.nds` qualsiasi

## Preparazione Scheda SD

1. Copia il contenuto del file `.zip` di fwTool nella root della Scheda SD
2. Rinomina il file `.nds` di fwTool a `boot.nds`
3. Copia il contenuto del file `.zip` di ugopwn nella root della Scheda SD
  - Solo per console di regione USA

## Dump dei file chiave

1. Apri l'applicazione Impostazioni
2. Seleziona **Gestione dati > Console > Flipnote Studio > Copia > Sì**
	- Se Gestione Dati non appare, apri il DSi Shop, chiudilo e riprova
3. Torna al Menu DSi
1. Apri l'applicazione Flipnote Studio
  - Assicurati che l'opzione *Apri calendario all'avvio* sia disabilitata nelle impostazioni di Flipnote Studio
  - Se hai un'altro exploit DSiWare installato, apri quello e salta al Passo 17
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
  - Ciò dovrebbe avviare fwTool
14. Seleziona le opzioni `Dump CID` e `Dump BIOS`
15. Seleziona `Dump  nand_dsi.bin`
  - Questo richiederà qualche minuto
15. Una volta fatto, spegni la console

## Preparazione per TempNAND e No$GBA

1. Scarica ed estrai il file `.zip` di No$GBA in una cartella sul Desktop
2. Inserisci la Scheda SD nel computer
3. Apri la cartella con numeri casuali nella Scheda SD
4. Copia il BIOS DSi alla cartella di NO$GBA
4. Copia il file `nand_dsi.bin` in un posto sicuro sul tuo computer
5. Rinomina il file `nand_dsi.bin` a `clean_nand_dsi.bin`
6. Copia il file `CID.bin` in un posto sicuro sul tuo computer
7. Copia i contenuti del file `.zip` di Unlaunch in una cartella sul Desktop
8. Copia i contenuti del file DSi `.zip` di SRL Extractor in una cartella sul Desktop
9. Vai a /Private/DS/Title/ sulla tua Scheda SD
10. Copia il file `.bin` nella cartella di DSi SRL Extractor
11. Esegui il file `console_id.py` dentro la cartella
  - Questo script richiede [WINE](https://www.winehq.org/){:target="_blank"} su sistemi Mac/Linux/*nix
12. Quando richiesto, premi Invio
13. Copia il nuovo file `console_id.txt` in un posto sicuro sul tuo computer
zip
## Using TempNAND

1. Scarica ed estrai il file `.zip` di TempNAND da qualche parte sul Computer
2. Apri il file `.jar` di TempNAND
  - Assicurati di avere Java installato
3. Vai nella scheda setup
4. Seleziona **Console ID > get Console ID from file**
5. Seleziona il file `console_id.txt` preso in precedenza
6. Seleziona **CID > get CID from file**
7. Seleziona il file `CID.bin` preso in precedenza
8. Seleziona **File > Open Encrypted NAND**
9. Seleziona il file `clean_nand_dsi.bin` preso in precedenza
  - Potrebbe richiedere qualche secondo
  - Se sembra essersi bloccato, dalli tempo
10. Seleziona "Install Unlaunch"
11. Seleziona il file `unlaunch.dsi` dal file `.zip` di Unlaunch che hai estratto in precedenza
12. Seleziona **File > Save As**
13. Salva una copia del backup della NAND per utilizzarlo più tardi
14. Rinominalo in `unlaunch_nand_dsi.bin`
15. Seleziona **File > Save for No$GBA**
16. Salva il file nella cartella di No$GBA
17. Rinomina il backup della NAND di No$GBA in `DSI-1.mmc`

## Test della NAND

1. Apri No$GBA
2. Seleziona **Options > Emulation Setup**
3. Imposta "Reset/Startup Entrypoint" a "GBA/NDS BIOS (Nintendo Logo)"
4. Imposta "NDS Mode Colors" a "DSi (retail/16MB)"
5. Seleziona **Save Now > OK**
6. Seleziona **File >> Cartridge Menu (FileName)**
7. Apri il file `.nds`

La tua NAND verrà emulata da No$GBA. Se non funziona, il backup della NAND non è sicuro da usare e non è sicura flasharla sul DSi.

Se il backup funziona su No$GBA, continua pure nella prossima sezione.

## Flash della NAND

1. Copia il file `unlaunch_nand_dsi.bin` nella cartella creata da fwTool
2. Elimina il file `nand_dsi.bin` sulla Scheda SD
  - Assicurati di avere il backup originale sul Computer!
3. Rinomina `unlaunch_nand_dsi.bin` in `nand_dsi.bin`
4. Apri l'applicazione Flipnote Studio
  - Assicurati che l'opzione *Apri calendario all'avvio* sia disabilitata nelle impostazioni di Flipnote Studio
  - Se hai un'altro exploit DSiWare installato, apri quello e salta al Passo 16
5. Seleziona **Visualizza > Scheda SD > Seleziona Cartella > User > ugopwn**
6. Clicca sul Flipnote per metà rosso
7. Seleziona "Modifica"
8. Clicca sull'icona della rana in basso a sinistra
9. Clicca sull'icona del rullino
10. Seleziona **Copia > Indietro > Esci**
11. Clicca sul seondo flipnote.
12. Clicca sull'icona della rana in basso a sinistra
13. Clicca sull'icona nel rullino
14. Clicca sul tasto con una sola freccia a destra (accanto all'ultimo tasto con due freccie) due volte
  - Verrà creato un nuovo foglio
15. Clicca il tasto incolla esattamente 122 volte.
16. Seleziona "Cancella" e poi "Incolla"
  - Ciò dovrebbe avviare fwTool
17. Seleziona "Restore `nand_dsi.bin`"
  - Richiederà qualche minuto
18. Una volta finito, spegni la console

Con Unlaunch installato, il tuo sistema ha una protezione dai brick di base, a meno che il file TMD del launcher non venga distrutto. Unlaunch ha protezioni che dovrebbero impedire questo dal succedere, e HiyaCFW usa la tua Scheda SD come NAND del DSi, facendo così il sistema teoricamente non brickabile.

[Installazione di HiyaCFW](/guide/installing-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}
