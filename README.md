# differential-barometric

Code for the paper **“Differential Barometric Altimetry for Submeter Vertical Localization and Floor Recognition Indoors.”**

This repository contains utilities and integration code that support the paper. It links two main components:

* **ESP32\_Barometer** — firmware for ESP32 to read the HP206 barometer and stream measurements.
  [https://github.com/witsir/ESP32\_Barometer](https://github.com/witsir/ESP32_Barometer)
* **ros\_barometer** — ROS 2 node that ingests pressure readings over serial or HTTP and republishes them in ROS.
  [https://github.com/witsir/ros\_barometer](https://github.com/witsir/ros_barometer)

## Features

* Read HP206 barometer on ESP32 and stream pressure samples.
* Convert serial/HTTP barometer streams to ROS 2 topics.
* Designed for submeter vertical localization and indoor floor recognition pipelines.

## Prerequisites

* HP206 barometric sensor and ESP32 development board.
* ROS 2 (recommended: Humble or later).
* Python 3.8+ for ROS node utilities.
* PlatformIO to build ESP32 firmware.
* See component READMEs for detailed dependency lists.

## Quick start

1. Flash the ESP32 firmware. See `ESP32_Barometer` README for build and flashing instructions.
2. Connect ESP32 to host machine.
3. Start the ROS 2 node. Use the provided launch file in `ros_barometer`:
4. Verify ROS topics and messages with `ros2 topic list` and `ros2 topic echo <topic>`.

## Data and message formats

Pressure and related telemetry are published as ROS messages. See `ros_barometer` README for exact topic names and message types.

## Citation
TODO
