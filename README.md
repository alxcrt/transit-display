# Smart Transit Display

Real-time public transit arrival display built with ESP32-S3 and HUB75 LED matrix panels.

## Features

- Real-time bus/tram arrival times
- 64x128 pixel LED matrix display (2x 64x32 panels)
- WiFi connectivity for live data
- Customizable routes and styling
- Low-cost DIY build (~$70 USD)

## Hardware

| Component | Description |
|-----------|-------------|
| ESP32-S3 | Microcontroller with WiFi |
| HUB75 LED Matrix | 64x32 RGB LED panel (x2) |
| 5V Power Supply | 4A minimum recommended |

## Firmware

Built with [ESPHome](https://esphome.io/) for easy configuration and OTA updates.

### Quick Start

1. Install ESPHome:
   ```bash
   pip install esphome
   ```

2. Configure WiFi in `firmware/simple-display.yaml`:
   ```yaml
   wifi:
     ssid: "YourNetwork"
     password: "YourPassword"
   ```

3. Flash to ESP32:
   ```bash
   cd firmware
   esphome run simple-display.yaml
   ```

## Pin Configuration

```
R1: GPIO42    G1: GPIO40    B1: GPIO41
R2: GPIO38    G2: GPIO37    B2: GPIO39
A:  GPIO45    B:  GPIO36    C:  GPIO48
D:  GPIO35    E:  GPIO21
LAT: GPIO47   OE: GPIO14    CLK: GPIO2
```

## License

MIT
