# About

GCC based template for interfacing SSD1306 based Adafruit 128*32 OLED driver. Modified from the Adafruit_GFX library from mbed by Neal Horman. Adapted to work with NRF5 SDK.

# State

* Only I2C mode is supported
* Graphics mapping for fonts etc., broken
* One to one pixel mapping done (You will have to cook up your own algorithm to come up with fonts etc on the screen)


# Instructions to use

NRF5 sdk is not included. Given below is my folder structure to get this project compiling:

```
.
├── components
│   ├── ant
│   ├── ble
│   ├── boards
│   ├── device
│   ├── drivers_ext
│   ├── drivers_nrf
│   ├── libraries
│   ├── nfc
│   ├── proprietary_rf
│   ├── sdk_validation.h
│   ├── serialization
│   ├── softdevice
│   └── toolchain
├── external
│   ├── cifra_AES128-EAX
│   ├── fatfs
│   ├── freertos
│   ├── licenses_external.txt
│   ├── micro-ecc
│   ├── nano-pb
│   ├── nfc_adafruit_library
│   ├── nrf_cc310
│   ├── protothreads
│   ├── rtx
│   ├── segger_rtt
│   └── tiny-AES128
├── src
│   ├── binary.h
│   ├── ble_app_uart_gcc_nrf52.ld
│   ├── glcdfont.c
│   ├── main.c
│   ├── Makefile
│   ├── sdk_config.h
│   ├── spi_module.c
│   ├── spi_module.h
│   ├── ssd1306.c
│   ├── ssd1306.h
│   ├── uart_module.c
│   └── uart_module.h
```

Navigate to `src` folder and run `make`, then `make flash` or `make flash_softdevice`

Only tested on Linux.
