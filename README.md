# Klipper KP3S 3.0
![alt text](https://github.com/9R/klipper_KP3S/blob/main/klipper%20kp3s_30.png?raw=true)


##Changes from upstream

* Fork of nehilo's klipper config with adjustments for Titan extruder

* The config is set up for connecting a 3d Touch sensor additionally to the default z endstop.
  The3D touch sensor pin is connected to the Z+ connector on the main board. In this config Homing
  is done with the z -endstop and the 3d-touch sensor is used only for probing.

* This config uses an dropin replacement for the LCD-PCB to drive a ssd1306 display with klipper. 
  See [additional GPIOs](#additional-gpios) for details.

* Tested on a KP3S 3.0 with GD32F303 MCU. Probably works without changes an STM32F103 as well.

# Additional GPIOs

The KP3S' touch screen is of no use when running Klipper firmware. The PCB holding the display 
can be replaced a custom PCB to expose additional GPIOs (including I2C) so more sensors, steppers 
or a Klipper-compatible display and rotary encoder can be attached. Design for a PCB exposing all 
available extra pins in the aperture of the housing where the touch screen resides can be found in 
this [repo](https://github.com/9R/kp3sExpander).

# Firmware build

```bash
cd ~/klipper
```
```bash
make menuconfig
```

![alt text](https://github.com/9R/klipper_KP3S/blob/main/make.png?raw=true)

```bash
make 
```

```bash
./scripts/update_mks_robin.py out/klipper.bin out/Robin_nano.bin
```

# Config Files Folder

```bash
printer.cfg
 -stepper.cfg
 -bltouch.cfg
 -uart.cfg
 -extruder.cfg
 -bed.cfg
 -fan.cfg
 -macros.cfg
```
