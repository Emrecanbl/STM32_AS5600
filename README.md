AS5600 STM32 Driver

This repository contains a driver for the AS5600 magnetic rotary position sensor, implemented for STM32 microcontrollers. The driver facilitates communication with the AS5600 sensor over I2C and provides functions to read the angle and status information.

Initialization of the AS5600 sensor.
Reading the angle from the AS5600 sensor.
Checking the status of the AS5600 sensor.

Hardware Requirements
STM32 microcontroller (tested with STM32F4 series).

AS5600 magnetic rotary position sensor.

I2C communication interface.

Pull-up resistors for I2C lines (if not already present on your board).

Software Requirements

STM32 HAL library.
A suitable IDE such as STM32CubeIDE or Keil uVision.

Installation
Clone the repository:

git clone https://github.com/Emrecanbl/STM32_AS5600.git

Add the src and include directories to your STM32 project.

Ensure the I2C HAL library is included in your project.

Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please create an issue or submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
