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
