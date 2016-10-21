Bring Up The 3D Sensor
==========================  

The 3D Sensor provided with the TurtleBot does not start with the minimal bringup commands to save power and netbook performance. It is usually started by apps that are launched with custom configuration. You can start the 3D Sensor manually with the following command on your TurtleBot netbook. 

.. Note:: Some 3D Sensors may not work with USB 3.0 port. Please make sure to use USB 2.0 for those devices

.. code:: bash

	roslaunch turtlebot_bringup 3dsensor.launch