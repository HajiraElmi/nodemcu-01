# nodemcu-01 Hajira Elmi 

## Introduktion
Projektet går ut på att en inbyggda LED-lampa ska blinka på en NodeMCU. 
Programeringen sker via Arduino IDE. 
### Vad är Mikroprocessor?
Mikroprocessor fungerar som en minidator, du kan programmera det så att den styr saker, till exempel en lampa eller sensor.Den har också wifi och kan kopplas till internet. Det kan programmeras med Arduino IDE. 

### Hur fungerar Arduino IDE programmet? 

Arduino programmet består av två delar. 
**setup()** 
- kör en gång när programmet startar.

  **loop()** 
- kör om och om igen.
- Tänder och släcker LED-lampan

#### Portinitialisering
För att använda LED-lampan på NodeMCU måste du ställa in pinnen som utgång. 
 pinMode(LED_BUILTIN, OUTPUT);

##### Kod exempel

the setup function runs once when you press reset or power the board
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

Det som händer här är att lED-lampan tänds i 1 sekund, släcks i 1 sekund, och försätter i en loop.
