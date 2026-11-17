# CAN Frame Types
There are 4 types of CAN Frames:

1. Data frame:
  * The structure of Data frame is as specified by standards such as CAN 2.0A and CAN 2.0B.
  * These frames are used for normal data transmission. for example sensor readings.
  * This is most commnly used type of CAN frames.

2. Error Frame:
  * Error frame is transmitted by a node when it detects a communication error.
  * error frames have 2 fields:
    * Error Flag (6 bits): it is either dominant 0 (active) or recessive 1 (passive).
    * Error Delimeter: it is always recessive 1.

3. Remote Frame:
  * Remote Frame has a strcture similar to that of data frame except here the RTR bit is recessive 1 and it does not have a payload frame.
  * Remote Frame is tranmitted by a node to request data to another node.
  * This type of frame is less commonly used as most high level protocols such as OBD2 and UDS can reliable request by using a data frame.

4. Overload Frame:
  * Overload frame is tranmitted when a node wants some delay before transmitting it's next frame.
  * overload frame has 2 fields:
    * Overload Flag (6 bits): it is always dominent 0 and supresses the frame transmission for a whiel
    * Overload delimeter (6 bits): it is always recessive 1.