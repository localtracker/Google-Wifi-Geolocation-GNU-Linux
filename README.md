# Wifi Geolocation through Google Maps
##### // dev: localtracker

Script written in python to determine your current GPS co-ordinates through the nearby wireless access points. 

The Google maps API helps you locate yourself by passing a list of nearby access points to the API. The signal strength plays an important role in this. The GPS co-ordinates and the accuracy of the positioning depends on how far/close you are located from these access points. The signal strength, MAC address and SSID being broadcasted can be viewed when you run the script. Very soon you will understand how this works and be able to come up with creative ways to find someone else's position, instead of yours. You might want to query multiple times and take an average.

## Requirements

Two things to function properly.

	1. Python 2.x (https://www.python.org/downloads/)
```
doh!
```
	2. Scapy (http://www.secdev.org/projects/scapy/) - For parsing wireless frames
```
pip install scapy
``` 
## Usage

Bring up a monitor interface.

```
airmon-ng start wlan1
```
If running the script for the first time, you will have to change permissions. Navigate to cloned directory and run-

```
chmod a+x gglocate
```
#### Results

```
./gglocate

Enter your monitor interface (ex: mon0): mon0
[*] Found: 02:aa:2c:gg:tt:hh -- broadcasting -- WiFiX -- signal strength -- -71
[*] Found: 9c:bb:26:ff:rs:ii -- broadcasting -- CA07E -- signal strength -- -75
[*] Found: 20:cc:c8:ee:qq:jj -- broadcasting -- 304-2M -- signal strength -- -75
[*] Found: 12:dd:2c:dd:pp:kk -- broadcasting -- Wifi2M-B -- signal strength -- -71

Your Location (as per google maps api):
Latitude: 43.8472031
Longitude: -2.8745418
Accuracy: Within 27 mts

```
Tested on kali linux, linux mint and ubuntu.
