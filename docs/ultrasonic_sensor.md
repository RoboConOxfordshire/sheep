---
title: Ultrasonic Sensors
category: Programming
position: 9
---

# Ultrasonic Sensors

Ultrasonic sensors can be used for calculating the distance from a sensor to the nearest solid object.

They do this through emitting a pulse of ultrasonic sound and recording the time taken for the echo to return.

We can control ultrasonic sensors through all gpio on the Brain Box.


## Python

You can create an ultrasonic sensor through creating an `UltrasonicSensor` object.

The arguments to the initialisation function are first the trigger pin, followed by the echo pin. For example this configures a sensor with trigger on GPIO0 and echo on GPIO1.

```python
sensor = robot.UltrasonicSensor(R.gpio[0], R.gpio[1])
```

We can then read the value of this sensor through calling the read() function which returns a distance in meters.

```python
distance = sensor.read()
```

Here's a complete example:

```python
import robot

R = robot.Robot()

sensor = robot.UltrasonicSensor(R.gpio[0], R.gpio[1])
distance = sensor.read()
```


### I want to use more than one ultrasound sensor but don't have enough GPIO

The BrainBox can support (theoretically) up to 7 ultrasonic sensors. We do this through daisy-chaining the echo pin of one sensor to the trigger pin of another.

For example for two sensors, sensor A has trigger pin GPIO0, and echo GPIO1, and sensor B has trigger pin GPIO1 and echo GPIO2.

You can create an ultrasonic sensor combining these two physical sensors, by listing the echo pins in order.

```python
sensors = robot.UltrasonicSensor(R.gpio[0], R.gpio[1], R.gpio[2])
```

:::warning

If the echo pins are listed in the wrong order incorrect values may be returned

:::


## Blockly

The use of ultrasonic sensors in blockly is currently unsupported.