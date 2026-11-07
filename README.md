# Raspberry Pi Pico — DHT22 Sensor Project

A MicroPython project for the **Raspberry Pi Pico (RP2040)** that reads temperature and relative humidity from a DHT22 sensor. The repository includes a custom driver using the RP2040's Programmable I/O (PIO), plus I²C LCD support modules.

## Features

- DHT22 temperature and humidity readings
- RP2040 PIO state machine for sensor timing and data capture
- Configurable sensor data and optional power-control pins
- Checksum validation before returning readings
- I²C LCD helper modules included in the repository
- Repeated sensor polling with a delay between readings

## Hardware

- Raspberry Pi Pico / RP2040 board
- DHT22 temperature and humidity sensor
- Jumper wires and breadboard
- Optional I²C LCD compatible with the included helper modules

### Example wiring

| Component | Pico GPIO |
| --- | --- |
| DHT22 data | GP15 |
| Optional sensor power control | GP14 |

Check your sensor module's pinout and electrical requirements before wiring. Never connect a 5 V signal directly to a Pico GPIO.

## Repository files

| File | Purpose |
| --- | --- |
| `DHT22.py` | DHT22 driver using RP2040 PIO |
| `main.py` | Main sensor example |
| `lcd_api.py` | LCD API helper |
| `pico_i2c_lcd.py` | I²C LCD driver helper |

## Requirements

- Raspberry Pi Pico with MicroPython firmware supporting `rp2` PIO
- Thonny or another MicroPython-compatible editor
- DHT22 sensor and wiring

## Run the project

1. Flash compatible MicroPython firmware to the Pico.
2. Connect the DHT22 data line to GP15 as used by the example.
3. Copy `DHT22.py`, `main.py`, and the LCD helper files (if required) to the board.
4. Open the serial/REPL output in Thonny.
5. Run `main.py` and monitor the temperature and humidity readings.

The example configures GP14 as an optional sensor power-control pin. Adjust the code and wiring if your setup differs.

## What this project demonstrates

- MicroPython development on a microcontroller
- RP2040 PIO state-machine concepts
- Digital sensor communication
- Hardware/software integration
- I²C display driver modules

## Future improvements

- Add a wiring diagram and real hardware photos
- Add data logging and display output
- Add Wi-Fi telemetry using a suitable network-enabled board
- Document calibration and error-handling tests

## Author

**Pratik Poudel** · [GitHub](https://github.com/pyatrick666)

> Hardware photos and a demonstration video will be added in a later update.
