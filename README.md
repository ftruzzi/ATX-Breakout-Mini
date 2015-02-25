ATX Breakout Board
=================

Eagle files for my ATX Breakout Board (v1, with USB support using a TPS2513 and voltage control with a LM317). Based on the Dangerous Prototypes' idea.

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
*   **NEW**: resistors added to the USB ports. You may want to use them for USB identification, as they are cheaper and easier to find than the TPS2513. Adafruit link for more info: https://learn.adafruit.com/minty-boost/icharging


More details and pictures on my blog: http://b.truzzi.me/building-a-better-breakout-board-for-atx-psus-2

Suggestions and feedback are very welcome!
