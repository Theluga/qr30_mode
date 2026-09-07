# QR30 HIDRAW Volume Control

A Bash script for controlling and querying the volume of a **QR30 USB HID device** directly through its `/dev/hidraw*` interface.

The script automatically finds the correct HIDRAW device using the QR30 USB identifiers:

- **Vendor ID:** `2d99`
- **Product ID:** `a101`
- **USB Interface:** `03`

It supports setting the volume from **0–16** and querying the current volume.

---

## Features

- Automatically detects the QR30 HIDRAW device.
- Sets volume from `0` to `16`.
- Queries the current volume.
- Uses raw HID hexadecimal payloads.

---

## Prerequisites

To run this script successfully, your Linux environment must have the following utilities installed:
* `bash` 
* `udevadm`
* `xxd`
* `coreutils` (`dd`, `timeout`, etc.)

--- 

## Usage 

```
./qr30_mode -v g # queries the volume
./qr30_mode -v [0-16] # sets volume level
./qr30_mode -v 0 # volume 0 (muted)
```
