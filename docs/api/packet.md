# Overview #

We call byte strings delimited by semicolons and terminated by `\r\n` as packets, or PDUs in swift-project.
Example: `#??FOO:BAR:1234\r\n`
Here, we call `#??` as the command (or PDU identifier in swift-project), `FOO`, `BAR`, `1234` as parts (or tokens in swift-project).

Most packets follow the format below:
```
(command)(source):(destination):(data)\r\n
```
In FSD4, most packets also allows more parts than required and they'll be ignored.

## `command` ##

The name of the command. See each section for the commands.

Each command is prefixed with one of the following:

| Symbol | Details                                |
| ------ | -------------------------------------- |
| `$`    | Requests and responses                 |
| `#`    | Adding/removing clients, text messages |
| `%`    | ATC update                             |
| `@`    | Aircraft update                        |
See TOC for full list of commands.


## `destination` ##

The destination of the packet. This may be any one of the following. Case does not seem to matter:

* `SERVER`
* `FP`
* The callsign of an online station / aircraft

Some packets allows more broadcast destinations.

## `source` ##

The sender of the packet. See `destination` for valid formats.



## `data` ##

The content of the packet. See the following sections for valid formats.


