## Project Index <a name="projectlist"></a>
1. **Python API to automate belt drive design** [read more](#projecta)

2. **Data logging API for Drone test rig** [read more](#projectb)<br />

3. **Damping characteristics visualisation using Excel** [read more](#projectc) <br />

4. **Vehicle flat ride curve for different configurations - Gross and half load** [read more](#projectd) <br />

5. **H-I-X Quadcopter frame design fabrication and flight** [read more](#projecte) <br />

6. **Two motor test rig to understand PID Tuning** [read more](#projectf) <br />

7. **Drone development for a national level robotics competition** [read more](#projectg) <br />

8. **Bicopter controller circuit design** [read more](#projecth) <br />

9. **Optical low cost tachometer circuit design** [read more](#projecti) <br />

10. **Robotic Arm design and circuit fabrication** [read more](#projectj) <br />
</div>

<a name="projecta"></a>

Python API to automate belt drive design     
=============================================================================
[Back to Project List](#projectlist)

**Overview :**<br>
The Project involves the creation of an application to automate the design process of a flat-belt drive system.<br>
**Manual Process Disadvantages:**<br>
The manual design calculation is a tiresome process involving many substitutions in pre-derived formulae and in case of design failure during stress testing, the design process has to be repeated again from the beginning. This is not only a tiresome process but also an inefficient one.<br>
**The Automated Process**<br>
- Thus with the advancement of faster computing and better user interfaces an application can be programmed or created to automate the above explained process.<br>
- These programs can produce results with viable inputs in milli-seconds. <br>
- Design failure can be treated with absolute simplicity i.e. just by altering the input values and the rest of the process is executed once again automatically with a click.

Github: <br />
_Python API Screen:_
<img src = "images/tsd_screen.JPG">
_Output in PDF Format:_
<img src = "images/tsd_input.PNG">
<img src = "images/tsd_output.PNG">

<a name="projectb"></a>

Data logging API for Drone test rig
=============================================================================

In order to understand and tune the drone features like battery life, PID values, throttle curve etc there is the need for data logging. This API provides the tool to record data and is based on Pyserial and Arduino library. Hence the program is portable to any place just using some arduino pins and a USB-COM Port. The program saves the data in a time-stamped file with a meta-file which stores additional user data during the initial and final stages of recording. The data is stored in plain text documents as comma seperated files(.csv) which can used in data analysis tools like pandas and excel.

Github: <br />
_API Interface:_
<img src = "images/dl_screen.JPG">
_Data and Meta files:_
<img src = "images/dl_raw_data.JPG">
<img src = "images/dl_data_files.JPG">

<a name="projectc"></a>

Damping characteristics visualisation using Excel 
=============================================================================

Based on the spring and damper hard point data of a vehicle te compression and rebound curves are plotted. The plot gives compression and rebound force for various velocities which are tuned by adjusting the damping coefficient for better ride characteristics

<img src = "images/damping_chart.JPG">

<a name="projectd"></a>

Vehicle flat ride curve for different configurations - Gross and half load
=============================================================================

The ride frequency is a fucntion of the front and rear spring attributes, sprung and unsprung mass. The curve behaves differently for different loading conditions such as Curb-weight, which is only the weight of the car without passengers and the gross weight which includes passenger and cargo. The ride frequency must be between 1~2 hz and a lower or higher value will cause rider discomfort and nausea. Hence this plot is used to analyze the oscillations.

<img src = "images/flat-ride.JPG">
_Curb weight plot_
<img src = "images/Curb-Plot.PNG">

<a name="projecte"></a>

H-I-X Quadcopter frame design fabrication and flight
=============================================================================
The common basic geometries of quadcopter frames are H, I and X type each with its own advantage during flight. This project is to design a frame by combining all the geometries. The outer arms are angled with respect to the pitch and roll axis, while a beam like structure holds them together. The aluminum frame is welded together with the legs at a angle to the yaw axis. This is a research experiment to understand the moment of inertia and how trade-off's are made to attain stable flight and structural integrity. The outer cover is 3D printed using ABS plastic. APM 2.8 is used to control the drone.

<img src = "images/sq.jpg" float="center">
<iframe src="https://drive.google.com/file/d/16gVv8Nz-2nTw7Rf4l84OMdho4PCZcGtm/preview" width="440" height="280"></iframe>

<a name="projectf"></a>

Two motor test rig to understand PID Tuning
=============================================================================
PID (Proportional, Integral and Derivative) controller is the most common control system used in Drones with excepttions such as PI and PD which are like derivated of PID of one knows how to tune a PID system in drones. The two motor test rig is used to tune the system by trial and error method. First the P Value is tuned until peak oscillation (high vibration) which means the system is over-compensating. The P is reduced to half and then the I value is slowly increased in small fractions such as 0.01 since it accumulates at a rate of 250 times per second. Then the D value is increased which retards any acceleration. very high D value is observed is the system does not allow to make any movements and at that point the D value is reduced. This way the below test rig is tuned for optimum self-balancing.

_PID Test Rig_
<img src = "images/pid_test_rig.JPG">

<a name="projectg"></a>

Drone development for a national level robotics competition
=============================================================================
The challenge is to design a frame based on given constraints such as max gross weight of 2 kg and max possible dimensions as 75x75x75 cm. We designed to design the frame using aluminium with some weight reduction plans. Every component of the drone was modelled, assembled and the flight was animated in blender to get a visualization of our end goal. We created a retractable landing gear system completely by ourselves from scratch and wrote a ground station program to control the retracting action from it. We chose NRF for communication between the base station and the drone, but due to high signal interference (SNR) we had to switch to static legs to reduce uncertainity. The APM 2.8 provided the primary flight control system, while we coded an auxillary control system for retractable landing gears and battery monitoring. 

<iframe src="https://drive.google.com/file/d/1fvGgsG8aiVjTWarVCdr8KI2V7szHVUk7/preview" width="340" height="180"></iframe>
<iframe src="https://drive.google.com/file/d/1ijBxgE2g2eeYl49UX6tmJkN4vhrk08eI/preview" width="340" height="180"></iframe>
<iframe src="https://drive.google.com/file/d/1_sE8QI4CoPbFCLRbtQGFpamv8rDjET-l/preview" width="440" height="280"></iframe>
<iframe src="https://drive.google.com/file/d/13qw0g4WzbTRAgL1LZvhbk4GM85R-7lYN/preview" width="440" height="280"></iframe>
<iframe src="https://drive.google.com/file/d/1WmLQ0-KMnjIk4gx-XqOTp5qRfpA_5LjI/preview" width="440" height="280"></iframe>

<a name="projecth"></a>

Bicopter controller circuit design
=============================================================================
The bicopter is a drone with four actuators and unlike a quadcopter the lifting thrust is provided by two and the other two actuators do the work of tilting the thruster axis to control roll and yaw motion. Since aluminium is the primiary material we work with due to material availability, machining and cost effectiveness the circuits often tend to shortcircuit when testing and during crashes. In order to do quick testing one cannot keep insulating and removing the insulation all the time to change and tune PID values. Hence I designed this circuit with a external relay circuit which once activated by a switch is powered by the controller itself. This can be used as a worst case kill switch but that's the most worst case.

<iframe src="https://drive.google.com/file/d/1cZzxsjWjvbPHn8EWmUKaTTPfMXSHzwox/preview" width="640" height="480"></iframe>

<a name="projecti"></a>

Optical low cost tachometer circuit design
=============================================================================
Metrology is the study of measurements standards and techniques. This being a part of my curriculum, I took the project of designing a decent tachometer based on available tools. After going through various aspects to measure RPM (Revolutions per minute) like measuring using encoder, hall effect etcetera optical obstruction seemed like the way to go. The arduino has a interrupt function which is called whenver a change in voltage is observed in the analog pin with refrence to another analog pin. The interrupt handler has a counter which gets incremented every time it is called and a refresh rate of 250 hz (i.e, interrupt being called 250 timed per second) can be achieved quite effortlessly. A laser is pointed on two LDR's (Light dependent diodes) which are monitored for interrupts by the controller. This is a non-contact type tachometer but the only requirement is that the rotating object must have a slim protrusion which can act as a obstruction to the laser source. The circuit diagram shows the connections for the diodes and the wires to be connected to the arduino nano. The LDR can vary its output based on ambient light changes too, hence a potentiometer is integrated to vary the refrence analog voltage. The system must be set and must be calibrated before actual measurement. 

<iframe src="https://drive.google.com/file/d/17cLcyLHuudeTYt8weOdfksoMZv76OEw5/preview" width="640" height="480"></iframe>

<a name="projectj"></a>

Robotic Arm design and circuit fabrication
=============================================================================
Robotic arm are of various types and this is an articualated type which mimic's a human arm. I went to a workshop on 3D printing and found a service provider near me. For the kinematics of machinery project, I modelled the robotic arm and 3D printed it. The circuit was designed using EasyEDA and JLCPCB provides a very low rate on circuit fabrication (2$ for 10 PCB's). I tried their service and got the board within a week time. I solered the components and tested the circuit. The design was not good and had a lot of assembly issues since I didn't account for various 3D printing parameters. I thought not to post this project, but convinced myself that my failures will surely help someone else to design a successful project. 

Tips:  * Account for 3D printing parameters like wall thickness and warping especially for ABS materials. Design curves considering the          extruder diameter to get better shape accuracy and think about the axis of printing for better strength.
       * During any mechanical design, especially cases where movements are default, consider dynamic forces on the body. 
       * Test the actuators with loads prior to designing to get better focus on what is achievable in reality.

<iframe src="https://drive.google.com/file/d/129rR5ZFK4MuVYPfQjMhfjkrr8us1eEwG/preview" width="640" height="480"></iframe>
<iframe src="https://drive.google.com/file/d/1Fl5sxpJg_JtpvMeCFXc11l2F_TS7OqFk/preview" width="640" height="480"></iframe>
<iframe src="https://drive.google.com/file/d/1AzP2k_zsIMuxpWfUex_wcJrfOpzFXNBK/preview" width="640" height="480"></iframe>
