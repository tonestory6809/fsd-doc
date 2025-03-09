# Adding and removing clients #

The following commands are used to login/logoff itself by the client.

## Adding clients ##

### ATC ###

```
#AA(callsign):(unused):(real name):(network ID):(password):(rating):(protocol version)
```

| Placeholder      | type    | details                                              |
| ---------------- | ------- | ---------------------------------------------------- |
| callsign         | string  | See [Definitions](../intro/defs.md#definitions)      |
| unused           | any     | Unused paramater, ignored by FSD 4, usually `SERVER` |
| real name        | string  | Real name of the user                                |
| network ID       | string  | See [Definitions](../intro/defs.md#definitions)      |
| password         | string  | Plain password                                       |
| rating           | integer | See [ATC ratings](../intro/defs.md#atc-ratings)      |
| protocol version | integer | See [Definitions](../intro/defs.md#definitions)      |

### Pilots ###

```
#AP(callsign):SERVER:(network ID):(password):(rating):(protocol version):(simtype):(real name)
```

| Placeholder      | type    | details                                                        |
| ---------------- | ------- | -------------------------------------------------------------- |
| callsign         | string  | See [Definitions](../intro/defs.md#definitions)                |
| unused           | any     | Unused paramater, ignored by FSD 4, usually `SERVER`           |
| network ID       | string  | See [Definitions](../intro/defs.md#definitions)                |
| password         | string  | Plain password                                                 |
| rating           | integer | See [Pilot ratings](../intro/defs.md#pilot-ratings), usually 1 |
| protocol version | integer | See [Definitions](../intro/defs.md#definitions)                |
| simtype          | integer | Unknown, marked as `simtype` in FSD 4, usually 10              |
| real name        | string  | Real name of the user                                          |

## Removing clients ##

### ATC ###

```
#DA(callsign)
```

### Pilots ###

```
#DP(callsign)
```

