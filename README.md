# Yamaha RX-450 IR Control via RM4C Mini + Home Assistant

This document describes a simple way to control a Yamaha RX-450 using a Broadlink RM4C Mini with Home Assistant.

## Setup

Copy the contents of `scripts.yaml` into your Home Assistant `scripts.yaml` file.

## Usage

```yaml
service: script.send_ir_code
data:
  transmitter: remote.blaster_ir
  device_name: yamaha_rx450
  command_name: vol_up
  repeats: 2
  delay_secs: 0.15
```

## Example UI

There is a simple control panel example using `custom:button-card` in `buttons.yaml`.
