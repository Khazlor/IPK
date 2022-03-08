# IPK Projekt 1 - jednoduchý HTTP server

## Autor

Vladimír Horák - xhorak72

## Popis funkce

Cílem projektu bylo vytvořit lehký HTTP server s minimem závislostí spustitelný na Linux Ubuntu 20.04 LTS.
Server je schopen zpracovat 3 příchozí požadavky:

#### GET http://servername:12345/hostname

Pošle zprávu obsahující síťové jméno počítače

#### GET http://servername:12345/cpu-name

Pošle zprávu obsahující informace o procesoru

#### GET http://servername:12345/load

Pošle zprávu obsahující aktuální zatížení procesoru

## Způsob použití

### Kompilace

Kompilace se provede pomocí příkazu make z příkazové řádky

### Spuštění serveru

Server se spustí pomocí spuštění programu hinfosvc s portem pro server v argumentu.

např:
```
$./hinfosvc 12345
```
spustí server na portu 12345

### Komunikace se serverem

Komunikace se dá provádět např. přes webový prohlížeč, nebo pomocí příkazové řádky

#### Webový prohlížeč

Pomocí zadání adresy serveru, jejího portu a požadavku

např:
```
$http://localhost:12345/hostname
$http://localhost:12345/cpu-name
$http://localhost:12345/load
```
funguje lokálně na zařízení kde běží server, z jiného zařízení se localhost musí nahradit IP adresou zařízení na kterém server běží

#### Příkazová řádka

Pomocí otevření nového terminálu a zadání příkazu curl a adresy jako u webového prohlížeče

např:
```
$curl http://localhost:12345/hostname
$curl http://localhost:12345/cpu-name
$curl http://localhost:12345/load
```

### Vypnutí serveru

Pomocí klávesové zkratky `ctrl + c` v terminálu kde server běží
