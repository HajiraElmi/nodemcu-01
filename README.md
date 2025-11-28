# nodemcu-01 Hajira Elmi 

## Introduktion
Detta projekt visar hur man skriver ett enkelt blinkprogram. Syftet är att förstå hur Arduino fungerar och hur man styr en inbyggd LED med kod. 
Vi kommer att använda oss av den här kitten.

<img width="350" height="343" alt="image" src="https://github.com/user-attachments/assets/2938e632-84aa-4e58-ba49-6824a49e556f" />


### Vad är Mikroprocessor?
Mikroprocessor fungerar som en minidator, du kan programmera det så att den styr saker, till exempel en lampa eller sensor.Den har också wifi och kan kopplas till internet. Det kan programmeras med Arduino IDE. 
Här är en bild på mikroprocessorESP8266 som vi ska använda under projektet

<img width="3000" height="3000" alt="image" src="https://github.com/user-attachments/assets/d0989e15-e498-4538-97f9-8820bbfd9d7f" />

### Hur fungerar Arduino IDE programmet? 

Arduino programmet består av två delar. 
```cpp
setup()
```
- kör en gång när programmet startar.

```cpp
   loop()
```
- kör om och om igen.
- Tänder och släcker LED-lampan

#### Portinitialisering
För att använda LED-lampan på NodeMCU måste vi berätta att pinnen ska fungera som utgång. 
```cpp
 pinMode(LED_BUILTIN, OUTPUT);
```

##### Kod exempel

```cpp
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);

 
}

// the loop function runs over and over again forever
void loop() {

  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  
  delay(1000);                      // wait for a second
  
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  
  delay(1000);                      // wait for a second
  
}
```
Det som händer här är att lED-lampan tänds i 1 sekund, släcks i 1 sekund, och försätter i en loop.
