Setting Up Color Video Stream
==============================

To set up the color video stream on the Orbbec Astra pro, make a sourced
workspace from the repositories below. If you're not familiar with making your
own sourced workspace in ROS, just follow these step by step instructions!
If you already have a turtlebot_ws workspace, you may need to remove it before
running through these instructions

.. code:: bash

 $ rm -rf turtlebot_ws

Then run these commands!

.. code:: bash

  $ mkdir -p turtlebot_ws/src
  $ cd turtlebot_ws/src
  $ catkin_init_ws
  $ git clone https://github.com/clearpathrobotics/ros_astra_launch.git --branch upstream
  $ git clone https://github.com/clearpathrobotics/ros_astra_camera.git --branch upstream
  $ cd ..
  $ rosdep install --from-paths src --ignore-src --rosdistro=melodic -y
  $ catkin_make
  $ source devel/setup.bash
  $ rosrun astra_camera create_udev_rules
  $ roslaunch astra_launch astra_pro.launch

That should do it! You can not open up Rviz and see color videos.
Make sure to always source this workspace when opening a new terminal.
