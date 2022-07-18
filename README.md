# Klipper KP3S
![alt text](https://github.com/nehilo/klipper_KP3S/blob/main/klipper%20kp3s.png?raw=true)


# Firmware build

```bash
cd ~/klipper
```
```bash
make menuconfig
```

***STM32F103***

![alt text](https://github.com/nehilo/klipper_KP3S/blob/main/make.png?raw=true)

***GD32F103***

![alt text](https://github.com/nehilo/Klipper_KingRoon_KP3S/blob/main/GD32.jpg?raw=true)

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

# TMC UART Pin KingRoon 1.3 Motherboard

![alt text](https://github.com/nehilo/Klipper_KingRoon_KP3S/blob/main/UART_Kingroon%201.3.jpg?raw=true)

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
