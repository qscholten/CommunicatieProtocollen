# Practicum 2 - Communicatie protocollen
## Qing Scholten (20208294)

1. Omdat er een uplink-bericht nodig is van de device om het downlink-bericht naar de device te verzenden.
2.
```
mac tx cnf 1 66
ok
mac_rx 1 03
```
4.
![alt text](image-5.png)

5. Duty cycle is het percentage van de tijd dat een apparaat mag zenden.

6. 865-868.6 MHz is de duty cycle <1,0%, 868.7-869.2 MHz is de duty cycle <0,01%, 869.4-869.65 MHz is de duty cycle <10%

7. De uplink airtime per node is gelimiteerd tot 30 seconden per dag en de downlink berichten zijn gelimiteerd tot 10 berichten per dag per node.

8. Symbol time wordt berekend door $T_s=\frac{2^{SP}}{BW}$. In dit geval is dat $T_s = \frac{2^7}{125}=\frac{128}{125000} = 0.001024$. Dit is de on air time voor een 1 byte bericht. Met 30 seconden airtime per dag mag je $30/0.001024$ is ongeveer 29296 berichten versturen.

9. Door gebruik van een lagere spreadingsfactor of een hogere bandbreedte.

10. 
01 - RSSI = -71 en SNR = 9.25\
02 - Gateway is afwezig, dus niet aangestraald\
03 - RSSI = -106 en SNR = -4
Doordat 01 dichter bij de Gateway is gezonden, is de RSSI hoger en daardoor ook de SNR. Doordat bij 02 er te veel interferentie (Tuinhuis is heel afgezonderd en er zit veel muren tussen het tuinhuis en de gateway) was is de gateway van NSE niet aangestraald. Bij 03 is er minder interferentie doordat het bericht buiten is verzonden en er dus minder muren tussen zaten, maar het is verder weg van de gateway dan 01.