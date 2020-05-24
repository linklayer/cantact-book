# Utilities

The SocketCAN utilities provide simple command-line tools for interacting with CAN buses.

## candump
candump displays messages on the specified CAN bus. To show all traffic in real time on device can0:
```
candump can0
```

The displayed messages can be filtered using a mask and identifier. Two filter types are available: 

- `[can_id]:[can_mask]` matches when `[received_can_id] & [can_mask] == [can_id] & [mask]`
- `[can_id]~[can_mask]` matches when `[received_can_id] & [can_mask] != [can_id] & [mask]`  

### Examples
Only show messages with ID 0x123 on vcan0:
```
candump vcan0,0x123:0x7FF
```

Only show messages with ID 0x123 or ID 0x456 on can3:
```
candump can3,0x123:0x7FF,0x456:0x7FF  
```

## cansend
cansend sends a single CAN frame on the bus using the specified identifier and data bytes. For example:
```
cansend can0 123#1122334455667788
```

This sends a message on interface `can0` with identifier `0x123` and data bytes `[0x11, 0x22, 0x33, 0x44, 0x55, 0x66, 0x77, 0x88]`. This tool assumes all values (ID and data) are provided in hexadecimal. 

## cangen
cangen can generate random CAN data, which can be useful for testing. Run `cangen` for detailed usage information. 

## cansniffer
cansniffer displays frames that are currently on the bus, but filters out frames with data that is not changing. This is very useful for reverse engineering CAN bus systems. Run `cansniffer` for detailed usage information.
