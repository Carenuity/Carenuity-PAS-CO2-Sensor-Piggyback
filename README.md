# Carenuity PAS CO₂ Piggyback

![image alt](https://github.com/0mollo/Carenuity-PAS-CO2-Piggyack/blob/main/PAS%20CO2%20Sensor%20Piggyback.pdf) ![image alt]()
Piggyback PCB for the **Infineon XENSIV™ PAS CO₂** sensor, designed for easy integration into the **Carenuity modular hardware ecosystem**.

## Features

- Supports XENSIV PAS CO₂ sensor interface
- Compact piggyback form factor
- Breaks out key communication and control pins
- I2C pull-up resistor support included
- Suitable for ESP32-C3 Mini style integrations
- Clean modular layout for prototyping and product development


Used for I2C pull-up on:
- SCL
- SDA


## Board Notes

- Designed as a sensor piggyback module
- Carries Carenuity branding
- Board revision shown: **V1.1**
- Best treated as a **3.3V logic** interface unless otherwise confirmed in the sensor documentation

  # Pinout

## Signal List

| Signal | Description |
|--------|-------------|
| TX     | UART transmit |
| RX     | UART receive |
| SCL    | I2C clock |
| SDA    | I2C data |
| PWM    | PWM output/interface |
| PSEL   | Interface select |
| INT    | Interrupt |
| GND    | Ground |
| 3V3    | 3.3V supply |
| 5V     | 5V supply |

## I2C Pull-ups

| Ref | Value |
|-----|-------|
| R1  | 10K   |
| R2  | 10K   |

Pull-ups are connected to **3V3**.

## Applications

- CO₂ monitoring
- Indoor air quality systems
- Embedded sensor development
- IoT environmental monitoring

## Firmware/Example

#include <Wire.h>

void setup() {
  Serial.begin(115200);
  Wire.begin();
  Serial.println("I2C scan started");
}

void loop() {
  byte error, address;
  int count = 0;

  for (address = 1; address < 127; address++) {
    Wire.beginTransmission(address);
    error = Wire.endTransmission();

    if (error == 0) {
      Serial.print("Found device at 0x");
      if (address < 16) Serial.print("0");
      Serial.println(address, HEX);
      count++;
    }
  }

  if (count == 0) {
    Serial.println("No I2C devices found");
  }

  delay(3000);
}
## License

Recommended:
- **MIT** for firmware
