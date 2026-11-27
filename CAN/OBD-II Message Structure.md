# OBD-II Message Structure

* **OBD-II Message Parts**:
  * **Mode**:
    * Mode is a number Specified under SAE J1949 Standard under which multiple PIDs are Specified.
    * There are 10 Such modes under SAE J1949 Standard.
    * It is not compulsory that all 10 modes are supported and there could also be OEM defined proprietory modes.

  * **PID - Parameter ID**
    * PID is a number that uniquely identifies a parameter for which the data length and Conversion formula are specified.
    * Under a mode there could be hundreds of PIDs, though some mode do not have a single PID.
    * It is not compulsory that all PIDs are supported.
    * the PIDs 00, 20, 40, 60 and so on are the PIDs that are used to request the exact number of PIDs supported under that range. for example for PID 00 is used to identify the PIDs supported under the range 01 to 20.

* **OBD-II Request**: [Mode][PID]
  * A request always has a Mode ID
  * PID is not compulsory as there are some modes that do not have PIDs

* **OBD-II Response**: [Response SID][PID][Data-Bytes]
  * A response always has a Response SID.
  * PID and Data-Bytes are not compulsory as some modes do not ask for Data. for example a mode 04: Clear DTCs.



# Doubts

** Enter the doubts you encountered here **



# Reference

** Enter the references you used to study this concept here **