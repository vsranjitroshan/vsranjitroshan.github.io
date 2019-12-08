## Ranjit Roshan
I am a undergrad student who found his flow in drone design and development. Feel free to check my projects and works.

## Project Index 
-> **Python API to automate belt drive design**
-> **Data logging API for Drone test rig**

Python API to automate belt drive design
=============================================================================

The Project involves the creation of an application to automate the design process of a flat-belt drive system. The manual design calculation is a tiresome process involving many substitutions in pre-derived formulae and in case of design failure during stress testing, the design process has to be repeated again from the beginning. This is not only a tiresome process but also an inefficient one. Thus with the advancement of faster computing and better user interfaces an application can be programmed or created to automate the above explained process. These programs can produce results with viable inputs in seconds. Design failure can be treated with absolute simplicity i.e. just by altering the input values and the rest of the process is executed once again automatically at the click of a button.

Github: 
_Python API Screen:_
<img src = "images/tsd_screen.JPG">
_Output in PDF Format:_
<img src = "images/tsd_input.PNG">
<img src = "images/tsd_output.PNG">

Data logging API for Drone test rig
=============================================================================

In order to understand and tune the drone features like battery life, PID values, throttle curve etc there is the need for data logging. This API provides the tool to record data and is based on Pyserial and Arduino library. Hence the program is portable to any place just using some arduino pins and a USB-COM Port. The program saves the data in a time-stamped file with a meta-file which stores additional user data during the initial and final stages of recording. The data is stored in plain text documents as comma seperated files(.csv) which can used in data analysis tools like pandas and excel.

Github:
_API Interface:_
<img src = "images/dl_screen.JPG">
_Data and Meta files:_
<img src = "images/dl_raw_data.JPG">
<img src = "images/dl_data_files.JPG">

