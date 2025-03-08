# Klipper config

## Printer

Sapphire pro

## Board

MKS Robin nano v1.2

## Install procedure

### Octoprint:
```
cd ~
git clone https://github.com/Klipper3d/klipper
./klipper/scripts/install-octopi.sh
```

On octoprint GUI:
Settings tab (wrench icon) -> Serial Connection -> Additional serial ports -> add /tmp/printer
Settings tab (wrench icon) -> Serial Connection -> Behavior -> Cancel any ongoing prints but stay connected to the printer

### MCU firmware:
```
make menuconfig # see menuconfig options here: config/printer-twotrees-sapphire-pro-sp-3-2020.cfg
make
./scripts/update_mks_robin.py out/klipper.bin out/Robin_nano35.bin
```
Copy out/Robin_nano35.bin into SD card, power cycle printer.

