# WiFiSanta

Santa for the internet age

## Hardware

- "Dancing Santa" ornament/toy (modified)
- ESP-03 (ESP8266 development board)
- Push switch (push on boot to program via the ftdi)
- 5 pin connector (ftdi for serial monitoring and programming)
- pin connector (to connect to modified "Dancing Santa" toy)
- pin connector (power in)
- Toggle switch (power on/off)
- 10k pulldown resistor
- 1k current limiting resistor

### Connections

# Software

Download the following code and upload it to the ESP-03:

https://github.com/alicraigmile/WiFiSanta/tree/master/src/WiFiSanta

## Dependancies

DNSServer, ESP8266WebServer, ESP8266WiFi and WiFiManager libraries are required to get this working.

# Configuration

On first boot, WifiSanta will need to be configured with your Wifi settings.  Conveniently, this can be done by connecting to the WifiSanta Wifi AP and following the prompts.

You may need to manually visit http://192.168.4.1/ during this process.

After setup, you can safely 'forget' the WifiSanta AP and connect to your normal Wifi.

# Usage

Look at your Wifi router logs to find out what IP address has been assigned to WifiSanta. For the remainder of this guide, we'll assume it was given the address 192.168.1.165.

Point your web-browser at this URL to turn Santa on and off:

http://192.168.1.165/santa/toggle

# Acknowledgments

This project is dedicated to the BBC Bitesize development team based in Pacific Quay, Glasgow. Ho ho ho!
