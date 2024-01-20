# Klipper_makefiles
This repo contains Klipper and Canboot config files for MCUs on my printers. 

I find that remembering how to set my menuconfig options everytime I need to recompile the firmware is a pain. So instead of remembering what I did each time I simply copy the appropriate config file for the MCU I am updating to the klipper or canboot folder. Remove the existing `.config` file and copy my backup to `.config`. E.g., when updating my Manta E3EZ board, I do the following. 


```
make clean
rm .config
cp manta.config .config
make
```

I then repeat for all my MCU's. i.e., SB2209-RP2040

```
make clean
rm .config
cp sb.config .config
make
```

In the future I will turn this into a script so that I can just update from within the mainsail console.