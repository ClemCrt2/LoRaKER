# Network analysis

Some wireshark files with all the network messages sent by each devices & softwares

## 1 - Message receive on the Kerlink Gateway

According to my trace, the message is receive by the Kerlink packet forwarder software and sent to the chirpstack-gateway-bridge on localhost:1700

## 2 - Message transmited to Network Server

The chirpstack-gateway-bridge software process the data and send a MQTT message to the Network Server with all the radio metadata and sensor data

## 3 -  Processing in the Network-Server

Some message are transmitted to Chirpstack-application-server

## 4 - Data receive by InfluxDb

This is the message sent by the application-server to the influxdb. For this I use the "influxdb integration" available in the application-server menu. We cleary see here that the app-server don't send all the radio rx information : Indeed, my sensor is well receive by my 2 gateways but only one RSSI and one SNR are stored in my influx database. 
A solution to get all radio rx information is maybe to use the "http integration" of the app-server menu
