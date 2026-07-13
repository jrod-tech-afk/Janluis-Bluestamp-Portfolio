# Pulse Sensor
I have made a pulse sensor using the arduino, a small ambient light photosensor, and an I2C LCD screen which are both connected to the arduino via its I2C pins. My project is able to display your heartrate through the LCD screen if you put your finger on the sensor, which I was able to achieve through coding it in the arduino in order for it to input my BPM and output it throughh the LCD screen.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Janluis R | KIPP NYC College Prep | Computer Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](https://images.openai.com/static-rsc-4/4ETYzXp-AUNUHz89ztndnw7IjdW0455alfZaRVzCQocTNUy_72DidtLhmRs1HApy1O6MrlZsctkKtUyj5Jjx_GRgmkL_kQfzM8GhTFjRX2eH5mRlZsfJpnBhSIju1jriLQlgdOyu-_z6WdBC98STqYjrMXzSGA50XawZqNMvC5--8hXDRt7YLuQBqP3hPzaT?purpose=fullsize)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

- Finalized project, finished portfolio, I am ready to present
- My biggest challenges were learning to use the softwares like github and arduino
- I learned how to implement my hardware into my pc in order to make it work with the software
- I hope to continue using computer hardware and software

# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

- Modded my pulse sensor. Now I have a working sound system that matches the pulse rate with a 'beep' noise
- I was surprised on how much the arduino can do with just a few wires and being plugged in to my PC
- The faulty parts were an easy fix, BSE just sent me replacements
- I need to now complete my portfolio by adding pictures, videos, and the schematic. 

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

- The arduino is the heart of the whole project, it connects to a sensor and an lcd screen to display the pulse rate
- I have connected all of the wires to the arduino 
- I am having trouble with parts, the sensor doesn't come with the wires attatched and so does the LCD screen, so I had replacements sent to me in order to make it work
- I just want to get the base project working first, then I will worry about the modifications in my next milestone

# Schematics 
![Schematic Image](https://images.openai.com/static-rsc-4/4ETYzXp-AUNUHz89ztndnw7IjdW0455alfZaRVzCQocTNUy_72DidtLhmRs1HApy1O6MrlZsctkKtUyj5Jjx_GRgmkL_kQfzM8GhTFjRX2eH5mRlZsfJpnBhSIju1jriLQlgdOyu-_z6WdBC98STqYjrMXzSGA50XawZqNMvC5--8hXDRt7YLuQBqP3hPzaT?purpose=fullsize)

# Code 

```c++
// Include necessary libraries
#define USE_ARDUINO_INTERRUPTS true
#include <PulseSensorPlayground.h>
#include <LiquidCrystal_I2C.h>
LiquidCrystal_I2C  lcd(0x27, 16, 2); // set the LCD address to 0x27 for a 16 chars and 2 line display
 
 
// Constants
const int PULSE_SENSOR_PIN = 0;  // Analog PIN where the PulseSensor is connected
const int LED_PIN = 13;          // On-board LED PIN
const int THRESHOLD = 550;       // Threshold for detecting a heartbeat
 
// Create PulseSensorPlayground object
PulseSensorPlayground pulseSensor;
 
void setup()
{
  // Initialize Serial Monitor
  Serial.begin(9600);
  lcd.init();
  lcd.backlight();
 
  // Configure PulseSensor
  pulseSensor.analogInput(PULSE_SENSOR_PIN);
  pulseSensor.blinkOnPulse(LED_PIN);
  pulseSensor.setThreshold(THRESHOLD);
 
  // Check if PulseSensor is initialized
  if (pulseSensor.begin())
  {
    Serial.println("PulseSensor object created successfully!");
  }
}
 
void loop()
{
  lcd.setCursor(0, 0);
  lcd.print("Heart Rate");
  
  // Get the current Beats Per Minute (BPM)
  int currentBPM = pulseSensor.getBeatsPerMinute();
 
  // Check if a heartbeat is detected
  if (pulseSensor.sawStartOfBeat())
  {
    Serial.println("♥ A HeartBeat Happened!");
    Serial.print("BPM: ");
    Serial.println(currentBPM);
 
    lcd.clear();
    lcd.setCursor(0, 1);
    lcd.print("BPM: ");
    lcd.print(currentBPM);
  }
 
  // Add a small delay to reduce CPU usage
  delay(20);
}
```

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino UNO Board | Software and Hardware setup | $25 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Pulse Sensor | Sense the pulse from your finger and feed it through the arduino | $17 | <a href="https://amzn.to/45W4blY"> Link </a> |
| 16X2 I2C LCD Display | Display Pulse Rate | $10 | <a href="https://amzn.to/3UDntGw"> Link </a> |
| Jumper Wires | Connects everything together | $7 | <a href="https://amzn.to/3F8fLhW"> Link </a> |
| Breadboard | Prototypes Electric Circuits | $8 | <a href="https://amzn.to/3Bg68wE"> Link </a> |
| Name | Description | $price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
- [Resource 1](https://how2electronics.com/pulse-rate-bpm-monitor-arduino-pulse-sensor/)
- [Resource 2](https://chatgpt.com/c/6a44250c-60f0-83ea-bedf-9c5fe65b8f04?mweb_fallback=1)
- [Example 1](https://drive.google.com/file/d/1GIGxyskToY8Ep137GnfTcfMCH4LaB6MF/view?pli=1)
