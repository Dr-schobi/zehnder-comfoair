# Interface to Zehnder Comfoair 350

## Goal

The Zehnder Ventilation system is able to provide data about temperatures and fan speed.
I want to link this to my home automation / monitoring

Info found at [see-solutions](http://www.see-solutions.de/sonstiges/Protokollbeschreibung_ComfoAir.pdf)

## Components

- Inside the Unit, there is an RJ45 jack which provides an RS232 interface.
In addition, there is 12V from the control module available on this jack.
Pinout: Pin 1: 12V out, Pin 2: RS232 RX, Pin 3: RX232 TX, Pin 8: GND
I used a short unshielded cable to route the connection to the outside of the unit.

- A small DC-DC converter is used to create 5V from 12V. 

Data is connectecd to a [USR-TCP232-302 module](https://www.pusr.com/products/1-port-rs232-to-ethernet-converters-usr-tcp232-302.html). 
Data Format is 9600 8N1.
Inside the TCP232, the bridge was shorted. This way, 5V can be fed into the TCP232 module via the DB9 connector. No additional power supply is needed.

![IMG_20230901_155552](https://github.com/Dr-schobi/zehnder-comfoair/assets/78444256/3d2fcc21-8200-4ed5-97fb-7fa12d69a095)

![IMG_20230901_155604](https://github.com/Dr-schobi/zehnder-comfoair/assets/78444256/cce6e74f-ee2a-40fb-b6e2-473611d66d76)


## Software 

A module for the Edomi KNX automation is used to fetch the data. See [in the forum](https://knx-user-forum.de/forum/projektforen/edomi/992693-lbs-f%C3%BCr-zehnder-comfoair-ca350-550-stork-und-baugleiche)


