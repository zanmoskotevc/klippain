# Setting up Cartographer

>**THIS IS ONLY FOR FIRMWARE WITH SURVEY TOUCH ENABLED (>4.0.1)**  
> Older versions of firmware are not supported.

As things tend to change over time and get updated, please always check official instructions on [Cartographer 3D website](https://docs.cartographer3d.com/cartographer-probe/survey-touch) and the files from Klippain to make sure everything is setup correctly.

## 1. Install Klipper module
Follow the instructions on the Cartographer 3D website [here](https://docs.cartographer3d.com/cartographer-probe/installation-and-setup/klipper-setup).

## 2. Update Firmware
Follow the instructions on the Cartographer 3D website [here](https://docs.cartographer3d.com/cartographer-probe/firmware/firmware-updating).

## 3. Modify printer.cfg
Uncomment this line by removing the `# `.
```
# [include config/hardware/probes/cartographer_virtual.cfg]
```
It should like this:
```
[include config/hardware/probes/cartographer_virtual.cfg]
```

## 4. Modify mcu.cfg
Set your serial or CANBUS UUID in the `[scanner]` section.

## 5. (OPTIONAL) Enable accelerometer
If your board has an accelerometer, you can enable it by uncommenting it in the **printer.cfg**
  
Uncomment **one** of these two lines, depending on the sensor you have.
```
# [include config/hardware/accelerometers/adxl345_cartographer.cfg]
# [include config/hardware/accelerometers/lis2dw_cartographer.cfg]
```

## 6. Continue with official instructions
For calibration and everything else, follow the official instructions [here](https://docs.cartographer3d.com/cartographer-probe/survey-touch#first-print).