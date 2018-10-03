# UdpLogger

A simple logger for ESP8266 projects to log status/debug information over UDP. 

# Why?

When developing and debugging a ESP8266, it's very useful to write logging messages out over the Serial port so they can be viewed on the computer.

But after the project is installed, this capability is lost, which makes debugging in the field harder. 

UdpLogger is a very simple replacement; it will send whatever messages you would like into the local network using the UDP protocol. These messages can then be easily viewed from a host computer.

# Operation

UdpLogger sends broadcast UDP messages; that means that they go to all of the nodes on the local network. That means you don't have to define the IP address of the node that will be receiving the messages. 

When calling init(), you can pass both the port and a "message prefix" string; the message prefix string will be written at the start of every message so that the receiver can have more information about who sent the message. 

# Example

#include "UdpLogger.h"

UdpLogger.init(12345, "LandscapeController: ");  // Do this in setup...

UdpLogger.println("Here is my message");

# Viewers

Any program that can view UDP messages will work. Wireshark is a common one.

If you want a simple (very simple) one, see https://github.com/ericgu/UdpMonitor

