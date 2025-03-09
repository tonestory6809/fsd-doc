# Definitions #

| Term                            | Definition                                                                                                                                                                                                 |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Callsign                        | The unique identifier that a client is logged in as; e.g. `AAL123`, `EGLL_TWR`, `XX_SUP`, etc. Callsign must not contain any of `!@#$%*:& <tab>` and its length must be greater than 1 and lesser than 13. |
| Client                          | A pilot or ATC station. For the purposes of FSD, observers are considered to be ATC stations.                                                                                                              |
| Frequency (freq)                | The network analogue to VHF frequencies used for aircraft radio communication. For the purposes of FSD, observers are always tuned to **199.998 MHz**.                                                     |
| Latitude (lat), longitude (lon) | Latitude and longitude. They have a precision of 5 decimal places.                                                                                                                                         |
| Network ID                      | A unique ID used by the network, aka. CID                                                                                                                                                                  |
| Protocol version                | The version of the FSD protocol being used by the client. FSD uses 9.                                                                                                                                      |
| Rating                          | The ATC or pilot rating, as assigned by the network. This is stored as an integer; the lowest rating is `1`. Examples: S1/C2/C3, AS3/ADC, FS3/SPP, etc.                                                    |
| Server                          | A FSD server.                                                                                                                                                                                              |
| Packet                          | A formatted unit of data sent over an FSD network, see [Overview](../api/packet.md#overview)                                                                                                               |

Placeholders are indicated using brackets; e.g. `(client)`.



# Ratings #

Each user has a pilot and ATC rating. 

This is stored as an integer inside `cert.txt` on the server, but is advertised by IVAO and VATSIM under the following names:

## ATC ratings ##

| `cert.txt` value | VATSIM rating | IVAO rating |
| ---------------- | ------------- | ----------- |
| 1                | OBS           |             |
| 2                | S1            | AS1         |
| 3                | S2            | AS2         |
| 4                | S3            | AS3         |
| 5                | C1            | ADC         |
| 6                | C2            |             |
| 7                | C3            | ACC         |
| 8                | I1            |             |
| 9                | I2            |             |
| 10               | I3            |             |
| 11               | SUP           |             |
| 12               | ADM           |             |


## Pilot ratings ##

| `cert.txt` value | VATSIM rating | IVAO rating |
| ---------------- | ------------- | ----------- |
| 1                | No rating     |             |
| 2                |               | FS1         |
| 3                |               | FS2         |
| 4                |               | FS3         |
| 5                |               | PP          |
| 6                |               | SPP         |
| 7                |               | CP          |
| 8                |               | ATP         |
| 9                |               | SFI         |
| 10               |               |             |
| 11               | P1            |             |
