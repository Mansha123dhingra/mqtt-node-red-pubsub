# MQTT Publish Subscribe System using Node-RED

**Name:** Mansha  
**Registration Number:** 22MIC0162

This project demonstrates an MQTT publish–subscribe system using Node-RED and Mosquitto.

## Publishers
1. **Temperature Publisher**  
   Topic: `home/livingroom/temperature`

2. **Humidity Publisher**  
   Topic: `home/livingroom/humidity`

## Subs[flow.json](flow.json)criber
Wildcard subscriber listening to:

`home/#`

## Technologies
- Node-RED
- MQTT
- Mosquitto
- Node.js

## Features
- Two publishers generating live sensor data
- Wildcard subscriber receiving all topics
- QoS level 1 message delivery
- Demonstrates MQTT publish–subscribe architecture

## Project Structure
