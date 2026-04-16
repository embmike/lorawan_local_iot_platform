# LoRaWAN Local IoT Platform

## Overview

This project implements a fully local LoRaWAN-based measurement system:

Sensor → LoRaWAN → Gateway → Network Server → MQTT → GUI

## Goals

- Local operation (no cloud)
- Modular architecture
- Clear data flow
- Reusable reference system

## Structure

- embedded/  -> STM32 firmware
- backend/   -> Network server & MQTT processing
- gui/       -> Qt visualization
- docs/      -> Architecture & process docs
- tools/     -> Scripts & utilities

## Next Steps

- Define first work package
- Define BDD scenarios
- Setup MQTT client
