# Klipper KP3S 3.0
![alt text](https://github.com/9R/klipper_KP3S/blob/main/klipper%20kp3s_30.png?raw=true)

# HOST Recommendation

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

![alt text](https://github.com/nehilo/Klipper-KingRoon-Printers/blob/main/pic/stm32.png?raw=true)

***GD32F103 / F303***

![alt text](https://github.com/nehilo/Klipper-KingRoon-Printers/blob/main/pic/GD32.jpg?raw=true)

```bash
make 
```

```bash
./scripts/update_mks_robin.py out/klipper.bin out/Robin_nano.bin
```

If you don`t want to use LCD and turn off cable from motherboard:


```bash
./scripts/update_mks_robin.py out/klipper.bin out/Robin_nano43.bin
```

# TMC UART Pin KingRoon Motherboard ( FOR ADVANCED USERS )

Manual:

KP3S 1.2 Motherboard
https://www.youtube.com/watch?v=BF19ZXk5KRw

KP3S 1.3 Motherboard
https://youtu.be/2X_U2wZV_pw


Pins:
```bash
X:PA5　Y:PC13　Z:PC7　E:PA10  E1:PA9
```

Thanks for Video to [こんゆたか](https://www.youtube.com/@user-wk7lu7ph4e)


# Basic Files Folder Configuration

```bash
 -printer.cfg
 -stepper.cfg
 -extruder.cfg
 -bed.cfg
 -fan.cfg
 -thermistor.cfg
 -macros
    macros.cfg
    printing.cfg
```

# Advanced Files Folder Configuration

```bash
 -printer.cfg
 -stepper.cfg
 -bltouch.cfg
 -tmc.cfg
 -extruder.cfg
 -bed.cfg
 -fan.cfg
 -thermistor.cfg
 -macros
    macros.cfg
    printing.cfg
```

You question and main information you can checked https://cutt.ly/5LHo4yC
