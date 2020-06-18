# Getting SocketCAN

Specifics for installing SocketCAN will depend on your Linux distribution.

## Ubuntu & Debian

SocketCAN is built into the kernel provided with these systems. You will need to install the `can-utils` package to use the SocketCAN utilities (candump, cansend, etc...):
```
sudo apt-get install can-utils
```
