# Smart Irrigation Control System (Android + IoT + MQTT)

## Overview

This project is a distributed smart irrigation system designed for remote monitoring and control of home irrigation devices.

The system combines:

* Raspberry Pi as the central controller
* Arduino-based wireless endpoints
* MQTT communication protocol
* Android application for remote control
* Local and remote database integration

The goal was to create a scalable and reliable irrigation system capable of managing valves and environmental sensors in real time.

---

## My Contribution

I designed and developed the software architecture for both the Android control application and the communication flow between devices.

My primary implementation focused on:

* Android application architecture (MVVM)
* Sensor and valve state management
* MQTT communication logic
* ViewModel and data binding systems
* Remote monitoring and manual control workflows
* System reliability and real-time synchronization

---

## System Architecture

Arduino Sensors/Valves
↓
MQTT Communication Layer
↓
Raspberry Pi Controller
↓
Local + Remote Database
↓
Android Application (Monitoring + Control)

This architecture allows distributed endpoint management while keeping communication lightweight and responsive.

---

## Technical Challenges

### Reliable Real-Time Device Communication

The system needed to maintain stable communication between wireless endpoints and the central controller while handling live state updates.

### State Synchronization

Sensor readings, valve states, and manual overrides needed to remain consistent across:

* physical devices
* local controller
* Android application
* remote database

### Scalable Architecture

The application needed to support multiple endpoints without tightly coupling UI logic to hardware behavior.

---

## Solution

I used MQTT for lightweight asynchronous communication and implemented MVVM architecture in Android to separate UI, state management, and business logic.

Observable ViewModels and BindingAdapters were used to keep the UI synchronized with real-time system state changes.

This improved maintainability and allowed flexible scaling of sensors and irrigation zones.

---

## Technologies

* Java
* Android SDK
* MVVM
* MQTT
* Raspberry Pi
* Arduino
* SQLite
* Data Binding
* Observable Patterns

---

## Features

* Remote irrigation control from Android app
* Real-time sensor monitoring
* Valve status management
* Manual and automatic irrigation workflows
* Distributed endpoint communication
* Local and remote data persistence

---

## What I Learned

* Distributed systems design
* Real-time communication with MQTT
* Android MVVM architecture
* State synchronization across hardware and software
* Building reliable IoT workflows
