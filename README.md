# Autonomous Parking System

Autonomous Parking System is an integrated system of a self-driving robot and smart parking garage to save fuel and time for parking. Eelf driving robot is based on a
Parallax Basic Stamp 2 microcontroller and a smart parking garage is based on an Arduino Uno R3 microcontroller.

## **Smart Parking Garage**

The smart parking arena is equipped with Arduino Uno R3 which computes the empty parking spots by reading data from ultrasonic ping sensors attached at the parking spots. The goal is to determine the closest open parking spot from the total of empty parking spots in the arena. Once, the closest location to the car is computed then the data is sent to the smart car. 

![image](https://user-images.githubusercontent.com/73630123/228930580-977cc34c-4346-4b45-a58e-c3c836ba5775.png)

## **Self-Driving Robot**

The smart bot has been built on the chassis available in the Boe-Bot kit from PARALLAX. The Basic Stamp 2 microcontroller is responsible for taking signals from Arduino Uno regarding availability of parking spots in the arena. This data is collected from 4 ultrasonic sensors that have been installed at every parking spot in the arena and transmitted to the Smart Bot through wireless communication. Once this data is collected, the BS2 then drives the continuous rotation servo motors to allow the bot to navigate to the free parking spot. 2 IR sensors have been mounted at the front of the bot to guide it’s navigation along the path.

![image](https://user-images.githubusercontent.com/73630123/228931140-fc2aa0dd-2fa8-4c2b-8b09-f19b247c2089.png)

## **Communication between two Systems**

The data is transmitted and received using two NRF24L01 Wi-Fi modules on the parking arena and the smart car. The NRF24L01 Wi-Fi module works on a 2.4 GHz ISM frequency band. That is why it is used in this project which then helps high speed data transmission to the receiver end. The parking arena is capable of sending data up to 2 Megabytes and the data transmissions happens in series which means the data of ultrasonic sensor is transmitted to the receiver at very high speed. 

The parking arena can communicate with 125 smart cars at one particular moment which makes the system very robust. The receiver data and can compute the path according to the data received from the parking arena about the empty parking space in the area. The receiver is also equipped with NRF24L1 Wi-Fi module which enables the car to receive the data at a high-speed rate to register any new change required to adapt to make necessary change in the path.
