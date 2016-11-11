Setting Up Color Video Stream
===============================    

1.  Install the ``libuvc_camera`` by running ``sudo apt-get install ros-indigo-libuvc_camera﻿⁠⁠⁠⁠``. The ROS_MASTER_URI tells the rest of the nodes at which address they can find the ROS master.

2.  Start ``roscore`` in a terminal and run the uvc camera driver by ``rosrun libuvc_camera camera_node``.  This hsould give an error which is related to the Udev rules as shown below. 

.. code:: bash 

	[ INFO] [1478626609.932998554]: Opening camera with vendor=0x0, product=0x0, serial="", index=0
	[ERROR] [1478626609.933144867]: Permission denied opening /dev/bus/usb/XXX/XXX

3. Change the permission with ``sudo chmod o+w /dev/bus/usb/XXX/XXX``. Note that the values of XXX/XXX depend on your system. 

4. Launch the Turtlebot as normal.  Open a new terminal and change the default namespace with ``export ROS_NAMESPACE=camera/rgb/``. Run the uvc driver using ``rosrun libuvc_camera camera_node``. 

5. Open rViz and add aDepthCloud display type. Select ``/camera/depth/image_raw`` as the Depth Map Topic and ``/camera/rbg/image_raw`` as the Color Image Topic.  This will show the depth cloud in rViz. 

