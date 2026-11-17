# CAN Frame
According to data link layer the message in CAN protocol is transmitted via CAN Frames.

A typical CAN Frame has 8 different fields and following is the description of all the data fields of CAN 2.0 A:
* SOF - Start of Frame (1 bit)
It is dominent 0 by the nodes that want to transmit the data.

* ID - Identifier (11 bits)
  * This is the number that determines that type of the message that is being transmitted as well as the priority of the message.
  * The lower the value the higher the priority.

* RTR - Remote Transmission Request (1 bit)
  * Remote Transmission Request determines whether the transitting node is transmitting the data or merely requesting the data.
  * Dominent 0 means that node is transmitting the data and has Payload field
  * Recessive 1 means that node is merely requesting the data and does not have a payload field
  * A frame with Recessive 1 looses the arbitration to the frame with dominent 0 with the same identifier

* Control - Control Filed (6 bits) has following subfields:
  * IDE - Idenfier extension (1 bit)
    * dominent 0 in case of 11 Identifier bits of CAN 2.0 A
    * recessive 1 in case of 29 Identifier bits of CAN 2.0 B.
    * In case of CAN 2.0 B the first 11 identifer bit are immediately followed by the Identifier entension bit. and the rest 19 bits follow IDE.
  * R - Reserved bit (1 bit): This bit is reserved for future use.
  * DLB - Data length bit (4 bits): These bits determine the no of bytes in payload from 0 byte to 8 bytes.

* Payload: The acutaly message we intent to transmit.

* CRC - Cyclic Redundancy Check (16 bits): to ensure the data integrity.

* ACK - Acknowledgement (2 bits): to check whether our frame has been acknowledged and correctly received by a node.

* EOF - End of Frame (7 bits): to mark the end of the data frame.
