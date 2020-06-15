# WiFiSanta

Santa for the internet age

## Hardware

- "Dancing Santa" ornament/toy
- ESP-03 (ESP8266 development board)
- Momentary switch
- 5 pin header (0.1" pitch)
- Toggle switch
- Resistors: 2 x 10k, 1 x 1k

### Block diagram

![](https://github.com/alicraigmile/WiFiSanta/blob/master/wifisanta%20block%20diagram.svg "Block diagram of the required hardware")

### Connections

1. CH_PD connected to Vcc
2. 5 pin headers is connected to ESP-03 (see: https://tewarid.github.io/2016/05/13/getting-started-with-the-esp-03.html)
3. Momentary switch connected between GPIO0 and GND (with a 10k pull-up resistor). 
4. GPIO12 connected to base of transistor via 1k current limiting resistor.
5. Emitter of transistor connected to ground via 10k pulldown resistor.
5. On the dancing santa, locate the toggle on/off switch and connect one side of this to the transistor's collector, and the other to it's emitter.
5. Batteries connected to ESP-O3 Vcc via toggle switch, and GND.

## Software

Download the following code and upload it to the ESP-03:

https://github.com/alicraigmile/WiFiSanta/tree/master/src/WiFiSanta

### Flashing the ESP-03

Connect your FTDI connector to the 5 pin connector.

From Arduino IDE, select the correct board and serial port settings, then upload your code.

NB: Hold down the momentary switch as you connect the power in order to put the ESP-03 intro flashing mode.

### Dependancies

DNSServer, ESP8266WebServer, ESP8266WiFi and WiFiManager libraries are required to get this working.

## Configuration

On first boot, WifiSanta will need to be configured with your Wifi settings.  Conveniently, this can be done by connecting to the WifiSanta Wifi AP and following the prompts.

You may need to manually visit http://192.168.4.1/ during this process.

After setup, you can safely 'forget' the WifiSanta AP and connect to your normal Wifi.

## Usage

Look at your Wifi router logs to find out what IP address has been assigned to WifiSanta. For the remainder of this guide, we'll assume it was given the address 192.168.1.165.

Point your web-browser at this URL to turn Santa on and off:

http://192.168.1.165/santa/toggle

## Acknowledgments

This project is dedicated to the BBC Bitesize development team based in Pacific Quay, Glasgow. Ho ho ho!
