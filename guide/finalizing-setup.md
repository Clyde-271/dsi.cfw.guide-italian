---
title: Completamento dell'Installazione
layout: single
sidebar:
  nav: "side"
---

Installeremo adesso l'SRLoader nel Menu di Sistema copiandolo nella tua scheda SD.

SRLoader è un'applicazione homebrew che può eseguire homebrew e ROM retail. Ha inoltre diversi emulatori inclusi.

## Downloads

- L'ultima release di [SRLoader](https://github.com/Robz8/SRLoader/releases){:target="_blank"}

## Istruzioni

1. Inserisci la tua scheda SD (<2GB) che fungerà da NAND SD
2. Copia *i contenuti di* `CFW - SDNAND root` dal file `.7z` dell'SRLoader sulla root della tua scheda NAND SD (<2GB)
3. Copia le cartelle `_nds` e `roms` dal file `.7z` dell'SRLoader nella root della tua SD Card
4. Rimuovi la tua scheda SD e inseriscila nel DSi
5. Avvia il sistema
6. "Apri" il nuovo pacco regalo premendo su di esso
    - L'SRLoader dovrebbe apparire

L'SRLoader dovrebbe essere adesso nel tuo Menu Principale, dove si trovano solitamente gli altri titoli DSiWare. Con l'SRLoader potrai eseguire homebrew e ROM retail, oltre ad usare diversi emulatori inclusi nel software.

## Utilizzo

1. Copia le ROM nelle loro rispettive cartelle
  - Metti le rom Gameboy in `/roms/gb`
  - Metti le rom NDS in `/roms/nds`
  - Metti le rom NES in `/roms/nes`
  - Per GBA, crea una cartella in `roms` chiamata `gba` e metti le rom lì
  - GBA richiede una copia del GBA BIOS chiamto `bios.bin` nella root della Scheda SD, e attualmente non ha il supporto per i            salvataggi
2. Avvia l'SRLoader dal Menu Principale
3. Ora vedrai la lista delle tue ROM NDS
  - Premi **Y** per avviare applicazioni homebrew senza nds-bootstrap
  - Premi **A** per avviare ROM homebrew/commerciali utilizzando nds-bootstrap (Homebrew con DSi-extended header non verranno eseguiti da bootstap)
  - Premi **SELECT** per impostare una donor ROM quando la lista di compatibilità lo richiede
  - Premi **SU** o **GIÙ** per cambiare tra ROM NDS a DSiWare
  - Premi **START**, poi vai a **Start GBARunner2** per eseguire ROM GBA
  - Premi **B** per tornare al Menu DSi
