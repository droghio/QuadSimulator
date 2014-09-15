QuadSimulator
=============

***A blender powered simulator for trying out quadcopter stabilzation algorithms.***


###PREREQUISITES

You'll need blender, grab a copy here <a href="http://www.blender.org/">blender</a>. If you are not familiar with blender I would highly suggest looking online for some tutorials.


###RUNNING
  Press the "p" key.


###CONFIGURATION

After grabbing the repo double click the .blend file, it should automatically load in blender.

It will dump you in blender's game logic view.
Most people won't have to do too much here but in the bottom right you can set the max thrust each propellor can output (units are Newtons) and specify inital RPMs for each motor.

By default max rpm is 10,000 and counter clockwise rotations are negative.

If you want click on the code view on the right and follow the commented instructions to make the simulated quadcopter match your own.
I would suggest not messing with the inital values until you have a good idea of what the software is doing.

Once you are ready scroll to the stabilzationTick function and replace it with whatever code you want.

Right now it is set for a simple derivative control.

The accel parameter holds a list of the x, y, and z accelerations calcualted from the last tick.
The function must return the RPMs for each motor, remember couterclockwise rotations must be negtaive, all units are SI.




###DETAILS

Right now the program does not really look for directional input (ie "go forward, turn left, move up") but that'll change shortly.
For now can press the w or e keys to launch either of the front fans to max rpm.

The simulator does not take into account pressure changes or any aerodynamics. It uses simple angular and linear inertial physics calculations to simulate the quadcopter.

You can refine the simulation by specifing thrust curves or adding force fields but the stock code should do for most situations.

One again all units are in SI that means kg, meters, and yes radians. Trust me it's for the best.

Happy flying!
