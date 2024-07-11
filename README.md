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

Usage
Initialization
To initialize the AS5600 sensor, call the AS5600_Init function. This function sets up the I2C communication and configures the AS5600 sensor.


#include "AS5600.h"

AS5600_HandleTypeDef hAS5600;

HAL_StatusTypeDef status = AS5600_Init(&hAS5600, &hi2c1);
if (status != HAL_OK) {
    // Handle initialization error
}


Reading Angle
To read the angle from the AS5600 sensor, use the AS5600_GetAngle function. This function returns the angle in degrees.


float angle = 0;

HAL_StatusTypeDef status = AS5600_GetAngle(&hAS5600, &angle);

if (status == HAL_OK) {
   
    printf("Angle: %f degrees\n", angle);

} else 

{
   
    // Handle read error

}


Reading Status
To read the status of the AS5600 sensor, use the AS5600_GetStatus function. This function returns the status register value.


uint8_t status_reg = 0;
HAL_StatusTypeDef status = AS5600_GetStatus(&hAS5600, &status_reg);
if (status == HAL_OK) {
    printf("Status: 0x%02X\n", status_reg);
} else {
    // Handle read error
}

Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please create an issue or submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
