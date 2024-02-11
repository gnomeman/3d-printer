# Klipper

## Big Tree Tech SKR Mini v3

### Firmware

``` bash
make menuconfig
# quit to save
make
# firmware will bin in /out directory
```

- [x] Enable extra low-level configuration options
- [x] Microcontroller architecture `STMicroelectronics STM32`
- [x] Processor model `STM32G0B1`
- [x] Bootloader offset `8KiB bootloader`
- [x] Clock Reference `8 MHz crystal)
- [x] Communication interface `Serial (on USART2 PA3/PA2`
- [x] Baud rate for serial port `250000`
- [ ] GPIO pins to set at micro-controller startup


### Config

On the Raspberry Pi, add the `$HOME/printer_data/config` file from the SKR Mini v3 repo.
Make sure the UART option is enabled for hardwired Pi.

```
[mcu]
serial: /dev/ttyAMA0
restart_method: command
```

BLTouch requires a pullup.

```
[bltouch]
sensor_pin: ^PC14
```


### Raspberry Pi

The following pins need to be paired:

```
Raspberry Pi <==> SKR Mini v3.0 TFT pins
      P4 +5V <==> +5V
      P6 GND <==> GND
     P8 TXD0 <==> RX2
    P10 RXDO <==> TX2
```



# Setup after Klipper install

## Calibrations

### Config files

### X and Y offsets

### Z offset

### Macros
