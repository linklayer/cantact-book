# Hardware Devices

A hardware device is required to connect to a real CAN bus. When using hardware SocketCAN devices, each hardware CAN channel is given a number based on the order which the devices were connected in. The first device's first channel will be `can0`. 

To set up a device with channel `can0` at a bitrate of 500000 kbps:
1. Connect the device to a Linux computer
2. Set the device bitrate: 
```
sudo ip link set can0 type can bitrate 500000
```
3. Bring the interface up:
```
sudo ip link set up can0
```
