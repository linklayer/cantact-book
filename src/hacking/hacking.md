# Hacking

Want to hack on CANtact? Great!

All CANtact related development takes place on Github. If you find a bug, please file an issue there. There are several relevant repositories containing code and design files.

## CANtact CLI and Driver

The CANtact CLI and Driver are written in Rust. The repository can be found [on Github](https://github.com/linklayer/cantact).

## CANtact Pro

Design files and firmware for CANtact Pro:

- [CANtact Pro Hardware](https://github.com/linklayer/cantact-pro-hw)
- [CANtact Pro Firmware](https://github.com/linklayer/cantact-pro-fw)

## CANtact

Design files and firmware for CANtact:
- [CANtact Hardware Repository](https://github.com/linklayer/cantact-hw)
- [CANtact SLCAN Firmware](https://github.com/linklayer/cantact-fw)
- [candleLight Firmware for CANtact](https://github.com/candle-usb/candleLight_fw)

### Hardware
CANtact and CANtact Pro is designed using the open source [KiCAD EDA](https://kicad-pcb.org/) suite.

### Firmware

The CANtact Pro is powered by an NXP LPC546xx series microcontroller (specifically, the [LPC54616J512BD100](https://www.nxp.com/products/processors-and-microcontrollers/arm-microcontrollers/general-purpose-mcus/lpc54000-cortex-m4-/power-efficient-microcontrollers-mcus-with-advanced-peripherals-based-on-arm-cortex-m4-core:LPC546XX?fpsp=1&tab=Documentation_Tab)). 

NXP provides their [MCUXpresso IDE](https://www.nxp.com/design/software/development-software/mcuxpresso-software-and-tools/mcuxpresso-integrated-development-environment-ide:MCUXpresso-IDE)
free of charge, which can be used to develop and debug firmware for the device.

