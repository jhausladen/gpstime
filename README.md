# gpstime
Script that sets system time through a GPS

Meant for use with SOC devices that either lack a real time clock or internet connection (such as a raspberry pi), gpstime will work with your GPS through the GPSd (http://gpsd.berlios.de/) utility to access the current time, and will apply that to your system clock.

Usage examples include remote data logging and chartplotters. I use this module to set the time on my raspberry pi which I use as a chartplotter with OpenCPN. In order to ensure that the tide tables are displaying the correct information, the system time must be set correctly.

This script requires the gps python modules included with GPSd to acess the NMEA stream. I have included these modules with the download.

In order to function properly, your GPS must be connected and GPSd must be running (type 'gpsd' in the terminal).

There are far more accurate ways to receive and set time using NTP and PPS. But gpstime has a much lower overhead and is fast to get things going. If you are looking for extreme time accuracy (milliseconds), I recommend looking into NTP/PPS.