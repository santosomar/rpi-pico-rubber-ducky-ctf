# USB Rubber Ducky with Raspberry Pi Pico

The purpose of this GitHub repository is to provide the resources that I demonstrated during the IoT Hacking exercises I created for Cisco Live US. The demo is inspited by [pico-ducky](https://github.com/dbisu/pico-ducky) which allows you to create a USB Rubber Ducky with a Raspberry Pi Pico. This project aims to demonstrate the process of building a USB Rubber Ducky device using the Raspberry Pi Pico, providing an opportunity to explore the inner workings of these devices while highlighting potential risks and promoting responsible use of technology.

## Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction
The USB Rubber Ducky is a powerful tool that emulates a keyboard to execute commands or automate tasks on a target computer. By leveraging the capabilities of the Raspberry Pi Pico, we can create a cost-effective alternative to the traditional USB Rubber Ducky device.

In this project, we will guide you through the process of building your own USB Rubber Ducky using a Raspberry Pi Pico, providing step-by-step instructions, code samples, and explanations of key concepts along the way.

## Getting Started
To get started with this project, you will need the following:
- Raspberry Pi Pico board
- USB cable
- Computer with a USB port
- [Python](https://www.python.org/) installed on your computer
- Text editor or integrated development environment (IDE) of your choice

## Detailed Instructions

1. Connect the Raspberry Pi Pico to your computer using a USB micro cable. Connect the device to a USB port while holding the boot button. It will appear as a removable media device named "RPI-RP2". 

**NOTE:** The Pico W will not appear as a USB drive by default.

2. Obtain a local copy of the files by cloning this repository using the command: 
```
git clone https://github.com/santosomar/rpi-pico-rubber-ducky-ctf
```

Change to the directory/folder of your local clone of this repository:

```
rpi-pico-rubber-ducky-ctf
```

3. Download the CircuitPython version 8.x for the Raspberry Pi Pico from the following sources:
   - Raspberry Pi Pico: [CircuitPython Download](https://circuitpython.org/board/raspberry_pi_pico/) (Updated to 8.x)
   - Raspberry Pi Pico W: [CircuitPython Download](https://circuitpython.org/board/raspberry_pi_pico_w/) (Updated to 8.x)

4. Transfer the downloaded `.uf2` file to the main directory of the Pico (identified as "RPI-RP2"). The device will reboot, and after a brief moment, it will reconnect as "CIRCUITPY".

5. Copy the following files and directories to the Raspberry Pi Pico:
```
boot.py
code.py
duckyinpython.py
lib
settings.toml
webapp.py
wsgiserver.py
```
**NOTE**: The `webapp.py` and `wsgiserver.py` files are optional in case you want to run a web server and you have a Raspberry Pi Pico W (wireless).

## Creating the payload
The USB Rubber Ducky is a versatile tool that utilizes DuckyScript 3.0, a scripting language designed specifically for automating tasks and executing payloads on target systems. DuckyScript 3.0 provides a simple yet powerful syntax for creating scripts that can simulate keyboard input, interact with the operating system, and perform various actions. By leveraging the USB Rubber Ducky, users can easily automate repetitive tasks, perform security assessments, and execute pre-defined sequences of commands on a wide range of systems. With DuckyScript 3.0, the USB Rubber Ducky offers a flexible and efficient solution for automating tasks and carrying out advanced penetration testing activities.

- You can obtain a script from [Hak5](https://github.com/hak5/usbrubberducky-payloads) or create your own script using Ducky Script syntax described [here](https://docs.hak5.org/hak5-usb-rubber-ducky/ducky-script-basics/hello-world). 
- Save the script as `payload.dd` in the main directory of the Pico. 
- Please note that RPi Pico only supports DuckyScript 1.0, not 3.0.

**Warning!** If your device is not in [setup mode](#setup-mode), it will reboot, and the script will run automatically half a second after reboot.


## Contributing
Contributions are welcome! If you have any improvements, suggestions, or bug fixes, please feel free to submit a pull request. For major changes, please open an issue first to discuss the proposed changes.

## License
This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the code for personal and commercial purposes.

