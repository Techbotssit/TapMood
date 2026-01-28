TapMood is a simple, interactive emoji display project built using NodeMCU (ESP8266) and an SH1106 SPI OLED display.
A touch sensor is used to cycle through different facial expressions (emojis), making the display react instantly to user interaction.

This project demonstrates bitmap rendering, scaling, animation, and touch input handling on a monochrome OLED screen.

**Features:**

Touch-based emoji switching

Smooth slide-in animation (Right → Position)

Scaled bitmap emoji rendering

Flicker-free OLED updates

Simple debounce handling for touch input

Modular and easy-to-extend emoji system



**User Interface:**

OLED Display:
SH1106 128×64 SPI OLED used to display emojis

Touch Control:
Single touch input cycles through different emoji states

**Hardware Required:**

NodeMCU (ESP8266)

SH1106 OLED Display (SPI, 128×64)

Touch Sensor Module

Jumper Wires



**How to Use:**

Power on the NodeMCU

OLED displays the initial emoji

Touch the sensor to change the emoji

Each touch triggers a slide animation

Emoji stays visible until the next touch



**Software Architecture:**

Bitmap-based emoji rendering

Manual pixel scaling for large emojis

Non-blocking touch detection

Debounce logic using millis()

No dynamic memory allocation

Optimized for stable OLED refresh



**Libraries Used:**

Adafruit SH110X

Adafruit GFX

SPI (built-in)

Install all libraries via Arduino Library Manager.


**Important Notes:**

Ensure correct SPI wiring for SH1106 displays

Use a safe GPIO pin for the touch sensor (D2 recommended)

Avoid using SPI pins for touch input


**License**

This project is open-source and free to use for educational and personal projects.
