Smart Farming System using IoT Sensors
 -> Project Overview
        This project is a Smart Farming System that helps farmers monitor soil and environmental conditions in real-time using IoT sensors. It focuses on two main measurements:

   Soil Moisture – To determine if irrigation is needed.

   Temperature and Humidity – To ensure optimal conditions for crops.

   The system uses Arduino to collect sensor data and Java to process, monitor, and alert farmers. It also demonstrates Object-Oriented Programming (OOP) concepts such as classes, inheritance, encapsulation, and polymorphism.

-> Hardware Used
    Arduino Uno

   DHT22 Sensor (Temperature + Humidity)

   Soil Moisture Sensor

   USB cable for Arduino connection

   Wires

-> How It Works
Sensors collect data:

Soil moisture sensor measures water content in soil.

DHT22 measures temperature and humidity.

Arduino reads sensor values and sends them via Serial communication to the Java program.

Java program monitors the farm:

If soil moisture < 30% → alerts for irrigation.

If temperature > 30°C → alerts for high temperature.

If humidity < 50% → alerts for low humidity.

Alerts and readings are displayed on the console, allowing farmers to take immediate action.

-> Java Code Explanation
Sensor (Base Class): Stores sensorId and location. Provides a generic method readData() and displayInfo().

SoilMoistureSensor (Derived Class): Extends Sensor. Reads and checks soil moisture, alerts if soil is dry.

EnvironmentSensor (Derived Class): Extends Sensor. Reads temperature and humidity, alerts if conditions are not optimal.

Farm Class: Manages all sensors, iterates through them, and displays readings and alerts.

SmartFarmingSystem (Main Class): Creates sensors, adds them to the farm, and calls the monitoring method.

-> Arduino Code Explanation
Reads soil moisture from analog pin A0.

Reads temperature and humidity from DHT22 sensor on digital pin 2.

Converts readings to human-readable format (soil moisture in %, temperature in °C, humidity in %).

Sends data to Java program via Serial every 2 seconds.
-> Features
Real-time monitoring of soil and environment.

Alerts for irrigation and adverse conditions.

Object-Oriented Programming principles in Java.

Can work with real sensors (Arduino) or simulated data.

-> Benefits
Helps farmers save water and maintain healthy crops.

Reduces manual monitoring effort.

Demonstrates practical IoT + Java integration.

