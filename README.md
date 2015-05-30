ATX Breakout Board
=================

Eagle files for my ATX Breakout Board (v1, with USB support using a TPS2513 and voltage control with a LM317). Based on the Dangerous Prototypes' idea.

## New version (v1.2) ##

<p align="center">
  <a href="image.png"><img src="https://github.com/ftruzzi/ATX-Breakout-Mini/blob/master/image.png" align="center" height="595"   width="609" ></a>
</p>

Just finished updating the board. BOM updates and post blogs will follow. I'm also printing a second batch (20-30 PCBs) soon.

Changes and additions:

*   Thickened many traces, **removed pin header** in the middle of the board and **added one behind each binding post** (up to 5 output pins per voltage line, with no risk of burning any traces).
*   **Added resistors to the USB ports.** You may want to use them for USB identification, as they are cheaper and easier to find than the TPS2513. Adafruit link for more info: https://learn.adafruit.com/minty-boost/icharging
*   Moved LM317 so that you can mount it horizontally + used a footprint with longpads, should you want to solder wires to an external voltage reg + heatsink.
*   **Prototyping area added** at the top left of the board. Not sure if it will ever come useful, but I had some empty space there. You have easy access to the 3V3 and 5V lines.
*   Moved/rearranged several parts (pot, switch, LEDs) in order to draw shorter and cleaner traces.


##Features

*   **24-pin ATX** connector.
*   Voltage lines are all broken out individually on **binding posts**.
*   **LM317-based voltage regulator**. Using a 300 ohm resistor and a 2K ohm potentiometer, voltage range is 1.25-9V.
*   **2 USB ports **based on the TPS2513 from Texas Instruments. They can automatically detect what device is connected and adjust resistance on D+ and D- lines as needed. This means **full compatibility and maximum charging speed on both Apple and Android devices**. One of them is connected to 5v_STDBY, so that it works even when the PSU is off.
*   Pretty much everything can be **fused**. I left -12V out because it can only carry low amounts of current on most PSUs (mine is 500mA maximum).
*   **Breadboard pin headers** so that voltage lines can be connected to a breadboard using jumper cables.
*   **Voltmeter** headers in order to know the LM317 output voltage.
*   There is room for a **9W power resistor** is your PSU needs it to stabilize output voltages. You can connect it either to the 5v rail or to the 12v one by jumpering the corresponding pads.
*   **Status LEDs** on fused lines and USBs so you can check if everything works fine.
*   Screw holes for standoffs.


More details and pictures on my blog: http://b.truzzi.me/building-a-better-breakout-board-for-atx-psus-2

Suggestions and feedback are very welcome!
