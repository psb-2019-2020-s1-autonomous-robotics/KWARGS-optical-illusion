# KWARGS-optical-illusion

Our project is to be used by the [confused](https://www.youtube.com/watch?v=U7X7cEh5au8) of our population. Basically, it just adds to everyone's [confusion](https://www.google.com/search?q=confusion).

Our Code:
```
#!/usr/bin/env pybricks-micropython

from pybricks import ev3brick as brick
from pybricks.ev3devices import (Motor, TouchSensor, ColorSensor,
                                 InfraredSensor, UltrasonicSensor, GyroSensor)
from pybricks.parameters import (Port, Stop, Direction, Button, Color,
                                 SoundFile, ImageFile, Align)
from pybricks.tools import print, wait, StopWatch
from pybricks.robotics import DriveBase

#kwargs
# Write your program here
kwarg = UltrasonicSensor(Port.S1)
mototsa = Motor(Port.A)
mototorb = Motor(Port.B)
#i dont think these have any significance but it didnt work without them soooooooooooooo
wheel_diameter = 56
axle_track = 114
robot = DriveBase (mototsa, mototorb, wheel_diameter, axle_track)
while True:
    if kwarg.distance() < 1000:
        robot.drive(200,0)
        wait(1000)
        #mototsa.run_target(500,3600)
        #mototorb.run_target(500,-3600)
    else:
        robot.stop()
```
