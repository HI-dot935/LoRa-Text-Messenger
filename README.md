A small DIY text messenger built around an ESP32-devkit-v1 and LoRa-module.

The idea is pretty simple: build two standalone devices that can send text messages to each other without Wi-Fi, Bluetooth, or a phone. Each unit has a keypad for typing, an OLED display for the interface, and an RFM95W LoRa module for the radio link.

Typing uses the old-school Nokia-style multi-tap system, so letters can be entered using a normal 3×4 keypad. Messages are sent between the two devices over LoRa, with acknowledgements and retries so the sender can tell whether the message was received.

Hardware
ESP32
RFM95W / SX1276 LoRa module
SSD1306 OLED display
3×4 matrix keypad
TCA8418 keypad controller
Li-ion battery
PowerBoost 1000C
What it does
Two-device A ↔ B messaging
Nokia-style multi-tap typing
A–Z and 0–9 input
OLED-based interface
LoRa communication
Message IDs and delivery acknowledgements
Automatic retry if an acknowledgement isn't received
Battery powered and completely standalone

This is mainly a learning project for understanding how the different parts fit together — keypad input, embedded software, SPI/I²C communication, LoRa packets, acknowledgements, and the hardware itself.

The hardware and software are intentionally kept modifiable so the project can be built, changed, and experimented with rather than treated as a finished commercial device.
