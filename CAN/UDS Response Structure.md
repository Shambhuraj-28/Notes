# UDS Response Structure
* UDS Reponse is sent by the server aka ECU after it completes the processing of the request.
* There are two types of UDS Reponses:
  * Positive Response: Positve response is sent by when ECU it Succesfully completes the operations mentioned under a Service.
  * Negative Response: Negative Response Structure is sent by ECU when a service is not supported or it fails to complete the operations mentioned under a service.

* Positve Response Structure
  * Positive Resposne Structure: [SID][Subfunction-Identifier][Data]
  * SID - Service Identifier but in case of positive reposnse SID (request) + 0x40
  * Subfunction-identifier same as in request
  * Data - Different from request

* Negative Response Structure
  * Negative Response Strtuctre: [NRSID][RSID][NRC]
  * NRSID: Negative Response Service ID - 8 Byte. it is used in case of Service ID.
  * Rejected SID: The SID that was sent in request but was rejected (8 byte)
  * NRC: Negative Response Code. An error code that points towards the explanation behind the negative response.
  



# Doubts

** Enter the doubts you encountered here **



# Reference

** Enter the references you used to study this concept here **