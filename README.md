# Gameboy Zero RetroPie status overlays
This repository contains a script to display lovely slightly-transparent overlays on top of your RetroPie games and emulationstation menus

This is a fork created for the TinkerBoy 3.0.1 Contoller board with Li-Ion battery soldered to the BATT+ pin.

## What can it do?
- adjust to the current resolution
- gracefully shut down the Pi after 60s from when voltage goes below 3.2V
- show a big imminent shutdown warning when the counter starts ticking
- display battery level (charging, discharging, %, critical)
- display WiFi state (connected/disconnected/disabled)
- display Bluetooth state (connected/disconnected/disabled)
- display under-voltage state
- display warning if frequency-capped
- display warning if throttling

## What do I need to get it running?
- [pngview](https://github.com/AndrewFromMelbourne/raspidmx/tree/master/pngview) from AndrewFromMelbourne
- [material-design-icons](https://github.com/google/material-design-icons/archive/master.zip) from Google
- Tinkerboy Controller 3.0.1 https://www.tinkerboy.xyz/getting-started-guide-for-tinkerboy-controller-v3-0/
- a symbolic link to *overlay\_icons/ic\_battery\_alert\_red\_white\_36dp.png* under *material\_design\_icons\_master/device/drawable-mdpi/*
- an entry in /etc/rc.local
- check and adjust paths in the script header
- some battery readings calibration - check logs
- some patience

## But what does it look like?
Like that:

![Bluetooth, wifi connected, battery discharging](_images/connected.png)  
Bluetooth, wifi connected, battery discharging

![Bluetooth, wifi disconnected, battery discharging](_images/disconnected.png)  
Bluetooth, wifi disconnected, battery discharging

![Bluetooth, wifi disabled, battery charging](_images/disabled_charging.png)  
Bluetooth, wifi disabled, battery charging

![CPU throttled due to high temperature](_images/throttle.png)  
CPU throttled due to high temperature

![Under-Voltage, Freq-capped due to high temperature, battery critical, shutdown imminent warning](_images/freqcap_undervolt_criticalbat_shutdown.png)  
Under-Voltage, Freq-capped due to high temperature, battery critical, shutdown imminent warning - shutting down in 60s

![In-game](_images/ingame.png)  
In-game

