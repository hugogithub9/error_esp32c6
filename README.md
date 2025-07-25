This project demonstrates a critical issue encountered when using the ESP32-C6 board with the GY-BNO055 9-axis sensor (accelerometer, magnetometer, gyroscope) via I2C.

------  

Context
The code used in this project is based on working examples for reading BNO055 sensor data, such as acceleration, magnetometer, and gyroscope values.

I noticed that:

Reading and printing only one type of sensor data (e.g. acceleration) works perfectly.

As soon as I try to print two values (e.g. acceleration and magnetometer), the board crashes and I get the following bootloader error:

E (77) esp_image: Segment 0 load address 0x42058020, doesn't match data 0x00010020
E (84) boot: Factory app partition is not bootable
E (88) boot: No bootable app partitions in the partition table

I opened an issue on GitHub to document and investigate this problem. So far, the cause remains unknown, and the issue is not resolved.

https://github.com/issues/created?issue=esp-rs%7Cesp-idf-hal%7C536
