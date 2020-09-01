# OPEC
## Nine Tested Applications Details
PinLock and QRcode are evaluated on the STM32F4-Discovery board, whereas the other seven applications are evaluated on the STM32469I-EVAL board. It is because these seven applications are developed on two different boards and use two different hardware abstraction layers.

### PinLock
PinLock is an unofficial smart lock application running on the STM32F4-Discovery board. When it first starts up, the application prompts the user to enter the correct pin code. Next it receives the pin code from the serial port. The application then uses the functions of mbedtls library to compute the hash of the received pin code.
The result is compared with a stored value. If the pin is correct, an LED will be turned on to indicate the unlock state. Otherwise, the application will continue to ask a new user input.

### QRcode
QRcode generates a QR code based on the content of a text file stored in the SD card. The generated QR code is then displayed on a Nokia5100 screen. We can get the content of the text file by parsing the QR code.

### Camera
This application uses the camera on the STM32469I-EVAL board to take a photo after the user press the button. The photo is stored as a BMP file at a USB disk.

### Animation
Animation demonstrates a moving butterfly against the background of the ST logo on the screen.

### Filename
FileName presents the names of the files stored in the SD card with fade-in and fade-out effects.

### Fatfs-uSD
Fatfs-uSD implements a FAT file system on a micro SD card. It writes some fixed contents to a newly created file in the file system.
After that, it reads the file and checks whether the content is correct.

### RAMDisk
RAMDisk implements a FAT file system on a RAM disk.

### TCP_Echo
This application runs a TCP echo server on the board. The server is developed based on lwIP, which is a lightweight implementation of TCP/IP protocol.

### StarWar
StarWar is a space war game running on the STM32469I-EVAL board.
