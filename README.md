# LSM303AGR Sensor Library
Welcome to the LSM303AGR Sensor Library Repository! This repository hosts a modified version of the [stm32-lsm303agr](https://github.com/STMicroelectronics/stm32-lsm303agr) library originally developed by STMicroelectronics.
# Modifications:
The modifications in this repository aim to enhance the functionality, performance, and usability of the original STM32 LSM303AGR library. These enhancements may include:
1. Flexible Mode Selection: Introducing flexible mode selection functionality, allowing users to easily switch between different operating modes of the LSM303AGR sensor based on application requirements.
2. Shift Bit for Raw Data Calculation: Addition of shift bit to raw data calculation to eliminate unused bit, optimizing the data processing pipeline and improving accuracy.
3. Gravity Calculation: Incorporation of gravity calculation for the three axes with reference to Earth's gravity, the moon's gravity, and the sun's gravity. This feature provides users with valuable insights into the gravitational forces acting on the sensor, facilitating advanced motion analysis and orientation tracking applications.
# Usage:
Developers can utilize this modified library to interface with the LSM303AGR sensor seamlessly on STM32 microcontroller platforms. By leveraging the enhanced features and optimizations, users can accelerate development cycles and improve the performance of their applications.
# Contributions:
Contributions to this repository, including bug fixes, feature additions, and documentation improvements, are welcome. Developers are encouraged to collaborate and further refine the library to meet the evolving needs of the community.
# License:
The modified STM32 LSM303AGR library is provided under an open-source license, ensuring accessibility and freedom for developers to use, modify, and distribute the code according to their requirements.
# Note:
It's advisable to refer to the original [STM32 LSM303AGR datasheet](https://www.st.com/resource/en/datasheet/lsm303agr.pdf) and documentation for detailed specifications and usage guidelines of the sensor.
# Example:
```C
		/* Init Accelerometer MEMS */
		  if(BSP_ACCELERO_Init() != HAL_OK)
		  {
		    /* Initialization Error */
			  printf("Initialization Accelerometer Error \n");
		    Error_Handler();
		  }

		  Buffer[0] = 0;
		  Buffer[1] = 0;
		  Buffer[2] = 0;

		  BSP_ACCELERO_GetXYZ(Buffer);

		  X = Buffer[0];
		  Y = Buffer[1];
		  Z = Buffer[2];

		  printf("X: %.2f - Y: %.2f - Z: %.2f \n", X,Y,Z);

		  fflush(stdout);

		  HAL_Delay(10);
```
When the sensor is placed flat on the surface, the collected data will be similar to the following data.
```
X: -0.75 - Y: -0.04 - Z: 9.69 
X: -0.98 - Y: 0.04 - Z: 9.92 
X: -0.98 - Y: -0.04 - Z: 9.92 
X: -0.78 - Y: -0.04 - Z: 9.92 
X: -0.78 - Y: 0.04 - Z: 9.81 
X: -0.78 - Y: -0.04 - Z: 9.92 
X: -0.82 - Y: 0.16 - Z: 9.92 
X: -0.82 - Y: -0.08 - Z: 9.89 
X: -0.75 - Y: -0.08 - Z: 9.89 
X: -0.75 - Y: -0.08 - Z: 9.92 
X: -0.98 - Y: -0.04 - Z: 9.69 
X: -0.75 - Y: -0.08 - Z: 9.81 
X: -0.75 - Y: -0.04 - Z: 9.85 
X: -0.75 - Y: -0.04 - Z: 9.85 
```
Because the sensor is placed flat on the surface, it will measure an acceleration due to Earth's gravity on the Z-axis of approximately 9.81 m/s^2. Looking at the collected data, it can be seen that the data appears to be unstable due to various influencing factors. We need to address this to ensure that the sensor will function and provide accurate results.
