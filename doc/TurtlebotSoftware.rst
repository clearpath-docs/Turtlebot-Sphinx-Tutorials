Bring Up The TurtleBot Software
===================================    

Once the network is setup, we now need to bring up the TurtleBot software. This starts up the TurtleBot with the basic single master ROS environment in which all processes can be started/stopped via roslaunchers. Enter the following line in a terminal on the TurtleBot netbook:

.. code:: bash

	$ roslaunch turtlebot_bringup minimal.launch 

You should now be able to see all of the TurtleBot related nodes on both your TurtleBot netbook and workstation if you type to following command:

.. code:: bash

	$ rosnode list