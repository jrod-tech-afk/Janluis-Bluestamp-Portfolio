# Pulse Sensor
I have made a pulse sensor using the arduino, a sensor, and an LCD screen. My project is able to display your heartrate through the LCD screen if you put your finger on the sensor. I have modified it by adding a beeping noise that matches with the pulse rate

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Janluis R | KIPP NYC College Prep | Computer Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
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
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

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
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
