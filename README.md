# Blinkprogram på NodeMCU

## Översikt
Blinkprogram är ett simpel designat program som får LED på NodeMCU att blinka. Detta är ett bra första testprogram för nya studenter. 
## Mikroprocessor 
NodeMCU är en liten mikrokontrollbaserad ''mini-dator'', som man kan progammera och styra för olika projekt. Den kan köra enkel kod och kopplas till LED, sensorer osv.
## Två basfunktionera i Arduino 
`setup()` - körs en gång nör programmet startar

`loop()`- körs om repetetivt 
## Portinitialisering 
LED kopplad till ´LED_BUILTIN´ förbereds som utgång för att styras av programmet:

![MikroBILD](https://github.com/user-attachments/assets/7267f7f1-7014-44fe-85a2-b470138dafe8) 

Det betyder att kodningen sker via Arduino, där man bestämmer ifall pinnen ska vara en input eller output, alltså en ingång eller utgång. 
## Kodförklaring


```C++
void setup() {
  pinMode(LED_BUILTIN, OUTPUT); // LED som utgång
}

void loop() {
  digitalWrite(LED_BUILTIN, LOW);  // Tänd LED
  delay(500);                       // Vänta 0,5 s
  digitalWrite(LED_BUILTIN, HIGH); // Släck LED
  delay(500);                       // Vänta 0,5 s
}



