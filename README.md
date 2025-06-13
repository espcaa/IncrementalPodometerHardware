# Incremental Podometer Hardware

In this repo, you'll find details about our journey to make a little PCB board that counts steps and keeps you entertained!  
You can take a look at the schematics in the `/pcb` directory or just keep reading this!

**If you want to look at the software of the Incremental Podometer, check out [this repo](https://github.com/theMathR/incremental-podometer/tree/main)**

# Its History

So first, what is the Incremental Podometer?  
It's a podometer! (No waaayyyyy)  
But. With. An. Incremental. Game!!!!!!  
You'll get stats about your physical activity, but you'll stay entertained! Amazing, right?

So we started to brainstorm a bit and came up with a list of essential components:
- A screen (needed to have a UI for the game)
- A microcontroller (with CircuitPython — I don't code in C)
- Some buttons (our first idea was 8 buttons)
- An accelerometer (for counting steps)

With that in mind, we started looking individually at these components:  
First, for the microcontroller, we chose a Pico W because it's cheap, easy to use, and mainly because it has wireless capabilities.  
Second, the screen. We planned to use [the same one as the Sprig](https://www.adafruit.com/product/358). But we quickly realized it wasn't cheap enough, so we finally opted for an [equivalent screen from a German seller](https://www.az-delivery.de/fr/products/1-8-zoll-spi-tft-display?variant=6106727841819).

Our main problem during this project _was the cost of the podometer_. Our first prototype was $30 per board. We planned to make 30 of them, and with $450, at that price, we could only make 15. :/  
We cut costs by not ordering the Picos from JLCPCB (saved $6 via DigiKey!), using a different screen ($4.50 per screen), and soldering all the parts ourselves. I also grouped all the parts we needed assembled by the PCB maker on the same side, because double-sided assembly is SO EXPENSIVE!!!  
We finally opted for an ADXL345 over an ADXL335 because it has I2C, is more power-efficient, and costs $2 less!


## Components list

- Pico W
- ADXL345
- Some [adafruits buttons](https://www.adafruit.com/product/3101l)
- [BH-AAA-B5AA005](https://www.lcsc.com/product-detail/Button-And-Strip-Battery-Connector_MYOUNG-BH-AAA-B5AA005_C2979170.html) (battery holder)
- [1N5817](https://www.lcsc.com/product-detail/Schottky-Barrier-Diodes-SBD_LGE-1N5817_C7544876.html)
- [JS202011SCQN](https://www.lcsc.com/product-detail/Slide-Switches_C-K-JS202011SCQN_C221666.html) (slide switch)
- Some 1uf capacitors

![image](https://github.com/Spectralo/IncrementalPodometerHardware/assets/122629939/8b52cbc5-6c25-48c8-80b6-783f29762f13)
