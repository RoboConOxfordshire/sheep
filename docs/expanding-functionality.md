---
title: Expanding Functionality
category: Hardware
position: 5
---
# Expanding Functionality

## USB

You can use USB devices using the [`serial`](https://pyserial.readthedocs.io/en/latest/shortintro.html) library. The connection will probably open on something similar to `dev/ttyUSB0` but if you can't find it where you expect then connect the device to a Raspberry Pi running a recent OS image and observe where it appears. However during the competition **RoboCon** will need access to one USB port, so if you want to use the USB port you'll have to use a USB hub.
