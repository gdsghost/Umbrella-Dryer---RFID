# Umbrella Dryer RFID Smart Locker System

A smart locker-based umbrella drying system designed to securely store and dry wet umbrellas in public spaces. The system uses RFID/NFC-based user identification, automated drying components, environmental sensors, and servo-controlled locking mechanisms to improve customer convenience while reducing wet-floor safety hazards.

This project was developed as a collaborative hardware and embedded systems project by a 5-member team. My responsibilities included hardware integration, RFID reader implementation, embedded programming, sensor interfacing, and system-level testing.

## Project Overview

Wet umbrellas in public places such as shopping malls, offices, universities, hospitals, and transport hubs can create inconvenience and increase the risk of slippery floors. This project provides a practical solution by allowing users to place wet umbrellas inside a secure drying locker.

Each user receives an NFC/RFID tag that is linked to a locker. When the RFID tag is scanned, the system identifies the user, controls locker access, and activates the umbrella drying process. Humidity and temperature sensors monitor the drying environment, while heating coils and blower fans help remove moisture from the umbrella. PIR sensors detect user presence and trigger interactive instructions through LCD displays.

## Key Features

- RFID/NFC-based locker access
- Secure umbrella storage using servo-controlled locks
- Automated umbrella drying system
- Humidity and temperature-based drying control
- PIR-based user detection
- LCD-based user instructions and system feedback
- Buzzer alerts for interaction and status indication
- Support for different umbrella sizes
- Heating coil and blower fan integration
- PCB design for hardware implementation
- Embedded C programming for Atmega32 microcontrollers

## Demo Video

Project demo video:

[Watch the demo video on Google Drive](https://drive.google.com/file/d/1XvV7v88Koq5fNVAzytpqA9nxbofrzeYg/view?usp=sharing)

## Technologies and Components Used

### Microcontroller

- Atmega32 microcontroller

### Sensors and Modules

- MFRC522 RFID reader
- NFC/RFID tags
- PIR motion sensor
- Humidity sensor
- Temperature sensor

### Output and Control Components

- Servo motors
- LCD display
- Buzzers
- Heating coils
- Blower fans

### Communication and Interfaces

- SPI communication
- Digital input/output control
- Sensor-based embedded control logic

### Design and Development

- Embedded C
- AVR programming
- PCB design
- Hardware prototyping
- Sensor integration
- Microcontroller-based automation

## System Workflow

1. The user approaches the umbrella dryer locker.
2. The PIR sensor detects the user's presence.
3. The LCD displays instructions for the user.
4. The user scans an assigned RFID/NFC tag.
5. The system validates the tag and links it to the relevant locker.
6. The servo motor unlocks the locker.
7. The user places the wet umbrella inside the locker.
8. The locker is secured after the umbrella is placed.
9. Humidity and temperature sensors monitor the internal drying condition.
10. Heating coils and blower fans are activated to dry the umbrella.
11. The system provides status updates through the LCD and buzzer.
12. The user scans the RFID/NFC tag again to unlock and collect the umbrella.

## Hardware Architecture

The system is built around the Atmega32 microcontroller, which manages RFID authentication, LCD output, sensor readings, and actuator control.

```text
RFID/NFC Tag
     |
     v
MFRC522 RFID Reader
     |
     v
Atmega32 Microcontroller
     |
     |---- LCD Display
     |---- PIR Sensor
     |---- Humidity and Temperature Sensor
     |---- Servo Lock
     |---- Buzzer
     |---- Heating Coil
     |---- Blower Fan
```

## RFID Reader Functionality

The RFID reader is responsible for detecting NFC/RFID cards and reading the card serial number. The system uses the MFRC522 RFID module connected through SPI communication. Once a valid card is detected, the card serial data is processed and displayed through the LCD.

Main RFID-related functions include:

- Initializing the SPI interface
- Initializing the MFRC522 RFID reader
- Detecting RFID/NFC tags
- Reading card serial numbers
- Displaying card data on the LCD
- Supporting locker identification and access control logic

## Repository Structure

```text
Umbrella-Dryer---RFID/
│
└── Umbrella Dryer - RFID/
    │
    ├── main.c
    ├── lcd.c
    ├── lcd.h
    ├── spi.c
    ├── spi.h
    ├── spi_config.h
    ├── mfrc522.c
    ├── mfrc522.h
    ├── mfrc522_cmd.h
    ├── mfrc522_reg.h
    ├── myutils.h
    ├── utils.h
    ├── connection.pdf
    ├── pcb1.png
    └── pcb2.png
```

## PCB Design

The project also includes PCB design files/images used for the hardware implementation.

![PCB Design 1](Umbrella%20Dryer%20-%20RFID/pcb1.png)

![PCB Design 2](Umbrella%20Dryer%20-%20RFID/pcb2.png)

## Software Setup

### Requirements

- Atmel Studio or compatible AVR development environment
- AVR-GCC toolchain
- Atmega32 microcontroller
- MFRC522 RFID reader module
- LCD display module
- SPI connection setup
- Required sensors and actuator components

### Steps to Run

1. Clone the repository:

```bash
git clone https://github.com/gdsghost/Umbrella-Dryer---RFID.git
```

2. Open the project source files in an AVR-compatible IDE.

3. Connect the Atmega32 microcontroller with the required hardware components.

4. Compile the embedded C source code.

5. Upload the generated program to the Atmega32 microcontroller.

6. Scan an RFID/NFC tag to test card detection and LCD output.

## Example Use Case

This system can be used in:

- Shopping malls
- Office buildings
- Universities
- Hospitals
- Hotels
- Libraries
- Public transport stations
- Event venues

By drying and securely storing wet umbrellas, the system helps improve public safety, cleanliness, and user convenience.

## Team Contribution

This project was developed collaboratively by a 5-member team. My main contributions included:

- RFID reader integration
- Embedded C programming
- Microcontroller-based control logic
- LCD display integration
- SPI communication setup
- Sensor and actuator interfacing
- Hardware testing and debugging
- PCB-level implementation support

## Skills Demonstrated

- Embedded systems development
- Hardware and software integration
- RFID/NFC-based authentication
- Microcontroller programming
- Sensor-based automation
- Real-time control logic
- PCB design understanding
- Team-based engineering project development

## Future Improvements

- Add a central monitoring dashboard
- Store RFID access logs in external memory or a database
- Add IoT connectivity for remote locker monitoring
- Improve drying efficiency using adaptive temperature control
- Add mobile app-based locker reservation
- Add payment integration for commercial use
- Improve enclosure design for public deployment
- Add fault detection for sensors, fans, and heating elements

## License

This project is intended for educational and demonstration purposes. Add a suitable license if you plan to make the project open source.

## Author

Developed by Sudam and team as part of a smart embedded hardware project.
