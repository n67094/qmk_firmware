# How to Raspberry Pi RP2040 (.UF2)

To ensure compatibility with the rp2040 bootloader, make sure this block is present in your rules.mk: 

```
BOOTLOADER = rp2040
```

## Compiling
```
qmk compile -e CONVERT_TO=promicro_rp2040 
```

# Flashing

Flashing sequence:

    1. Enter the bootloader using any of the following methods:
        - Tap the QK_BOOT keycode
        - Hold the BOOTSEL button on the PCB while plugin in the usb cable.
        - Double-tap the RESET button on the PCB1.
    2. Wait for the OS to detect the device
    3. Copy the .uf2 file to the new USB disk
    4. Wait for the keyboard to become available
