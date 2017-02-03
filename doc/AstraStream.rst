Setting Up Color Video Stream
==============================

To set up the color video stream on the Orbbec Astra pro, make a sourced
workspace from the repositories below. If you're not familiar with making your
own sourced workspace in ROS, just follow these step by step instructions!
If you already have a turtlebot_ws workspace, you may need to remove it before
running through these instructions

.. code:: bash

 $ bash rm -rf turtlebot_ws

Then run these commands!

.. code:: bash

  $ bash mkdir -p turtlebot_ws/src
  $ bash cd turtlebot_ws/src
  $ bash catkin_init_ws
  $ bash git clone https://github.com/clearpathrobotics/ros_astra_launch.git --branch upstream
  $ bash git clone https://github.com/clearpathrobotics/ros_astra_launch.git --branch upstream
  $ bash cd ..
  $ bash rosdep install --from-paths src --ignore-src --rosdistro=indigo -y
  $ bash catkin_make
  $ bash source devel/setup.bash
  $ bash rosrun astra_camera create_udev_rules
  $ bash roslaunch astra_launch astra_pro.launch

That should do it! You can not open up Rviz and see color videos.
Make sure to always source this workspace when opening a new terminal.
