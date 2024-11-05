---
title: Zones
category: Programming
position: 8
---
# Zones

Your code will probably need to look for different markers depending on the zone your robot starts in.

## Python

`R.zone` will be equal to the the start zone of the robot, and will be equal to one of the teams.

| **Team** | **Code** |
|----------| --- |
| Ruby        | `robot.TEAM.RUBY` |
| Diamond    | `robot.TEAM.DIAMOND` |
| Jade     | `robot.TEAM.JADE` |
| Topaz      | `robot.TEAM.TOPAZ` |
Here's an example:

```python
import robot

R = robot.Robot()

if R.zone == robot.TEAM.RUBY:
    print("Do something!")
else:
    print("Do something else!")
```

## Blockly

You can find the zone block in the **Movement** section.
