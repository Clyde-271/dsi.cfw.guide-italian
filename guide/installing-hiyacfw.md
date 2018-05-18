---
title: Installazione di HiyaCFW
layout: single
sidebar:
  nav: "side"
---

Se si possiede una console di regione non USA, è necessario avere un exploit DSiWare già installato per continuare (ugopwn non è attualmente disponibile per console non USA).
{: .notice--info}

È necessario aver installato [Unlaunch](/guide/installing-unlaunch/) prima di continuare.
{: .notice--info}

Non effettuare aggiornamenti dopo aver installato HiyaCFW, in quanto le patch per la SD di HiyaCFW verrebbero rimosse.
{: .notice--danger}

HiyaCFW è un custom firmware per Nintendo DSi che, una volta installato, permetterà di:
- Avviare il sistema operativo da scheda SD
- Installare applicazioni homebrew sul Menù Home
- Avviare flashcart bloccate sulle versioni più recenti

## Requisiti
- L'ultima versione di [Python 3](https://www.python.org/downloads/){:target="_blank"}
  - Dovresti averlo già installato nella sezione precedente
- Una scheda SD da 2GB o meno, oppure una scheda SD più grande partizionata per essere da 2GB o meno
- L'ultima versione di [twlnf](https://github.com/Jimmy-Z/twlnf/releases){:target="_blank"}
- L'ultima versione di [HiyaCFW](https://github.com/Robz8/hiyaCFW/releases){:target="_blank"}
- L'ultima versione di [ugopwn](/assets/files/ugopwn.zip)
- [NUSDownloader](/assets/files/NUSDownloader.zip)
- Un backup della NAND del tuo dispositivo, con il footer di NO$GBA
  - twlnf crea questo footer automaticamente alla creazione di un backup
  - Dovresti già avere questo backup dalla sezione precedente 
- [Script d'aiuto per l'installazione di HiyaCFW](/assets/files/hiyacfw_helper.zip)

## Preparazione
1. Inserisci la scheda SD da <2GB nel computer
2. Copia *il contenuto* del file `.zip` di NUSDownloader in una cartella del PC
3. Copia *il contenuto* del file `.7z` di HiyaCFW in una cartella del PC
4. Copia *il contenuto* del file `.7z` dell'HiyaCFW helper nella cartella 'for PC' di HiyaCFW
5. Copia *il contenuto* del file '.zip' di ugopwn nella root della scheda SD da <2GB
6. Copia *il contenuto* del file '.7z' di twlnf nella root della scheda SD da <2GB, rinominando 'twlnf.nds' in 'boot.nds'
7. Copia il file 'console_id.txt' dalla root della scheda SD usata normalmente alla root della SD da <2GB,
  - Ovviamente, questo si applica solo se la tua SD da <2GB non è quella usata normalmente
8. Copia i file 'nand.bin' e 'nand.bin.sha' dalla root della scheda SD usata normalmente alla root della scheda SD da <2GB
9. Apri NUSDownloader sul tuo PC
  - Sui sistemi Mac/Linux/*nix bisogna utilizzare [Mono](http://www.mono-project.com/)
10. Seleziona la casella "Create Devrypted Contents (*.app"), e deseleziona la casella "Keep Enc. Contents"
11. Seleziona **Database > System (DSi) > System Menu (Launcher) > [Regione del tuo DSi] > v512 > Start NUS Download!**
12. Esci da NUSDownloader
13. Naviga in **titles > 00030017484e41XX > 512** nella cartella di NUSDownloader
14. Copia `00000002.app` dalla cartella `512` alla sottocartella `for PC` nella cartella di HiyaCFW
15. Copia il backup della tua NAND (`nand.bin`) nella cartella `for PC` di HiyaCFW

## Istruzioni
1. Inserisci la tua scheda <2GB nel tuo DSi
2. Accendi il tuo DSi
3. Apri Flipnote Studio
  - Assicurati che *Apri calendario all'avvio* sia disabilitato nelle impostazioni di Flipnote Studio
  - Se hai già installato un altro exploit DSiWare, utilizza quello, e riprendi dallo step 16
4. Seleziona **Visualizza > Scheda SD > Seleziona cartella > Utente > ugopwn**
5. Clicca sul Flipnote per metà rosso
6. Seleziona "Modifica"
7. Clicca sull'icona della rana in basso a sinistra
8. Clicca sull'icona della pellicola
9. Seleziona **Copia > Indietro > Esci"
10. Clicca sul secondo Flipnote
11. Clicca sull'icona della rana in basso a sinistra
12. Clicca sull'icona della pellicola
13. Clicca sul tasto con una sola freccia a destra (accanto all'ultimo tasto con due freccie) due volte
  - Verrà creato un nuovo foglio
14. Clicca  il tasto "Incolla" esattamente 122 volte
15. Clicca "Cancella" e poi "Incolla"
  - Ciò dovrebbe avviare twlnf
16. Premi **X** per montare la NAND direttamente
17. Premi **START** per aprire il menù di twlnf
18. Premi **R** per dumpare il contenuto della NAND sulla scheda SD
  - Il processo impiegerà qualche minuto
  - Mantieni il DSi collegato al caricatore durante la durata del processo, in modo da evitare che si spenga
  - Quando appare il testo `walk returned 0`, il processo è completato
19. Una volta finito, premi **Select** per uscire da twlnf
20. Premi **A** per confermare
  - La console si spegnerà
21. Inserisci la tua scheda SD da <2GB nel tuo PC
22. Sposta tutti i file dalla cartella `dump` alla root della scheda SD
  - Questo prepara la "SD NAND", dalla quale HiyaCFW si avvierà
23. Apri la cartella `for PC` di HiyaCFW
24. Esegui il file `hiyacfw_helper.py` per effettuare le modifiche necessarie
  - Questo script richiede [WINE](https://www.winehq.org/){:target="_blank"} sui sistemi Mac/Linux/*nix
25. Apri la cartella `Modified Files` appena creata
26. Copia il file `bootloader.nds` nella root della scheda SD da <2GB 
27. Copia il file 00000002.app nella cartella **title > 00030017 > 484e41XX > content** della scheda SD da <2GB
28. Copia *il contenuto* della cartella `for 2GB (or lower) SD card (SDNAND)` di HiyaCFW nella root della scheda SD da <2GB
29. Scollega la scheda SD da <2GB, e inseriscila nel DSi
30. Accendi la console
  - Dovrebbe apparire la schermata d'avvio di HiyaCFW

Il DSi d'ora in poi si avvierà dalla scheda SD invece che la NAND interna.

[Completamento dell'installazione](/guide/finalizing-setup){: .btn .btn--light-outline}
{: style="text-align: center;"}
