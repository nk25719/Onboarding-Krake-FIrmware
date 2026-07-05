**Subject:** Help Us Help You: Define Your Exact Hardware, Learn Multitasking, Advice for Beginners

## Your Embedded Hardware

You are developing firmware to run on hardware. What is your hardware?  
Please identify your exact Arduino or ESP development board. Provide a link to the exact board you purchased and, if possible, the schematic for that exact board. You must have the correct schematic.

For example:

> I have a HiLetgo ESP-WROOM-32 ESP32 ESP-32S WiFi + Bluetooth development board.  
> Product link: http://www.hiletgo.com/ProductDetail/1906566.html

I found its schematic through the Amazon listing, since I could not find it on the manufacturer’s site:

> https://www.amazon.com/HiLetgo-ESP-WROOM-32-Development-Microcontroller-Integrated/dp/B0718T232Z

You also need the manuals and datasheets for the ESP32. There is more than one, so download the relevant material here:

> https://docs.espressif.com/projects/esp-idf/en/latest/esp32/hw-reference/index.html

This can feel overwhelming at first, so start by looking at the table of contents.

Also identify the exact part numbers of the other components you are using, and provide links to their datasheets. You need to do this work for every part.

For example, for an LED:

> Kingbright Green 568nm LED Indication - Discrete 2.2V Radial  
> Vendor link: https://www.digikey.com/en/products/detail/kingbright/WP7113SGD/1957822

The datasheet is available there.

## Test Equipment

Tell us what test equipment you have.

You really should have a digital multimeter and learn how to use it well. Even better, have two or three.

For example, here is one I use:

> AstroAI DM6000AR  
> https://www.astroai.com/digital-multimeter-6000-counts-dm6000ar/ap/100019

It also helps a lot to have an oscilloscope.

You can start very simply by using an Arduino Uno in this way:

> https://www.youtube.com/watch?v=uYnaEBqN0Z4

That was very limited example. It had no control for sampel rate and was only one channel. But it did demonstrate the serial plotter.
Note this example used the Arduino IDE version 1 with a plot size of 500 points. Version 2 of the IDE has a 50 point plotter. Use a search or AI with the following qustion, "how to change the Arduino IDE version two serial plotter for 500 data points" for a fix.

Here is a more elaborate multi channel Arduino Serial Plotter using the legeond feature of the Serial Plotter. Again this example was written for the Arduino IDE version 1 plotter.
>  https://github.com/ForrestErickson/SerialPloterA0A1A2A3A4A5

Here is a very elaborate Arduino oscilloscope project with measurements and a tutorial. It uses a Processing (Jave) sketch for display of the waveforms.

> https://www.instructables.com/Oscilloscope-Arduino-Processing/

Need a function generator? Again, an Arduino Uno can help there too.
_(NEED SOME EXAMPLES HERE)_

What kind of power supplies do you have?

For example, I have:

> Wall supply, 9V at 200 mA  
> https://www.amazon.com/200mA-Adapter-Power-Supply-Charger/dp/B07DR7SV15

You should also have plenty of solderless breadboards and jumper wires.

## Good Beginner Resources

A good beginner website, including a PDF book:

> http://www.introtoarduino.com/

And:

> https://randomnerdtutorials.com/download/

Each of these includes lists of required parts.

## Bottom Line

In addition to several ESP boards, get about five Arduino Uno boards and get started.

For learning, focus on the ESP32. Do not bother learning the more limited ESP8266 unless you plan to build thousands of units and need to reduce cost.

## A Good ESP32 Resource for WiFi

I spent less than $30 on a Random Nerd Tutorials PDF book and found it very useful for learning to program these boards:

> https://randomnerdtutorials.com/build-web-servers-esp32-esp8266-ebook/

To get inspired, watch some of the Random Nerd Tutorials videos.

Make things.

## Real-Time Programming and Multitasking

Learn to program in a multitasking style.

The best reference I have found for writing multitasking code and getting rid of `delay()` is this three-part series, starting here:

> https://learn.adafruit.com/multi-tasking-the-arduino-part-1

Unfortunately, it is not written as a library, but rather as classes in the main file. That is a longer discussion and not ideal for beginners.

This example is written in a different style and explains why and how to use interrupts:

> https://circuitdigest.com/microcontroller-projects/esp32-timers-and-timer-interrupts

---

## KiCad Tutorials

The best KiCad tutorials I have found so far:

### First
For a mostly complete overview of a very simple schematic and PCB, including the symbol and footprint editors, start here:

> Robert Feranec — *What is KiCad about? Starting with KiCad...*  
> https://youtu.be/maaBkw7IRUc

This tutorial is for KiCad version 5, but it is still very good as a starting point.

### Second
For KiCad version 7.0, here is a much longer but well-done tutorial that covers a complete schematic and an abbreviated PCB project for an ESP32 design:

> Morten — *KiCad 7 ESP32 PCB Design Full Tutorial*  
> https://youtu.be/b-7bMl6fJio?si=NmS-i1ScGdcC0x-T&sfnsn=mo

I found it understandable even at 2× speed.

### Third
For hierarchical schematics, this is still the best tutorial I found:

> John’s Basement on KiCad 5 #17 — *Hierarchical Labels & Pins*  
> https://youtu.be/m_HTBurAJn4

This is for version 5, but the concepts still apply. Hierarchical, multi-page schematics are essential for complex designs.

### Fourth
For a much more elaborate project:

> Phil’s Lab #65 — *KiCad 6 STM32 PCB Design Full Tutorial*  
> https://youtu.be/aVUqaB0IMh4

Phil’s schematics and PCB layouts are attractive and electrically well thought out.

Also see the “BananaSchplit” design here:

> https://www.eevblog.com/forum/beginners/split-powersupply-(banana-schplit)-issues-with-negative-12v-rail/

## Design Review

To understand the many requirements that must be kept in mind when creating a schematic or PCB design, I encourage you to read this design review guide:

> https://resources.altium.com/p/pcb-design-and-review-checklist

Although it is written for Altium users, the requirements it identifies are largely the same for any good schematic and PCB design, regardless of software.

It will probably introduce you to many useful requirements worth learning.

## Fabricator Requirements

If you plan to fabricate PCBs or assemblies through a vendor such as JLCPCB, you need to read and understand the fabricator’s requirements:

> https://jlcpcb.com/capabilities/pcb-capabilities

## Getting Help

Finally, help us help you. Do not make us guess.

Share the exact file with the problem. Share your entire project, or a simplified version that reproduces the exact problem.

## Markdown and Document Viewing Tools

If you want to create images inside tables or work with documentation, these tools may help:

Notepad++ supports syntax highlighting for Markdown files with the `.md` extension:

> https://notepad-plus-plus.org/downloads/

For viewing locally edited Markdown files in Chrome:

> https://chrome.google.com/webstore/detail/markdown-viewer/ckkdlimhmcjmikdlpkmbgfkaikojcbjk

---

## USB Signal Measurements and Routing

This video discusses USB signal measurements, routing, and a KiCad feature:

> https://youtu.be/bkgdTBaORUw?si=k3yFN82HrQvH1ypU

It includes a lot of vocabulary related to high-speed signals that I have not introduced yet, but it gives you an idea of how much there is to learn.

However, the main takeaway is this:

For the very short USB traces in Krake, and since we are only using USB 2.0 signal speeds, it should work.

I hesitate to even show this, but here is another video about a KiCad feature we have not used because it is not necessary for the short trace lengths we are using:

> https://youtu.be/Itsrdc8tX7M?si=FgkSUxgF6YglOME_

We should not slow down our work to learn this feature right now.

---

## MQTT Learning Resources

Viewing premade templates can help you see how others put documents together.

Here are some notes on learning MQTT from HiveMQ.

For their future professional development, all Krake team members doing firmware development need to become fully familiar with all MQTT features.

### Introduction to MQTT
> https://www.hivemq.com/info/mqtt-essentials/#essential-guide

### MQTT Topics and Wildcards
> https://www.hivemq.com/blog/mqtt-essentials-part-5-mqtt-topics-best-practices/

### Important MQTT Features to Understand
- Last Will and Testament
- Retained messages
- Quality of Service (QoS)

---

## LaTeX Learning Resources

Below are some resources I used to learn LaTeX.

The forums on this site are very useful. Search for the issue you are having:

> https://tex.stackexchange.com/questions

For Overleaf in particular, the guides on its website are also very helpful:

> https://www.overleaf.com/learn/how-to/How_do_I_use_Overleaf%3F

There are also many useful resources and videos on YouTube. For example:

> https://www.youtube.com/watch?v=xcTN4F3l9Ds

---

## Krake-Related Onboarding and Learning Path

“There is no royal road.”

Go through this process:

1. Get the example **Blink** sketch, compile it, and load it onto the target.  
   The target can be an Uno or an ESP32.

2. Put under **Version Control**. Using git, as soon as you verify that `LED_BUILTIN` is blinking, put that code under version control and make the initial commit.

3. Clean up the Blink code by **removing magic numbers**. Create descriptive constants for things like GPIO pin numbers and baud rate. Commit those changes.

4. Add a **serial splash** screen, for example:

```cpp
void serialSplash() {
  Serial.println();
  Serial.println(F("======== " __FILE_NAME__ " " VERSION "========"));    
  Serial.println(MODEL_NAME);
  Serial.println(ESP.getChipModel()); // Prints "ESP32-S3", etc.
  Serial.print(F("Compiler: "));
  Serial.println(__cplusplus);
  Serial.print(F("Compiled at: "));
  Serial.println(F(__DATE__ " " __TIME__));
  Serial.println(LICENSE);
  Serial.println(F("==================================================="));
  Serial.println();
}
```

### Some required and optional defines

```cpp
#define VERSION "V0.0.2 "
#define MODEL_NAME "Model: HW2_Multitasking"
#define DEVICE_UNDER_TEST "SN: 00001"
#define LICENSE "GNU Affero General Public License, version 3 "
#define ORIGIN "LB"

#define BAUDRATE 115200

#define BOOT_BUTTON 0
const int LED_BUILTIN = 2;
```

Always include the program version and compile date/time, and sometimes also the hardware target, author name, and license. Then commit the changes with a descriptive message.

5. **Make Multitasking**. Refer to the multitasking article. Apply the second article by removing `delay()` and replacing it with `millis()`. Make a descriptive commit.

6. **WiFi Credentials** For ESP32:  
   Install WiFi Manager and follow the Random Nerd Tutorials guide. Make a descriptive commit.

7. **Over The Air** update. Install ElegantOTA and a filesystem, again following Random Nerd Tutorials. Make a descriptive commit.

8. If you have multiple ESP32 boards, customize the access point name using the MAC address. Make a descriptive commit.

9. Use the boot button for user input. This is a good time to introduce the Daily Struggle library examples. Report the different button press types to the serial monitor.

10. Use the flasher class from the multitasking article to change the blink rate of `LED_BUILTIN`.

### Example use case
- Long press returns the LED blink rate to default
- Two quick presses speed up the blink rate
- Three quick presses turn the LED off
- Four quick presses turn the LED back on

Make a descriptive commit.

11. Install the WebSockets library and serve a webpage. Add:
- a control for the LED
- an indicator for the LED
- an indicator for the microcontroller temperature using `temperatureRead()`

12. Add authentication and authorization:
- An **Administrator** can change the LED blink rate, view LED status, and see the temperature
- A **Viewer** can only view the blink rate, LED status, and temperature

Reference:
> https://share.google/aimode/RUgmEVkFHLmJ3OcD3

It will be very helpful if you become fluent with WiFi Manager and OTA.

I advise working through every single example from those libraries on an ESP32 kit.

Please purchase, or have Robert purchase, the ESP32 **ESP32-DEVKIT1** with controller part number:

> **ESP32-WROOM-32E-N4**

This will provide compatible development hardware.

A minimal human interface using the built-in LED and the boot button can already let you develop useful tests.

## Next Step After MQTT Basics

Once you understand MQTT publish and subscribe thoroughly, then it is time to learn how to host MQTT brokers.

Public Invention Krake project members need to know how to use and host brokers that are **not** the demo broker currently hardcoded into GPAD_API.

Some brokers should be hosted on the public internet.

Some brokers should be LAN-only, and Public Invention should be able to demonstrate how to host them.

The host hardware could be:
- another ESP32
- another single-board computer
- even a Windows computer
