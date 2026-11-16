# What is CAN BUS
* CAN Stands for Controller Area Network.
* CAN is a communication system in which multiple devices are connected to each other via a shared common bus.
* In Physical Terms all devices are connected to a 2 wired bus. the two wires are CAN High and CAN Low. they are often color coded: CAN High as yellow and CAN Low as green.
* In CAN, if a device(aka node) transmits a message, it is received by all the other devices(aka nodes) and each device(aka node) decides for itself whether to accept the message or not.

# ECU
* ECU Stands for electronic control unit.
* Most of the ECUs today have following components

## Microcontroller
* Performs data processing and decides the contents of message i.e CAN Frame to be transmitted.
* Also determies the moment or frequency of the message to be transmitted.

## CAN Controller
* Implements CAN Protocol on behalf of microcontroller.

## CAN Transceiver
* Converts the CAN Frame to differential signal and vice versa.
* Also provides electrical protection.