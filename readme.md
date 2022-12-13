# **ESP8266-DHT11-Project**

### Arkitektur 

<img src="/img/espbild.jpg">

# Beskrivning av projekt

* 1. Temp och Humidity, använder mig utav en DHT11 

* 2. ESP8266 D1mini fick löda ihop lita pina för att få den att funka 

* 3. Koden är skriven på C arduino ide


* 4. uppkopplingen är gjord med MQTT, Där du skapar en publisher vilket är Temp i mitt fall, och sen subscriber och iot connectionen, sen övervaka man MQTT-meddelande som skickas in till mitt AWS-konto 

* 5. AWS iot-core 

* 6. All min data som kommer från sensor lagrar jag i en table på DynamoDB, där tar jag även in API från openweather 

* 7. Lambda gör jag en api anrop från openwheather, med hjälp av en API Gateway

* 8. Visualisera och göra en korrelation med inomhus tempratuen och utomhus 



## **Målet med projektet**


Målet med detta projekt är att demonstrera hur man ansluter en ESP8266 mikrokontroller med DHT11 till AWS Iot-core för datalagring. ESP8266 samlar in temperaturdata från en sensor och skickar den till AWS Iot-core, som sedan lagrar data i DynamoDB i tables. Därifrån kan data nås och visualiseras med Quick seight, som referens Openwheather väderdata från närmaste station till sensorn lagras i Quick seight så jämförelser kan göras.

# AWS-Project
