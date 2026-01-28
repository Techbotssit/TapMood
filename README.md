Touch-Controlled Emoji Display (Arduino + OLED)

This project implements a touch-controlled animated emoji display using an Arduino-compatible board and a SH1106 / SSD1306 SPI OLED display.
A capacitive touch sensor is used to cycle through different emojis, which are displayed with a smooth slide-in animation and positioned precisely on the OLED screen.

The project demonstrates bitmap rendering, scaling, animation, and touch input handling on resource-constrained microcontrollers.

Features:
*Touch-based emoji switching
*Smooth slide-in animation (Right → Position)
*Scaled bitmap emoji rendering
*Flicker-free OLED updates
*Simple debounce handling for touch input
*Modular and easy-to-extend emoji system

Hardware Required

Arduino-compatible board (UNO / ESP8266 / ESP32 – SPI capable)

SH1106 or SSD1306 OLED Display (SPI, 128×64)

Capacitive Touch Sensor (Digital output)

Jumper wires

Pin Connections
OLED (SPI)

VCC → 5V

GND → GND

SCK → D13

MOSI → D11

CS → D8

DC → D4

RST → D3

Touch Sensor

OUT → D2

VCC →5V 

GND → GND

How It Works

Emojis are stored as 16×8 monochrome bitmaps in program memory (PROGMEM)

Each pixel is scaled up using a software scaling function

Touch input advances to the next emoji

New emoji slides in from the right side of the OLED

Final position is calculated dynamically to maintain alignment

User Interaction

Power on the board

The first emoji is displayed on the OLED

Touch the sensor to:

Advance to the next emoji

Trigger the slide animation

The emoji remains displayed until the next touch

Software Architecture

Bitmap rendering using Adafruit_GFX

SPI OLED control using Adafruit_SH110X

Program-memory optimized emoji storage

Non-blocking touch debounce logic

Modular functions for:

Static drawing

Scaled bitmap rendering

Slide animation

Libraries Used

Adafruit GFX Library

Adafruit SH110X Library

SPI (built-in Arduino library)

Install all required libraries via Arduino Library Manager.

Customization

Add more emojis by defining new bitmap arrays

Change emoji size using the scale variable

Modify animation speed by adjusting delay and step size

Reposition emoji by changing alignment calculations

Known Notes

OLED alignment depends on bitmap size and scaling factor

Touch sensor output may be HIGH or LOW depending on module

Avoid using blocking delays in future expansions

Future Improvements

Emoji selection menu

Long-press gesture detection

Multiple animation styles

Battery-powered portable version

I2C OLED support

License

This project is open-source and free to use for learning, experimentation, and personal projects.
