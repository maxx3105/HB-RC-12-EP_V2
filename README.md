# HB-RC-12-EP_V2
12 Tasten Fernbedienung mit E-Paper Display für Homematic

Zusätzlich die Option das E-Paper Display direkt anzuschließen und LiPo Akku per QI Ladefunktion aufzuladen.

Dieses Projekt basiert auf der Arbeit von [pa-pa](https://github.com/pa-pa/AskSinPP) ,[Jérôme](https://github.com/jp112sdl/HB-RC-4-Dis-TH) und [MajorTom](https://github.com/TomMajor/SmartHome/tree/master/PCB/HB-RC-12-EP).


# Hardware

### Bauteile

Bauteile                   | Bezeichnung          | Anzahl | Kommentar        | Quelle   |
-------------------------- | -------------------- | ------ | ------------ --- | -------- |
C1,C2,C14,C15,C16,C17      | 100nF, 10%, 50V      |   6    |  X7R-G0805 100N  |Reichelt  |
C18                        | 100µF/10V            |   1    | TAJ 3528 100/10  |Reichelt  |
D1                         | LED rot 12 mcd 160°  |   1    | OSO LHR974       |Reichelt  |
D2                         | LED grün 7.1 mcd 160°|   1    | OSO LGR971       |Reichelt  |
R1, R2                     | 1,5K Ohm             |   2    | RND 0805 1 1,5K  |Reichelt  |
R3                         | 10K Ohm              |   1    | RND 0805 1 10K   |Reichelt  |
U1                         | Atmega 1284P-AU      |   1    | TQFP44           |Reichelt  |
U2                         | CC1101               |   1    | 868Mhz Funkmodul |[eBay]      (https://www.ebay.de/itm/1-2-5PCS-CC1101-868MHZ-Kabellos-Modul-Long-Distance-Transmission-Antenne-1-8V/322983173720?ssPageName=STRK%3AMEBIDX%3AIT&var=512121286081&_trksid=p2057872.m2749.l2649)|
SW1-13                     | Taster 3x6x2,5mm     |  13    | DTSM-3           |[Aliexpress](https://de.aliexpress.com/item/32672806661.html)|
Q1                         | CSTCE8               |   1    | 8Mhz Resonator   |[Aliexpress](https://de.aliexpress.com/item/32436805954.html?spm=a2g0s.9042311.0.0.27424c4dFOxBvK)|


Bauteile ohne Hat          | Bezeichnung          | Anzahl | Kommentar        | Quelle |
-------------------------- | -------------------- | ------ | ---------------- | ------ |
C3-C13                     | 1µF, 10%, 25V        |  11    | KEM X5R0805 1,0U |Reichelt|
D3, D4, D5                 | MBR0530              |   3    | MBR0530T1G ONS   |Reichelt|
C3, ... C13                | 1µF, 10%, 25V        |  11    | KEM X5R0805 1,0U |Reichelt|
C3, ... C13                | 1µF, 10%, 25V        |  11    | KEM X5R0805 1,0U |Reichelt|
R8                         | 100K Ohm             |   1    | RND 0805 1 100K  |Reichelt|
R8-1,R8-2                  | 1,0 Ohm              |   2    | SMD-0805 1,00    |Reichelt|
Q2                         | IRLML 6346           |   1    | IRLML 6346       |Reichelt|
L1                         | Induktivität 68 µH   |   1    | L-1616FPS 68µ    |Reichelt|


Bauteile LiPo              | Bezeichnung          | Anzahl | Kommentar       | Quelle |
-------------------------- | -------------------- | ------ | --------------- | ------ |
C19,C20                    | 10uF, +-20%, 10V     |   2    | KEM X5R0805 10U |Reichelt|
D6                         | LED weiß 520 mcd 120°|   1    | SLO SMD-W0805-0 |Reichelt|
R9                         | 4,7K Ohm             |   1    | RND 0805 1 4,7K |Reichelt|
R10                        | 680 Ohm              |   1    | RND 0805 1 680  |Reichelt|
R11                        | 1K Ohm               |   1    | RND 0805 1 1,0K |Reichelt|
R13                        | 100K Ohm             |   1    | RND 0805 1 100K |Reichelt|
U3                         | MCP 1700T-3002E      |   1    | MCP 1700T-3002E |Reichelt|
U4                         | MCP 73831T-2ACI      |   1    | MCP 73831T-2ACI |Reichelt|

#### Sonstiges

~8,3 cm Draht als Antenne

### Programmieradapter
- 1x ISP (z.B. [diesen hier](https://www.diamex.de/dxshop/USB-ISP-Programmer-fuer-Atmel-AVR-Rev2))


# Software

### Fuses
Ext:  0xFF
High: 0xD2
Low:  0xE2

`C:\Program Files (x86)\Arduino\hardware\tools\avr\bin> .\avrdude -C ..\etc\avrdude.conf -p m644p -P com7 -c stk500 -U lfuse:w:0xE2:m -U hfuse:w:0xD2:m -U efuse:w:0xFF:m`


### Firmware

Projektverzeichnis: [HB-ES-PMSw1-Pl_GosundSP1](coming soon)

Benötigt werden die Bibliotheken [AskSinPP](https://github.com/pa-pa/AskSinPP) aus dem master-Branch, sowie die [HLW8012](https://github.com/xoseperez/hlw8012), die [MightyCore](https://github.com/MCUdude/MightyCore), die [EnableInterrupt](https://github.com/GreyGnome/EnableInterrupt) und [Low-Power](https://github.com/rocketscream/Low-Power).


# Bauanleitung

coming soon


# Kalibrierung

coming soon


# Bilder
![Vorderseite](https://github.com/maxx3105/HB-ES-PMSwX-Pl_Gosund/blob/main/HB-ES-PMSwX-Pl_Gosund_top.png)
![Rückseite](https://github.com/maxx3105/HB-ES-PMSwX-Pl_Gosund/blob/main/HB-ES-PMSwX-Pl_Gosund_bottom.png)
