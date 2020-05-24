# Virtual Devices

Virtual CAN devices, or vcan devices, can be used to simulate a CAN bus without any hardware. This is useful for simulation, testing, and bridging. It also lets you try out can-utils without having an actual CAN device. 

To create a vcan device run: 
```
sudo ip link add name vcan0 type vcan
```

Once created, the device can be used like a hardware device. It does not require a bitrate setting, but the interface must be enabled before use:
```
sudo ip link set up vcan0
```