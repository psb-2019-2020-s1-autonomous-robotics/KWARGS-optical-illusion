# KWARGS-optical-illusion

[Our](https://www.google.com/search?q=our&safe=active&rlz=1C1GCEU_enUS868US868&source=lnms&tbm=isch&sa=X&ved=0ahUKEwjMh43Y69XlAhUFmuAKHeGDCe4Q_AUIEygC&biw=1920&bih=969#imgrc=8OU-zKEIiOTmxM:) [project](https://www.google.com/search?q=project&safe=active&rlz=1C1GCEU_enUS868US868&source=lnms&tbm=isch&sa=X&ved=0ahUKEwjYnpLq69XlAhXEmuAKHfVJCucQ_AUIEigB#imgrc=hbjj3rhBJY76qM:) [is to be used by the](https://www.google.com/search?q=happy+cat&safe=active&rlz=1C1GCEU_enUS868US868&source=lnms&tbm=isch&sa=X&ved=0ahUKEwj34fSD7NXlAhWiTN8KHUk5DDAQ_AUIEigB&biw=1920&bih=969#imgrc=65g_eySYE0ziNM:) [confused](https://www.youtube.com/watch?v=U7X7cEh5au8) [of our population.](https://www.google.com/search?q=world+population&rlz=1C1GCEU_enUS868US868&oq=world+population&aqs=chrome..69i57j0l5.3263j1j9&sourceid=chrome&ie=UTF-8) [Basically,](https://www.google.com/search?q=basic+white+girl&safe=active&rlz=1C1GCEU_enUS868US868&source=lnms&tbm=isch&sa=X&ved=0ahUKEwjs-_uu7NXlAhXCnuAKHZImA8EQ_AUIEigB&biw=1920&bih=969#imgrc=qEbL6brJ_fUlkM:) [it just adds to everyone's](https://www.google.com/search?q=math&safe=active&rlz=1C1GCEU_enUS868US868&source=lnms&tbm=isch&sa=X&ved=0ahUKEwiQ6f6i7NXlAhUDhOAKHW6QBT8Q_AUIEigB&biw=1920&bih=969#imgrc=cnowjAsXD5FHcM:) [confusion](https://www.google.com/search?q=confusion).

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
