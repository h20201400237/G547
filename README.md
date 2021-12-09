# DRIVER CODE FOR PUSH SENSOR WITH LED

## SUMMARY
- This is just a basic device driver describing about LED toggling with push sensor and LED status retreival in userspace from kernel with IOCTL commands.
- 2 LEDs have been connected to the OUTPUT pin (GPIO 26 & GPIO 25 ) and touch sensor has been connected to INPUT pin (GPIO 6).
- Whenever touch sensor is detected, 
  - White LED status will be toggled in kernel space,and status is also displayed in User space. 
  - Red LED status is configurable from user space.

## HARDWARE DESIGN
### ***Schematic Diagram***




![Schematic diagram](https://github.com/h20201400237/G547/blob/Project/circuit_schematic.PNG)







### ***Actual Schematic***




![Actual Schematic](https://github.com/h20201400237/G547/blob/Project/Actual%20schematic.jpeg)



## KERNEL SPACE DRIVER CODE & BUILD PROCESS
### Code Link: 
[https://github.com/h20201400237/G547/blob/Project/main.c](url)
### Build Process:
- Build the driver by using Makefile (**sudo make**).
- Load the driver using **sudo insmod driver.ko** .
- Check whether module is inserted in kernel space with **lsmod** .
- Unload the driver using **sudo rmmod driver**, after checking LEDs.

## USER SPACE APPLICATION CODE & BUILD PROCESS
### Code Link:
[https://github.com/h20201400237/G547/blob/Project/user.c](url)

### Build Process:
- Compile user application code with **gcc -o output user.c**.
- Run the application - **sudo ./output**.


## RESULT 
- Initially we have given the touch input which is detected from kernel to userspace then the white led is on and red led status is given as 0 in userspace.
- Later we have given the touch input then the white led is off and red led status is given as 1 in userspace which can be seen below.

![Results](https://github.com/h20201400237/G547/blob/Project/sc.jpeg)
![Results](https://github.com/h20201400237/G547/blob/Project/white.jpeg)
![Results](https://github.com/h20201400237/G547/blob/Project/red.jpeg)










