# DRIVER CODE FOR PUSH SENSOR WITH LED 
This is just a basic device driver describing about LED toggling with push sensor and LED status retreival in userspace from kernel with IOCTL commands.
2 LEDs have been connected to the OUTPUT pin (GPIO 26 & GPIO 25 ) and the Touch sensor has been connected to the INPUT pin (GPIO 6).
Whenever touch sensor is detected, 
- White LED status will be toggled in kernel space,and status is also displayed in User space. 
- Red LED status is configurable from user space.



## Steps to be followed in build process:

- Build the driver by using Makefile (**sudo make**).
- Load the driver using **sudo insmod driver.ko** .
- Check whether module is inserted in kernel space with **lsmod** .
- Compile user application code with **gcc -o output user.c**.
- Run the application - **sudo ./output**.
- Unload the driver using **sudo rmmod driver**, after checking LEDs.

### Output: 
***Toggling LED :***




![Toggling LED output](https://embetronicx.com/wp-content/uploads/2020/09/GPIO-Linux-Device-Driver-using-Raspberry-Pi.gif).






