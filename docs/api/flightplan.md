# Flight plan #

Used by the client to file a flight plan.

```
$FP(callsign):(unused):(type):(aircraft):(tascruise):(depairport):(deptime):(actdeptime):(alt):(destairport):(hrsenroute):(minenroute):(hrsfuel):(minfuel):(altairport):(remarks):(route)
```

| Placeholder | type    | details                                                                                                                                        |
| ----------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| callsign    | string  | See [Definitions](../intro/defs.md#definitions)                                                                                                |
| unused      | any     | Unused paramater, ignored by FSD 4, usually `SERVER`                                                                                           |
| type        | string  | `V` for VFR or `I` for IFR                                                                                                                     |
| aircraft    | string  | See [Aircraft and equipment](#aircraft-and-equipment)                                                                                         |
| tascruise   | integer | TAS during cruise                                                                                                                              |
| depairport  | string  | Departure airport ICAO                                                                                                                         |
| deptime     | integer | Estimated departure time                                                                                                                       |
| actdeptime  | integer | Actually departure time                                                                                                                        |
| alt         | string  | Cruise altitude                                                                                                                                |
| destairport | string  | Arrival airport                                                                                                                                |
| hrsenroute  | integer | Hours enroute                                                                                                                                  |
| minenroute  | integer | Minutes enroute                                                                                                                                |
| hrsfuel     | integer | Hours fuel available                                                                                                                           |
| minfuel     | integer | Minutes fuel available                                                                                                                         |
| altairport  | string  | Alternative airport                                                                                                                            |
| remarks     | string  | Remarks delimited by slash, perhaps [this](https://www.reddit.com/r/VATSIM/comments/735lis/what_do_i_expect_to_see_in_your_flight_plan/) helps |
| route       | string  | Air route e.g. `HON UL10 CASEL`                                                                                                                |

## Aircraft and equipment

Reference: [swift-project/pilotclient](https://github.com/swift-project/pilotclient/blob/21bda3b3224e5b822218a742eca22b4002970c09/src/misc/aviation/flightplanaircraftinfo.cpp#L243C92-L243C105)
`(type)(designator)/(equipment)`, e.g. `H/A320/L`

| Placeholder | details                                                                                                                                                                                        |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| type        | `H/` for Heavy and `J/` for Super, else empty                                                                                                                                                  |
| designator  | [ICAO Type Designator](https://en.wikipedia.org/wiki/List_of_aircraft_type_designators) e.g. `A320`, `B738`                                                                                    |
| equipment   | See [swift-project's implementation](https://github.com/swift-project/pilotclient/blob/21bda3b3224e5b822218a742eca22b4002970c09/src/misc/aviation/flightplanaircraftinfo.cpp#L243C92-L243C105) |
