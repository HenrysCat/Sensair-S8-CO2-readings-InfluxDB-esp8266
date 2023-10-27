# Sensair-S8-CO2-readings-InfluxDB-esp8266

How to send Sensair S8 CO2 sensor readings to InfluxDB with an esp8266 devboard

install this library in ArduinoIDE first

https://github.com/jcomas/S8_UART

Now write the code to your esp device with Arduino IDE, this will send readings every 60 seconds, you can change this by editing the line 'Serial.println("Wait 60s"); delay(60000);;' to whatever you want.

The Sensair S8 is factory set to default to 400ppm CO2, as the current world wide level is around 420ppm I have added 20 in this line 'sensor_db.addField("co2_value", sensor_s8.co2 + 20);' you can of course change this if you wish.

Below is a screenshot from my InfluxDB dashboard.

![alt text](https://github.com/HenrysCat/Sensair-S8-CO2-readings-InfluxDB-esp8266/blob/main/CO2.png?raw=true)
