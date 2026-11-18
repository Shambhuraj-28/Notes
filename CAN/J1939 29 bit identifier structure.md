# J1939 29 bit identifier structure

The J1939 Identifier 29 bit identifier field has following subfields

* P - Priority (3 bits)
  * The priority subfiled determines the priority of the frame
  * The frame with lowest p i.e zero has highest priority and the frame with highest p has lowest priority.

* PGN - Parameter Group Number (18 bits)  
Parameter Group Number indicates the type of message that is being sent for example sensor value, diagnostic message etc. it is further divided into following sub fields
  * EDP - Extended Data Page (1 bit)
    * Extended Data Page along with Data Page form a number that determines the page to be selected.
  * DP - Data Page (1 bit)
    * Data Page is along with Extended Data Page determines the page to be selected.
  * PF - PDU Format (8 bits)
    * PF Determines how PS will be interpreted.
  * PS - PDU Specific (8 bits)
    * If PF < 240 Then PS is destination address. in this case the frame is sent only for the node with specified destination address. this combination is called as PDU1.
    * else if PF >=240 Then PS is considered extended part of PGN.

* SA - Source Identifier (8 bits)
    * Source Identifier indicates from which node the frame was sent.
    * it is uniquely assigned to each node



# Doubts
What is the Page?



# Reference
https://wellstsai.com/en/post/j1939-introduction/#packet-format