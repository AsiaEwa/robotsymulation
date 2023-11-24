# robotsymulation
1. creating a simple simulation in which ready-made elements were placed in the form of boxes, an environment and a robot, and checking basic functions such as moving and copying elements;
![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/3907980c-9955-42dd-8bd7-f2ec50d740d2)

2.Introducing these elements yourself (not ready-made). Step by step definition of Solid~Shape~Sphere constants and variables.

Presentation of changes in the behavior of elements in relation to the environment.
Adding an end to the board in the form of a border made of four cuboids.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/df6212ea-4f6d-484c-b03a-45e7fef1daed)

Changes in graphics rendering, either by changing the light or angle of the image or the colors of the elements themselves, which additionally increases the aesthetic value of the entire project. Additionally, the color of the walls was changed to blue.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/73e94c1d-99f3-4b4c-b96e-1da247123aa0)

Introduction of a general outline of programming robot controllers in the WEBOTS environment with the help of programming in C/C++/Python, etc.
(the concept of creating objects by combining them)

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/93847029-316f-4905-8176-0a02b27847fd)

Creating an element that consisted of two spherical shapes and one cylindrical one, which after appropriate processing (translation and rotation) resulted in a finished element.
Saving specific configurations, for example a shape, so that you can use and modify it at a later stage

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/7390aa44-cb10-40d8-bc9d-621874ca80e8)

Goal: combining several elements into a finished robot in the form of a toy car.
Adding sensors at the front and orienting them appropriately (using rotation) programming the controller for the finished robot.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/69b6284c-66b4-4241-ae64-73c739720f02)

You need to take into account the motors mounted in the wheels as well as the sensors with which the car is equipped.
The work began with preparing the background, for this purpose a background was added and the color was set to "Magenta". Then, in order to create the environment, a floor was added and its dimensions were set (5; 5; 0) on which the robot will operate.

Adding sides to the floor creates a closed board that prevents the robot from falling off the "map".
selecting and uploading the robot from cyberbotics.com/doc/guide/robots

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/7ab13cf9-a120-4181-8f55-6cba1d9eff1a)


The choice of the ALTINO robot was due to the purpose of the study.
In order to check a wide range of parameters, it was decided to perform two tests, the first one was a jump through a hoop and the second one was a test of distance sensors.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/b70fb77e-65e8-4afb-9dce-2f346bd64455)

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/4761aa48-705d-4f06-bb2d-df691afcd0ec)

Creating an environment for testing that is compatible with the robot's work.
In order to check the first problem, it was decided to build two ramps and a ring through which the robot was to jump. It is worth mentioning that the hoop was moved away from the ramp by 1 m. The ramp itself was one meter long and was half a meter away from the controller, which would provide a specific path that would give the robot time to accelerate.

Second test: The first step was to check where the sensors are located in the robot to avoid unpleasant surprises, this was done by entering View~OptionalRendering~ShowDistanceSensor.
preparing a new board with a bridge, which was intended to make it easier to check the given problem. For this purpose, a ramp was created by first adding solid functions, then shape was added in child and the whole thing was rotated and the appropriate angle was set (30o). Then another cuboid element was placed (forming half of the bridge) and the whole thing was copied and rotated to maintain both distances and dimensions. A support was also added in the middle to make the whole thing a bit more realistic. The process of creating map elements is roughly presented below.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/582470ae-f5c0-43d4-9cce-58481362641d)

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/3e49b0e5-b75b-4c64-9a15-faeaa036e88b)

To obtain the rim, the process was as follows. It was added by using the group~solid~shape~cylinder function to add the base of the rim and then adding a second solid~shpae~cylinder body and rotating it 90 degrees relative to the X axis. At this point, to get the rim instead of the "lollipop" it was necessary to subtract the middle part of the rim by negating the Top and Bottom functions, leaving only Side.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/b6373af1-4f25-47cb-9549-ef35c351347a)

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/fdc09e03-8d1d-4138-a2a0-920d70fc1e7a)


The entire map in a top view, which was theoretically supposed to meet
assumptions. Unfortunately, due to internal restrictions on the vehicle's speed, it was not possible to accelerate it to a speed higher than 29.8 [km/h]. Which is presented below.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/8bc40607-bd3e-4bce-907e-a4051cfd806c)

The next planned test was to check the distance sensors, for which the following board was prepared, and two robots were placed opposite each other to check whether the Altinos would pass each other or hit each other.
The robots should "meet" in the middle of the board, i.e. at the "rim".
Writing the code did not go well due to the limitations set by the manufacturer. First of all, limited knowledge of what the next wheel motors are called makes editing or writing code difficult or even impossible.

![image](https://github.com/AsiaEwa/robotsymulation/assets/101841759/1fb837bc-f0bf-49a6-af21-a1dbd2fe26a6)

#### Conclusions:

Unfortunately, due to the lack of knowledge of the names of individual elements (e.g. the names of the motors in the wheels), it was not possible to set all the parameters (as we would like and as it was possible, for example in the example). For this reason, unfortunately, test 1 ended in failure (the robot jumped over the hoop) and the process of starting the robot itself leaves much to be desired. In the second stage, the robots initially drive against each other, but after a while, when they meet on the bridge, the robots first collide and only after a while they pass each other. Which indicates poor configuration.
The process of creating and setting the environment parameters itself was positive.
The disadvantage of this programming environment is the difficulty in creating very complex models (limitation in the selection of shapes, frequent rotation and setting of parameters of smaller solids to obtain the final effect), while the positive aspect is the speed of work and good mapping of simple physical relationships.
This program is perfect for creating simulations that are intended to show the idea of a given work and reflect simple physical interactions as well as the interactions of bodies with each other.
