在上一篇推文，我们介绍了如何修改一个Card的Firmware，在这篇推文我们会介绍如何创建一个Card模块的硬件。
如果你想知道目前都有哪些可以使用的Card模块，可以点击链接获取列表。

In the last post, we introduced how to modify and create the firmware of a Card. In this post, we will introduce how to create the hardware of a Card module.
If you want to know which Card modules are currently available, you can click the [link](http://docs.longan-labs.cc/cards-system-summary/) to get the list.


# Required skills

* Familiar with basic electronic circuit
* Familiar with Eagle CAD software

# Download a template

We provide a template of Eagle files to help you to develop quickly. You can click the link to download the template.

Open the template and you can see that the basic part of the schematic has been completed. You only need to add the components you need in the blank part on the left.

// Insert picture


# How to design

In the schematic diagram, you can see a device called U1, which is the smallest system module of a single-chip microcomputer. The available interfaces are as follows:

// Insert picture
* I2C x 1
* UART x 1
* SPI x 1
* Analog input x 2
* Digital Input/Output x 2

If you choose an I2C interface, you only need to connect the device's I2C to DSDA/DSCL. Similarly, if you choose a UART/SPI or Analog Input device, you only need to connect to the corresponding interface.

In addition, you need to pay attention to the power supply. If the device you are using is 3.3V, you need to connect the VCC of U1 to 3V3 of U1, otherwise you can connect to 5V


# one example

In order to prove that it is not difficult to create a Card module, here we take BME280 as an example to design a BME280 Card.
BME280 is a temperature, humidity and pressure sensor.

// insert a picture

As you can see, we put in a BME280 chip, and made some simple connections, and we are done.
You can download Eagle File of BME280 Card for more information