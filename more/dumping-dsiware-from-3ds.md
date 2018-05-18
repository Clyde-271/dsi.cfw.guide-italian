---
title: Eseguire il dump di DSiWare da 3DS
layout: single
sidebar:
  nav: "side"
---

Questa guida richiede un 3DS modificato con [Luma3DS](https://github.com/AuroraWright/Luma3DS){:target="_blank"} e [FBI](https://github.com/Steveice10/FBI){:target="_blank"} installati.
{: .notice--info}

Questa guida ti consentirà di eseguire il dump di titoli DSiWare che potrai poi utilizzare sul tuo DSi. Avrai bisogno di un 3DS modificato ed equipaggiato con Luma3DS. Leggi [3ds.hacks.guide](3ds.hacks.guide){:target="_blank"} per modificare il tuo 3DS.

## Ricerca del TitleID del DsiWare
1. Esegui l'applicazione FBI sul tuo 3DS
2. Scrolla in basso fino ad arrivare a "Titles" e premi **A**
3. Premi **Select** e poi **A** su "Show game card" e "Show SD"
4. Premi **B** e aspetta che lo schermo smetta di muoversi
5. Scrolla in basso fino al titolo DsiWare di cui vuoi fare il dump
6. Annotati il `Title ID` del DSiWare sulla parte superiore dello schermo
7. Spegni il 3DS

## Dump del DSiWare
1. Accendi il 3DS tenendo premuto **Start** per lanciare il chainloader menu di Luma3DS
2. Naviga fino a GodMode9 e premi **A** per lanciarlo
3. Portati su `[2:] SYSNAND TWLN/title/00030004`
4. La cartella contenente il gioco  di cui vuoi eseguire il dump è chiamata con  gli ultimi 8 numeri del TitleID del gioco
5. Premi **R+A** su questa cartella
6. Seleziona "Copy to `0:/gm9/out`"
7. Premi **A** quando la cartella sarà stata completamente copiata sulla tua Scheda SD
8. Spegni il 3DS

Il tuo dump dovrebbe adesso trovarsi nella tua scheda SD, per la precisione nella cartella `gm9/out`.

Questa guida non è ancora stata completata. La prossima sezione ti guiderà attraverso l'installazione del titolo DsiWare sul tuo DSi. Tieniti aggiornato per il suo rilascio.
