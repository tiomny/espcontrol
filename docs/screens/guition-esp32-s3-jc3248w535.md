---
title: 3.5-inch Guition JC3248W535
description:
  EspControl on the Guition JC3248W535 — a 3.5-inch 320x480 portrait touchscreen with up to 24 cards, powered by ESP32-S3.
---

# 3.5-inch JC3248W535

The **Guition JC3248W535** is a compact 3.5-inch portrait touchscreen powered by an **ESP32-S3** processor. It uses a Quad-SPI MIPI display with the combined AXS15231B display/touch controller, and offers plenty of room for a dense **4×6 card grid** — up to **24 cards** on the home screen.

## Card Grid

<!--@include: ../generated/screens/guition-esp32-s3-jc3248w535-grid.md-->

## Install

Connect the display to your computer with a USB-C data cable, then click the button below.

<!--@include: ../generated/screens/guition-esp32-s3-jc3248w535-install.md-->

For a full walkthrough including WiFi setup and Home Assistant pairing, see the [Install guide](/getting-started/install).

::: tip After flashing or OTA update
This panel uses Quad-SPI with octal PSRAM, which requires a brief hardware reset after flashing or OTA updates. The firmware handles this automatically with a short deep-sleep cycle — the display may flicker once before coming back up normally.
:::

## ESPHome Manual Setup

If you use ESPHome and prefer to compile firmware yourself:

```yaml
substitutions:
  name: "desk-screen"
  friendly_name: "Desk Screen"

wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password

packages:
  setup:
    url: https://github.com/tiomny/espcontrol/
    file: devices/guition-esp32-s3-jc3248w535/packages.yaml
    refresh: 1sec
```
