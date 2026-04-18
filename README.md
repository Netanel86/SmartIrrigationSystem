# Smart Irrigation Control System (Android + IoT + MQTT)

## Overview

This project is a distributed smart irrigation system designed for remote monitoring and control of home irrigation devices.

The system combines:

* Raspberry Pi as the central controller and backend server
* Arduino-based wireless endpoints for sensors and valves
* MQTT communication protocol for real-time messaging
* Android application for monitoring and manual control
* Local and remote database integration for state persistence

The goal was to create a scalable and reliable irrigation system capable of managing multiple irrigation zones and environmental sensors in real time.

---

## My Contribution

I designed and developed both the backend system and the Android control application.

My primary implementation focused on:

### Backend (Raspberry Pi + Communication Layer)

* MQTT communication between endpoints and controller
* Device state synchronization and command routing
* Sensor and valve management logic
* Local and remote database integration
* Real-time control workflows and reliability handling

### Android Application

* MVVM architecture and ViewModel design
* Sensor and valve state management UI
* Data binding and observable state updates
* Remote monitoring and manual control flows
* Scalable UI architecture for multiple endpoints

The core engineering challenge was maintaining reliable synchronization between physical devices, backend services, and the Android application.

---

## System Architecture

Arduino Sensors / Valves
↓
MQTT Communication Layer
↓
Raspberry Pi Backend Controller
↓
Local + Remote Database
↓
Android Application (Monitoring + Control)

This architecture allows distributed endpoint management while keeping communication lightweight, scalable, and responsive.

---

## Technical Challenges

### Reliable Real-Time Device Communication

The system needed stable communication between wireless endpoints and the central controller while handling live sensor updates and valve control commands.

### State Synchronization

Sensor readings, valve states, and manual overrides had to remain consistent across:

* physical devices
* backend controller
* Android application
* database storage

### Scalable System Design

The architecture needed to support multiple irrigation zones and endpoints without tightly coupling UI logic to hardware behavior.

---

## Solution

I used MQTT for lightweight asynchronous communication and implemented MVVM architecture on Android to separate UI, business logic, and state management.

Observable ViewModels and BindingAdapters were used to keep the UI synchronized with real-time backend updates.

This improved maintainability, reliability, and made the system flexible enough to scale across multiple sensors and irrigation zones.

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
* Distributed Systems Design

---

## Features

* Remote irrigation control from Android app
* Real-time environmental sensor monitoring
* Valve status management
* Manual and automatic irrigation workflows
* Distributed endpoint communication
* Local and remote data persistence
* Multi-zone irrigation support

---

## What I Learned

* Distributed systems architecture
* Real-time communication using MQTT
* Android MVVM design patterns
* State synchronization across hardware and software
* Building reliable IoT control systems
* Full-stack thinking across mobile + backend + hardware
