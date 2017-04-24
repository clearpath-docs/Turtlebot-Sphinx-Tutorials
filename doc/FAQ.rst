Frequently Asked Questions
============================   

Teleop doesn't work, dashboard has errors, and there is no chime on bringup
-----------------------------------------------------------------------------

It's possible you are missing your udev rules. To check if that is the case, plug in your Kobuki and run:

.. code:: bash

	ls -l dev

If the udev rules are set up correctly, you should see something along the lines of :

.. code:: bash

	lrwxrwxrwx 1 root root 7 Dec 3 12:06 kobuki -> ttyUSB0

If you don't, then you can create the udev rules using:

.. code:: bash

	rosrun kobuki_ftdi create_udev_rules

Once that is done, reboot your netbook and try running the bring up again. You should her a chime from the Kobuki 

.. code::bash

	roslaunch turtlebot_bringup minimal.launch

There is no DepthCloud image in Rviz
---------------------------------------

There is a conflict with the DepthCloud and Registered Depthcloud. To bring up your camera in such a way to view the depth cloud, you will need to set the registered depthcloud arguments to false during launch, try using this:

.. code:: bash

	roslaunch turtlebot_bringup 3dsensor.launch depth_registered_processing:=false depth_registration:=false

You can then launch Rviz as you normally would

.. code:: bash

	roslaunch turtlebot_rviz_launchers view_robot.launch

You should now be able to see the DepthCloud simulation!

Why is my TurtleBot drifting?
--------------------------------

There have been reports of these Kobukis having a bug in the firware that caused a drift. Updating to the latest firmware should be relatively painless. You can follow these instructions: 

http://kobuki.yujinrobot.com/home-en/documentation/howtos/upgrading-firmware/

How can I power my latop with my Turtlebot?
-----------------------------------------------

The steps to perform this modification can be found on page 17 of our `User Manual <http://www.clearpathrobotics.com/turtlebot_2/downloads/>`_.


.. note:: Always test the polarity of your modified cable before plugging it into your netbook, the outside of the barrel should be grounded, and the inside should be positive.

The 19V laptop power connection does not provide power
--------------------------------------------------------

The 19V output will only turn on when the Kobuki is plugged in or docked for charging. The Netbook will charge along-side the Kobuki, but not at the same time. This is done to preserve the Kobuki battery by prohibiting it from discharging to charge the laptop

