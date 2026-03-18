![Python](https://img.shields.io/badge/Python-3.x-blue)
![ESP32](https://img.shields.io/badge/Hardware-ESP32-orange)
![Li-Fi](https://img.shields.io/badge/Communication-Li--Fi-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

# Image Transfer through Li-Fi (Hardware + Software System)

## Table of Contents

* [About the Project](#about-the-project)
* [System Overview](#system-overview)
* [Hardware Components](#hardware-components)
* [Software Components](#software-components)
* [Methodology](#methodology)
* [System Workflow](#system-workflow)
* [Key Features](#key-features)
* [Advantages of Li-Fi](#advantages-of-li-fi)
* [Limitations](#limitations)
* [Applications](#applications)
* [Future Scope](#future-scope)
* [Results](#results)
* [Repository Structure](#repository-structure)
* [Technologies Used](#technologies-used)
* [Conclusion](#conclusion)

---

## About the Project

This project presents a **Li-Fi-based image transfer system** that combines both **hardware and software components** to achieve secure and efficient data transmission using light.

Traditional wireless communication systems such as Wi-Fi use radio frequency (RF), which suffers from bandwidth limitations, interference, and security concerns. Li-Fi (Light Fidelity) provides an alternative by using visible light for communication, offering higher bandwidth and improved security, since light cannot pass through solid objects.

The goal of this project is to design and implement a **real-time image transmission system using Li-Fi**, integrating embedded hardware with intelligent software processing.

---

## System Overview

The system operates in two layers:

1. **Hardware Layer (Li-Fi Communication)**

   * Transmits and receives data using light signals

2. **Software Layer (Processing & Storage)**

   * Compresses, encodes, and reconstructs images
   * Stores data using cloud integration

---

## Hardware Components

* **ESP32 Microcontroller**

  * Controls data transmission and reception

* **Laser Diode (Transmitter)**

  * Converts digital signals into modulated light

* **Photodiode (Receiver)**

  * Detects light signals and converts them into electrical signals

* **Supporting Components**

  * Resistors, power supply, and connecting circuitry

---

## Software Components

* **Image Compression**

  * PCA-based autoencoder for reducing image size

* **Encoding**

  * Binary + Base64 encoding for transmission

* **Signal Processing**

  * Conversion of data into bit streams

* **Cloud Integration**

  * Dropbox API for storage and retrieval

---

## Methodology

### 1. Image Compression

* Images are compressed using a **PCA-based autoencoder**
* Reduces data size while maintaining quality

---

### 2. Image Encoding

* Image is converted into binary format
* Encoded using Base64
* Metadata (format, width, height) is added

---

### 3. Li-Fi Transmission (Hardware)

* ESP32 transmits binary data using a laser diode
* Light is modulated to represent bits

---

### 4. Signal Reception (Hardware)

* Photodiode receives light signals
* Converts light → electrical signals
* ESP32 decodes the binary data

---

### 5. Image Reconstruction

* Received data is decoded
* Image is reconstructed using metadata

---

### 6. Cloud Storage

* Image data is uploaded to Dropbox
* Enables secure storage and remote access

---

## System Workflow

1. Image is selected and preprocessed
2. Image is compressed using PCA-based autoencoder
3. Compressed data is encoded into binary/Base64 format
4. ESP32 transmits data using laser-based Li-Fi
5. Photodiode receives the optical signal
6. ESP32 decodes the received signal
7. Image is reconstructed at the receiver
8. Data is stored and accessed via Dropbox

---

## Key Features

* High-speed data transmission using light
* Secure communication (light cannot penetrate walls)
* Efficient image compression using AI techniques
* Integration of hardware (ESP32) and software (Python)
* Cloud-based storage using Dropbox API
* Low-cost and scalable prototype

---

## Advantages of Li-Fi

* **High Bandwidth**: Uses visible light spectrum
* **Enhanced Security**: Signal confined within physical space
* **No RF Interference**: Suitable for sensitive environments
* **Energy Efficient**: Can utilize existing lighting systems

---

## Limitations

* Requires line-of-sight communication
* Limited transmission range
* Affected by ambient light interference
* Requires precise alignment

---

## Applications

* Secure communication in hospitals
* Military and defense systems
* Underwater communication
* Smart homes and IoT systems
* High-speed indoor data transfer

---

## Future Scope

* Real-time video transmission using Li-Fi
* Integration with IoT ecosystems
* Advanced modulation techniques
* Error correction for improved reliability
* Full Li-Fi networking systems

---

## Results

The system successfully demonstrates:

* Real-time image transmission using Li-Fi
* Efficient image compression and reconstruction
* Reliable short-range communication
* Secure data transfer using light

---

## Repository Structure

```plaintext id="ultimate_struct"
project/
│
├── transmitter.ino        # ESP32 transmitter code
├── receiver.ino           # ESP32 receiver code
│
├── compress_image.py      # Image compression (PCA + autoencoder)
├── dropbox_handler.py     # Encoding + Dropbox upload
│
├── image_retrieval.mlx    # Image reconstruction
│
├── results/               # Output images
├── README.md
```

---

## Technologies Used

### Hardware

* ESP32
* Laser diode
* Photodiode

### Software

* Python
* TensorFlow / Keras
* NumPy
* Dropbox API

---

## Conclusion

This project demonstrates the successful integration of **hardware (Li-Fi communication)** and **software (image processing and cloud storage)** to build a complete image transfer system.

The system highlights the potential of Li-Fi as a secure and efficient alternative to traditional wireless communication technologies, especially for short-range applications.

---
