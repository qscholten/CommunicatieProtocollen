# Practicum 2 - Communicatie protocollen
## Qing Scholten (20208294)
1. Bij OTAA wordt er een Join-Request vanaf de device naar het netwerk gestuurd met een DevNonce, een AppEUI en een DevEUI. De netwerkserver ontvangt het bericht en controleert de DevNonce en genereert een 32-bits DevAddr van de 64-bits DevEUI. Vervolgens stuurt de netwerkserver een Join-accept met daarin de DLSettings, RXDelay en CFList. Hierna beschikken zowel de device als de netwerkserver over dezelfde AppNonce en DevNonce. Bij ABP worden er geen Join-Requests en Join-Accepts gestuurd. Hierdoor kan de ABP direct zenden zonder te wachten op een Join-accept. 
2. sys factoryRESET
3. System Commands, MAC Commands en Radio Commands
4. sys get vdd
5. mac get deveui
6. mac set appeui 0303030303030303
7. mac set appkey E05C89370B4CD40D96537FB9725457D2
8. De appkey wordt gebruikt voor authenticatie en beveiliging tijdens het activeren van de verbinding.
9. mac save, response is ok
10. OTAA
11. Er werd een Join-Request gestuurd vanuit de device en vervolgens werd de connectie geaccepteerd door de server die een Join-Accept stuurt naar de device.
![alt text](image-3.png)
12. Het Device Address is als een IP adres. Het dient als een identificatie adres binnen het netwerk. Het wordt gebruikt voor de adressering van dataverkeer.
13. De netwerk session key wordt gebruikt tussen een node en een netwerkserver om de Message Integrity Code van berichten te berekenen en te verifiëren en voor de encryptie en decryptie van data.
14. De app session key wordt gebruikt tussen een node en een applicatieserver voor een symmetrische 'shared key' om data te versleutelen.
15. De LoRa module zendt data naar een gateway. Vanaf de gateway wordt de data verzonden naar een netwerkserver en vervolgens naar The Things Network.
16. a. Frequency = 868100000\
    b. Spreading Factor = 12\
    c. Bandbreedte = 125000\
    d. Coding Rate = 4/5
17. 2
18. hhs-hboict-nse-delft, RSSI = -69
19. 1.155072s
20. -
21. -
22.  a. 
```
mac get ch freq 0
868100000
mac get ch freq 1
868300000
mac get ch freq 2
868500000
mac get ch freq 3
867100000
mac get ch freq 4
867300000
mac get ch freq 5
867500000
mac get ch freq 6
867700000
mac get ch freq 7
867900000
mac get ch freq 8
0
```
b. 
```
radio get freq
868100000
mac get rx2 868
3 869525000
```
c. 
```
mac get ch status 8
off
```
d. 
```
radio get pwr
14
```
Dit representeert het huidige powerlevel van de device. Deze ranget van -3 tot 15. \
e. radio get sf, de huidige waarde is sf12
```
radio get sf
sf12
```
f. radio get cr, de huidige waarde is 4/5
```
radio get cr
4/5
```
g. radio get bw, de huidige waarde is 125
```
radio get bw
125
```
h. Het zet de adaptive datarate aan.
```
mac set adr on 
invalid_param
mac set adr off
ok
```
i. Het geeft de huidige status van de device weer in Hex. De uitvoer betekent dat het netwerk gejoined is '1' en dat de kanalen geüpdated worden via CFList of NewChannelReq MAC command '8'
```
mac get status
00000810
```
j. Dit geeft een decimaal nummer die de duty cycle van het kannaal 2 representeert. De duty cycle van kanaal 2 is 100/(302+1) = 0.33 procent.
```
mac get ch dcycle 2
302
```
1.  
```
mac set ch freq <channelID> <frequency>
mac set ch drrange <channelID> <minRange> <maxRange>
mac set ch dcycle <channelID> <dutyCycle>
mac save
```

![alt text](image-4.png)

```
mac set ch freq 0 868100000
mac set ch drrange 0 0 5
mac set ch dcycle 0 302
mac save

mac set ch freq 1 868300000
mac set ch drrange 1 0 5
mac set ch dcycle 1 302
mac save

mac set ch freq 2 868500000
mac set ch drrange 2 0 5
mac set ch dcycle 2 302
mac save

mac set ch freq 3 867100000
mac set ch drrange 3 0 5
mac set ch dcycle 3 302
mac save

mac set ch freq 5 867500000
mac set ch drrange 5 0 5
mac set ch dcycle 5 302
mac save

mac set ch freq 6 867700000
mac set ch drrange 6 0 5
mac set ch dcycle 6 302
mac save

mac set ch freq 7 867900000
mac set ch drrange 7 0 5
mac set ch dcycle 7 302
mac save

mac set ch freq 8 868800000
mac set ch drrange 8 0 7
mac set ch dcycle 8 65535
mac save
```