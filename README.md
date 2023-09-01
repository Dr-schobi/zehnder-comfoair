# Interface to Zehnder Comfoair 350

## Goal

The Zehnder Ventilation system is able to provide data about temperatures and fan speed.
I want to link this to my home automation / monitoring

Info found at [see-solutions](http://www.see-solutions.de/sonstiges/Protokollbeschreibung_ComfoAir.pdf)

## Components

Inside the Unit, there is an RJ45 jack which provides an RS232 interface.
In addition, there is 12V from the control module available on this jack.

Pin 1: 12V out, Pin 2: RS232 RX, Pin 3: RX232 TX, Pin 8: GND

Data Format: 9600 8N1

A small DC-DC converter is used to create 5V. This is fed into a [USR-TCP232-302 module](https://www.pusr.com/products/1-port-rs232-to-ethernet-converters-usr-tcp232-302.html). 
This connects to Ethernet 

