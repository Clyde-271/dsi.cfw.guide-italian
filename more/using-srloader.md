---
title: Utilizzo di SRLoader
layout: single
sidebar:
  nav: "side"
---

nds-bootstrap è attualmente un proof-of-concept, ed è ancora lontano dall'essere completo. Aspettati tempo di caricamento lunghi e problemi di compatibilità. È altamente consigliato consultare la [lista di compatibilità](https://docs.google.com/spreadsheets/d/1M7MxYQzVhb4604esdvo57a7crSvbGzFIdotLW0bm0Co/edit#gid=0){:target="_blank"}.
{: .notice--info}

SRLoader è un'applicazione homebrew che ti consente ti eseguire applicazioni homebrew, così come le ROM commerciali usando [nds-bootstrap](https://github.com/ahezard/nds-bootstrap){:target="_blank"}. SRLoader ha anche vari emulatori inclusi, incluso l' emulatore GBA, che di consentirà di eseguire ROM del Gameboy Color, NES e GBA.

Puoi saperne di più su SRLoader [qui](https://gbatemp.net/threads/srloader-gui-for-flashcards-also-a-nds-app-for-dsi.472200/){:target="_blank"}.

## Downloads

- L'ultima versione di [SRLoader](https://github.com/Robz8/SRLoader/releases)

## Installazione
1. Inserisci la Scheda SD della tua console sul computer
2. Copia il contenuto del file `.7z` di SRLoader nella root della Scheda SD
  - Se richiede di sostituire boot.nds, metti sì
3. Copia le ROM nelle loro rispettive cartelle
  - Metti le rom Gameboy in `/roms/gb`
  - Metti le rom NDS in `/roms/nds`
  - Metti le rom NES in `/roms/nes`
  - Per GBA, crea una cartella in `roms` chiamata `gba` e metti le rom lì
  - GBA richiede una copia del GBA BIOS nella root della Scheda SD chiamato `bios.bin`, attualmente non ha il supporto per i salvataggi

## Utilizzo
1. Avvia SRLoader utilizzando un entrypoint homebrew di tua scelta
2. Ora vedrai la lista delle tue ROM NDS
  - Premi **Y** per avviare applicazioni homebrew senza nds-bootstrap
  - Premi **A** per avviare ROM homebrew/commerciali utilizzando nds-bootstrap (Homebrew con DSi-extended header non verranno eseguiti da bootstap)
  - Premi **SELECT** per impostare una donor ROM quando la lista di compatibilità lo richiede
  - Premi **SU** o **GIÙ** per cambiare tra ROM NDS a DSiWare
  - Premi **START**, poi vai a **Start GBARunner2** per eseguire ROM GBA
  - Premi **B** per tornare al Menu DSi
