STM32 Modbus RTU Simulation with RS485

This project is a Proteus simulation designed to read Modbus data using an STM32F103 microcontroller and a 3.3V RS485 module.

Virtual Port Configuration (com0com)

<img width="446" height="398" alt="image" src="https://github.com/user-attachments/assets/051a690a-1dc7-4988-80a1-ad3420d0784a" />

Here you can see the com0com settings. I created a virtual port pair to establish a virtual Modbus connection between my Proteus application and the Modbus Slave simulation software.

Modbus Slave Settings

<img width="566" height="458" alt="image" src="https://github.com/user-attachments/assets/2f063887-3347-452c-9735-a711ba13df6a" />

<img width="448" height="536" alt="image" src="https://github.com/user-attachments/assets/aaa53f22-b0bf-4ec6-8d9b-d2cff0333467" />

These are the configurations for the Modbus Slave application. I set the baud rate to 9600 bps since the data payload is relatively small.
You can download the Modbus Slave simulation tool from this link: https://www.modbustools.com/download.html

Proteus Circuit Design

<img width="1004" height="628" alt="image" src="https://github.com/user-attachments/assets/d1cd956c-c5cd-4022-a5a7-50ea8fbaa066" />

This is the Proteus circuit diagram featuring the STM32F103C8. I integrated several key components for stability and debugging:
I added a crystal oscillator to generate a stable and precise clock signal for the STM32.
The virtual terminal communicates via UART to help monitor and verify the incoming data.
The COMPIM module is placed at the top to connect the hardware simulation to the virtual COM port.
Finally, a status LED is included to visually verify that the STM32 main loop is running properly.
