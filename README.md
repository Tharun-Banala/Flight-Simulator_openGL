**INTRODUCTION

A third-person flight simulator is a kind of simulation game that enables users to control a plane and
experience flying from a third-person viewpoint. The camera in this kind of simulator is positioned
above or behind the aircraft, giving users a wider view of their surroundings and the movements of
the aircraft. The aircraft can be flown by players using a variety of controls, including the throttle,
rudder, and joystick. Third-person flight simulators can represent a wide range of aircraft, from small
planes to commercial airliners and military jets, and can be played on a variety of platforms, including
personal computers and gaming consoles. These simulators can be used for pilot instruction and
aviation research in addition to being frequently employed for entertainment reasons.

**SPECIFICATIONS

**Libraries Required:
1)bits/stdc++.h
2)GL/glut.h
3)glew.h
4)chrono
5)cstdint
6)SFML/Window.hpp
7)glm/gtx/transform.hpp
8)iostream
9)glm/glm.hpp
10)glm/vec3.hpp
11)glm/mat4x4.hpp
12)string
13)fstream
14)functional
15)vector
16)unordered_map
17)map
18)glm/gtc/matrix_tranform.hpp
19)glm/gtx/euler_angles.hpp
20)cmath
21)algorithm
22)numeric
23)glm/vec4.hpp
24)cmath
25)SFML/Window/Mouse.hpp
26) SFML/Window/Event.hpp
27) SFML/Window/Keyboard.hpp
28)utility
29)glm/geometric.hpp
30)glm/gtx/rotate_vector.hpp

How to run the project ?
You need the following versions :
• SFML 2.1+ development headers and library
• C++11 compliant compiler
• CMake 3.11+
• GLEW
Once the above dependencies have been downloaded ,open the source directory and run cmake
$ cd Fly
$ mkdir build
$ cd build
$ cmake .. (if didn’t work then cmake .)
$ make -j4
$ ./Fly

Details of Key Controls:
• W /UpArrow: Elevator Down
• S /DownArrow: Elevator Up
• A /LeftArrow: AntiClock wise Torque
• D /RightArrow: Clockwise Torque
• Space : Thrust Up
• LShift: Thrust Down
• K : Speed Up
• L;Speed Down
• MouseLeftCLick : Camera Angle Rotation
• Mouse Scroll : Scaling

FUNCTIONALITES IMPLEMENTED

• Created 3D model of Aircraft
The entire aircraft is created using vast number of triangles. Each part of the aircraft is
created by joining the large number of triangles. Each segment thus created are joined
to make the whole model. As the model includes large number of triangles, triangles
cannot be seen unless it is zoomed in.

• Assigned movement to the Aircraft
Model has been binded with the position attribute. Each time when there has to be a
movement in the aircraft, we update the position of the aircraft accordingly and render
the new position. Translation and rotation, both are involved in the movement
• Implemented rolling of the Aircraft
Rolling of the aircraft occurs when the keys A or D are pressed. i.e; leftward and
rightward rolling.
Rolling is performed using rotation about longitudinal axis of the aircraft

• Implemented altitude functionality to the Aircraft
Implemented using rotation about latitudinal axis of the plane.
And then translation and then again reverse rotation.
• Implemented Shadowing of the Aircraft
Top view projection of aircraft is displayed on the bottom plane
• Implemented lighting to the model
Whenever the camera angle is changed, the new camera angle is rendered and
shadowed the aircraft accordingly. Like when the plane is seen from bottom angle,
aircraft turnout to be black
• Colored the model using mtl
Using mtl library, the aircraft has been colored. Each part is colored separately
• Implemented crashing of the Aircraft
R

Whenever the co-ordinates of the aircraft and the terrain( which is hit by aircraft) are
matched, then the crashing occurs. And then explosion occurs implemented using
particle emitters.
• Implemented implicit keys for all the functionalities
Created the keys for the key functions using SFML/mouse and SFML/keyword
libraries
• Implemented Accelerator and Decelarator
They have been implemented using general laws of physics. Using the equations of
the motion.
• Camera angles
Camera angles are changed using the position of the mouse cursor. First we check the
left click of the mouse and analyze the change in its co-ordinates and then calculate
the angle of rotation(theta) which is then multiplied by a constant factor to determine
the final angle of rotation.

Output:

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/d9f15c69-48ff-45d2-bb21-0f8e15fafa1a)

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/2042f9ba-2bba-400a-9027-5ff0be761832)

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/51ba4dc4-809a-46df-9639-30b6287d0245)

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/9aef9bc6-1068-4bf1-b561-d0bb4acdcf8d)

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/ce9fab08-ead8-43d6-b31d-e2cf2d555dda)

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/483a3560-1b17-40ff-b0b8-d02be828b1fb)

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/44427ce4-fa0b-4d94-99da-d4384a379a2f)
Shading Effect

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/14d26d0a-5d1d-4d0a-91e8-768522a5faa8)
Top View

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/e6396b96-1e2c-48e6-bdfc-d6802ebe2af4)

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/e37f4bbb-8f6a-4749-9b59-1ad6438cb1f7)
Zoomed out

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/bab27959-2795-4e29-b59b-311f3fa192a6)
Lighting effect

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/e0372c41-c819-46aa-81f7-1771d89e8522)
Reversing the direction of Aricraft

  ![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/71b3598f-0b93-4261-9a14-c81ae3321f88)
Shadow of Airplane

![image](https://github.com/Tharun-Banala/Flight-Simulator_openGL/assets/90239020/ff1b0c58-5f53-484a-9b9c-97ca4ec2b45f)
Crashing of Airplane
