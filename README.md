# MQTT Publish Subscribe System using Node-RED

**Name:** Mansha  
**Registration Number:** 22MIC0162  

## Project Description
This project demonstrates the **MQTT Publish–Subscribe communication model** using **Node-RED and the Mosquitto MQTT broker**. The system simulates a smart monitoring environment where multiple publishers send sensor data and a subscriber receives and displays the data.

The project includes two publishers that generate simulated sensor values and send them to the MQTT broker. A wildcard subscriber receives messages from multiple topics and displays them in the Node-RED debug panel.

## Publishers

### Temperature Publisher
Topic:
home/livingroom/temperature

This publisher simulates a temperature sensor. It generates random temperature values and publishes them to the MQTT broker.

### Humidity Publisher
Topic:
home/livingroom/humidity

This publisher simulates a humidity sensor and sends humidity values to the MQTT broker.

## Subscriber

The system includes a **wildcard subscriber** that listens to all topics under:

home/#

The wildcard `#` allows the subscriber to receive messages from all subtopics such as:

home/livingroom/temperature  
home/livingroom/humidity  

This demonstrates how MQTT can monitor multiple sensors using a single subscription.

## Technologies Used
- Node-RED  
- MQTT Protocol  
- Mosquitto MQTT Broker  
- Node.js  

## Features
- Two publishers generating live sensor data  
- Wildcard subscriber receiving multiple topics  
- MQTT message routing through Mosquitto broker  
- QoS Level 1 message delivery  
- Demonstrates MQTT publish–subscribe architecture  

## Project Structure

mqtt-node-red-pubsub  
│  
├── flow.json  
├── README.md  
└── screenshots  
    ├── flow1.png  
    ├── flow2.png  
    ├── flow3.png  
    └── debug.png  

## How the System Works

1. The **Temperature Publisher** sends temperature values to the topic:
   home/livingroom/temperature  

2. The **Humidity Publisher** sends humidity values to the topic:
   home/livingroom/humidity  

3. The **Mosquitto MQTT Broker** receives messages from publishers and forwards them to subscribers.

4. The **Wildcard Subscriber** listens to:
   home/#  

5. The subscriber receives messages and displays them in the **Node-RED debug panel**.

Example output:

home/livingroom/temperature : 27  
home/livingroom/humidity : 63  

## Running the Project

### 1. Start the MQTT Broker
mosquitto -v

### 2. Start Node-RED
node-red

### 3. Open Node-RED Editor
Open the browser and go to:

http://localhost:1880

### 4. Import the Flow
Import the `flow.json` file into Node-RED.

### 5. Deploy the Flow
Click **Deploy** to start the publishers and subscriber.

### 6. Open Dashboard (Optional)
http://localhost:1880/ui

## Output
The subscriber receives messages from both publishers and displays them in the debug panel, verifying that the MQTT publish–subscribe system works correctly.

## Author
Mansha  
Registration Number: 22MIC0162
