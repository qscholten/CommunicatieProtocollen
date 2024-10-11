# Practicum 3
## Qing Scholten
1. 
```
Explicit Addressing Command Frame (API 1)

7E 00 16 11 5C 00 13 A2 00 41 92 98 20 FF FE 00 00 00 31 00 00 00 00 5C 00 C8

Start delimiter: 7E
Length: 00 16 (22)
Frame type: 11 (Explicit Addressing Command Frame)
Frame ID: 5C (92)
64-bit dest. address: 00 13 A2 00 41 92 98 20
16-bit dest. address: FF FE
Source endpoint: 00
Dest. endpoint: 00
Cluster ID: 00 31
Profile ID: 00 00
Broadcast radius: 00 (0)
Transmit options: 00
RF data (HEX): 5C 00
RF data (ASCII): \
```
2. De RF data is veranderd.
```
Explicit Addressing Command Frame (API 1)

7E 00 16 11 8C 00 13 A2 00 41 92 98 20 FF FE 00 00 00 31 00 00 00 00 8C 00 68

Start delimiter: 7E
Length: 00 16 (22)
Frame type: 11 (Explicit Addressing Command Frame)
Frame ID: 8C (140)
64-bit dest. address: 00 13 A2 00 41 92 98 20
16-bit dest. address: FF FE
Source endpoint: 00
Dest. endpoint: 00
Cluster ID: 00 31
Profile ID: 00 00
Broadcast radius: 00 (0)
Transmit options: 00
RF data (HEX): 8C 00
RF data (ASCII): Œ
```
3. AT commando is D2 (ASCII) en parameter value is 05 (HEX)
4.

```
Remote AT Command Request (API 1)

7E 00 10 17 01 00 13 A2 00 41 92 98 20 FF FE 02 44 32 04 2E

Start delimiter: 7E
Length: 00 10 (16)
Frame type: 17 (Remote AT Command Request)
Frame ID: 01 (1)
64-bit dest. address: 00 13 A2 00 41 92 98 20
16-bit dest. address: FF FE
Command options: 02
AT Command: 44 32 (D2)
Parameter: 04
Checksum: 2E
```
5.

- SM (Sleep Mode) = 0x04
- SP (sleep time) = 0x7D0
- ST (wake time) = 0xFA
- IR (IO Sampling Rate) = 0xC8
- SO (Sleep options) = 0x01

6. De ZED slaapt 20 seconden en ontvangt dan geen bericht en doet dan niks
7. SP (Sleep Time) aanpassen naar 0x7D0 op de ZC wat gelijk is aan de SP op de ZED.
