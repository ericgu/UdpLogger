# UdpLogger

A simple logger for ESP8266 projects to log status/debug information over UDP. 

# Why?

When developing and debugging a ESP8266, it's very useful to write logging messages out over the Serial port so they can be viewed on the computer.

But after the project is installed, this capability is lost, which makes debugging in the field harder. 

UdpLogger is a very simple replacement; it will send whatever messages you would like into the local network using the UDP protocol. These messages can then be easily viewed from a host computer.

# Viewers

Any program that can view UDP messages will work. Wireshark is a common one.

If you want a simple (very simple) one, see https://github.com/ericgu/UdpMonitor

