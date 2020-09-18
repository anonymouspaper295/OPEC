# OPEC
## Nine Tested Applications Details
PinLock and QRcode are evaluated on the STM32F4-Discovery board, whereas the other seven applications are evaluated on the STM32469I-EVAL board. It is because these seven applications are developed on two different boards and use two different hardware abstraction layers.

### PinLock
PinLock is an unofficial smart lock application running on the STM32F4-Discovery board. When it first starts up, the application prompts the user to enter the correct pin code. Next it receives the pin code from the serial port. The application then uses the functions of mbedtls library to compute the hash of the received pin code.
The result is compared with a stored value. If the pin is correct, an LED will be turned on to indicate the unlock state. Otherwise, the application will continue to ask a new user input.

source code: https://github.com/embedded-sec/ACES/tree/master/test_apps/pinlock

### QRcode
QRcode generates a QR code based on the content of a text file stored in the SD card. The generated QR code is then displayed on a Nokia5100 screen. We can get the content of the text file by parsing the QR code.

source code: https://github.com/kazimierczak-robert/STMQRCode

### Camera
This application uses the camera on the STM32469I-EVAL board to take a photo after the user press the button. The photo is stored as a BMP file at a USB disk.

source code: https://github.com/STMicroelectronics/STM32CubeF4/tree/master/Projects/STM32469I_EVAL/Applications/Camera/Camera_To_USBDisk

### Animation
Animation demonstrates a moving butterfly against the background of the ST logo on the screen.

source code: https://github.com/STMicroelectronics/STM32CubeF4/tree/master/Projects/STM32469I_EVAL/Applications/Display/LCD_AnimatedPictureFromSDCard

### Filename
FileName presents the names of the files stored in the SD card with fade-in and fade-out effects.

developed based on: https://github.com/STMicroelectronics/STM32CubeF4/tree/master/Projects/STM32469I_EVAL/Applications/Display/LCD_PicturesFromSDCard

### Fatfs-uSD
Fatfs-uSD implements a FAT file system on a micro SD card. It writes some fixed contents to a newly created file in the file system.
After that, it reads the file and checks whether the content is correct.

source code: https://github.com/STMicroelectronics/STM32CubeF4/tree/master/Projects/STM32469I_EVAL/Applications/FatFs/FatFs_USBDisk

### RAMDisk
RAMDisk implements a FAT file system on a RAM disk.

source code: https://github.com/STMicroelectronics/STM32CubeF4/tree/master/Projects/STM32469I_EVAL/Applications/FatFs/FatFs_RAMDisk

### TCP_Echo
This application runs a TCP echo server on the board. The server is developed based on lwIP, which is a lightweight implementation of TCP/IP protocol.

source code: https://github.com/STMicroelectronics/STM32CubeF4/tree/master/Projects/STM32469I_EVAL/Applications/LwIP/LwIP_TCP_Echo_Server

### StarWar
StarWar is a space war game running on the STM32469I-EVAL board.

developed based on: https://github.com/ChengChen2/STM32-MicroController-StarWarGame/blob/master/main.c
