# UDS Request Structure
UDS Request: [SID][Subfunction-Identifier>][Request-Parameters]  
SID - Service Identifier (1 byte i.e. 8 bits)
  * Service Identifier is a number that points towards the specific service. A service specifies a single operation or a set of operations to be performed by the server.

Subfubction Identifier (1 byte i.e. 8 bits)
  * It is number that points towards a specific single operation inside a service. Services that perform a single operation does not have a Subfunction Identifier.

Request Parameters (Variable bit length, depending on the service and subfunction used)
  * to peform an operation some data might be required that data is called request parameters.



# Doubts

** Enter the doubts you encountered here **



# Reference

** Enter the references you used to study this concept here **