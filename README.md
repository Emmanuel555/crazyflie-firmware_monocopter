# Monocopter Ver

# DSHOT 3D mode (current setup)✓✓✓
Direction flip is instant — just a param write, next DSHOT frame uses the other band
Half the throttle resolution (~999 steps per direction)
Requires ESC firmware support (Bluejay ✓)

# motorsSetDirection (the old approach we deleted)
Permanently reprograms ESC direction — 420ms stop + command sequence every flip
Full throttle resolution (1999 steps)
Motor stops completely during the flip
Totally unusable for frequent direction changes

# Wiring two ESCs/motors in opposite directions
Hardware solution, no software switching at all
Adds weight and complexity


# Installation:
Firmware - DSHOT Stable Tag
ESC - Flash to Bluejay esc firmware using esc configurator (online)
    - Connect battery to bolt and turn it off
    - Connect via USB cable to com for serial connection and turn on bolt
    - Flash with PWM freq of 24khz for 300 khz DSHOT protocol
    - Flash with forward/reverse direction (Bidirectional 3D Mode)
    - **Demag Compensation (default is low) set to high
    - **Brakes on stop (default is NOT selected) set to selected
    - **Set timing to (default is Medium High) low
    - Write settings at the bottom next to read settings 
    

# Bolt firmware flashing:
DISABLE the following cos NO telem provided...
- Enable bi-directional DSHOT (RPM measurements)  

# Crazyflie Firmware  [![CI](https://github.com/bitcraze/crazyflie-firmware/workflows/CI/badge.svg)](https://github.com/bitcraze/crazyflie-firmware/actions?query=workflow%3ACI)

This project contains the source code for the firmware used in the Crazyflie range of platforms, including the Crazyflie 2.x and the Roadrunner.

### Crazyflie 1.0 support

The 2017.06 release was the last release with Crazyflie 1.0 support. If you want
to play with the Crazyflie 1.0 and modify the code, please clone this repo and
branch off from the 2017.06 tag.

## Building and Flashing
See the [building and flashing instructions](https://github.com/bitcraze/crazyflie-firmware/blob/master/docs/building-and-flashing/build.md) in the github docs folder.


## Official Documentation

Check out the [Bitcraze crazyflie-firmware documentation](https://www.bitcraze.io/documentation/repository/crazyflie-firmware/master/) on our website.

## Generated documentation

The easiest way to generate the API documentation is to use the [toolbelt](https://github.com/bitcraze/toolbelt)

```tb build-docs```

and to view it in a web page

```tb docs```

## Contribute
Go to the [contribute page](https://www.bitcraze.io/contribute/) on our website to learn more.

### Test code for contribution

To run the tests please have a look at the [unit test documentation](https://www.bitcraze.io/documentation/repository/crazyflie-firmware/master/development/unit_testing/).

## License

The code is licensed under LGPL-3.0
