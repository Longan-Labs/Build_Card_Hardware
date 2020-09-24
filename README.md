In the last post, we introduced how to modify and create the firmware of a Card. In this post, we will introduce how to create the hardware of a Card module.
If you want to know which Card modules are currently available, you can click the [link](http://docs.longan-labs.cc/cards-system-summary/) to get the list.


# Required skills

* Familiar with basic electronic circuit
* Familiar with Eagle CAD software

# Download a template

We provide a template of Eagle files to help you to develop quickly. You can click the [link](https://github.com/Longan-Labs/Build_Card_Hardware/archive/master.zip) to download the template.

Open the template and you'll find that the basic part of the schematic has been completed. You only need to add the components you need in the blank part on the left.

![](https://raw.githubusercontent.com/Longan-Labs/Build_Card_Hardware/master/images/shc_card.jpg)


# How to design

In the schematic diagram, you can see a device called U1, which is the smallest system module of a single-chip microcomputer. The available interfaces are as follows:

* I2C x 1
* UART x 1
* SPI x 1
* Analog input x 2
* Digital Input/Output x 2

![](https://raw.githubusercontent.com/Longan-Labs/Build_Card_Hardware/master/images/card_core.jpg)

If you use an I2C interface, please connect the I2C of the device to DSDA/DSCL. Similarly, for others interfaces, such as UART/SPI or Analog Input device, do the same things.

In addition, you should pay attention to the power supply. If the device you are using is 3.3V, you need to connect the VCC of U1 to 3V3 of U1, otherwise you can connect it to 5V


# one example

In order to prove that it is not difficult to create a Card module, here we take BME280 as an example to design a BME280 Card.
BME280 is a temperature, humidity and pressure sensor.

![](https://raw.githubusercontent.com/Longan-Labs/Build_Card_Hardware/master/images/bme280card.jpg)

As you can see, we put in a BME280 chip, and made some simple connections, and we are done.
You can download Eagle File of BME280 Card for more information.