
### Arkitektur 

<img src="/img/espbild.jpg">

# Beskrivning av projekt

* 1. 
Jag använda mig utav DHT11 som har en Temp och Humidity sensor     

* 2. 
Använder en ESP8266 D1mini fick löda ihop lita pina för att få den att funka, en billig mikrokontroller som har inbyggt WiFi. 

* 3. 
Koden är skriven på arduino ide, koden kan ni se på (MainESP.ino, Secrets.h)


* 4. 
uppkopplingen är gjord med MQTT, MQTT är ett lätt, publicera och prenumerera meddelandeprotokoll som ofta används i IoT-applikationer eftersom det tillåter enheter att kommunicera med en server på ett effektivt och resursbesparande sätt. Där du skapar en publisher vilket är Temp i mitt fall, och sen subscriber och iot connectionen, sen övervaka man MQTT-meddelande som skickas in till mitt AWS-konto 


* 5. 
AWS iot-core Detta gör det möjligt för oss utvecklare att fokusera på att bygga sina applikationer utan att behöva oroa sig för den underliggande infrastrukturen.

* 6. 
AWS Iot-Core och Amazon DynamoDB integreras så jag hämtar och lagra datan från min sensor, IoT Core är en hanterad molnplattform som gör att du enkelt och säkert kan ansluta. 
Jag lagra allting på DynamoDB-tabell för senare analys och hämtning

* 7. 

Med AWS Lambda kör jag en Json kod för praktiskt göra en API förfrågan från OpenWheater som jag sedan lagrar i samma DynamoDB-tabell, Använder också API Gateway övervaka och lagra utomhus data, API Gateway låter dig skapa API:er som får åtkomst till AWS-tjänster

* 8. 
Amazon QuickSight är en snabb, molndriven business intelligence-tjänst som jag gör det enkelt att göra en visualisering och en korrelation på den datan jag har fått från min sensor och från API Openwheather



## **Målet med projektet**


Målet med detta projekt är att demonstrera hur man ansluter en ESP8266 mikrokontroller med DHT11 till AWS Iot-core för datalagring. ESP8266 samlar in temperaturdata från en sensor och skickar den till AWS Iot-core, som sedan lagrar data i DynamoDB i tables. Därifrån kan data nås och visualiseras med Quick seight, som referens Openwheather väderdata från närmaste station till sensorn lagras i Quick seight så jämförelser kan göras.

# AWS-Project
