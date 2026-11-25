# J19239 Message Types

1. Command:
    * Tells the recipient ECU to do something

2. Request
    * PGN: 0XEA00
    * Asks the recipient ECU for some data.
    * In case of directed request, the ECU responds with negative acknoledgement if requested PGN is not supported
    * In case of global request, the ECU does not respond if requested PGN is not supported.

3. Broadcast/Response:
    * Transmitted by the ECU that has processed a command or requested some data.
    * Also transmitted by the ECU that was configured to broadcast.

4. Acknowledgement:
    * PGN: 0XE800
    * The first byte of payload specifies what type of Acknowledgement:
      * 0X00: Positive Response
      * 0X01: Negative Response
      * OXO2: Access denied
      * 0X03: Cannot responds/Busy

5. Group Functions:
    * Some PGN are reserved for manufacturers that want to specify propritory functions.



# Doubts

** Enter the doubts you encountered here **



# Reference

https://wellstsai.com/en/post/j1939-introduction/#message-types