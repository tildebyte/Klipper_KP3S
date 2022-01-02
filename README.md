# Klipper KP3S 3.0
![alt text](https://github.com/9R/klipper_KP3S/blob/main/klipper%20kp3s_30.png?raw=true)


##Changes from upstream

* Fork of nehilo's klipper config with adjustments for Titan extruder

* The config is set up for connecting a 3d Touch sensor additionally to the default z endstop.
  The3D touch sensor pin is connected to the Z+ connector on the main board. In this config Homing
  is done with the z -endstop and the 3d-touch sensor is used only for probing.

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

You question and main information you can checked https://cutt.ly/Cgow7vL
