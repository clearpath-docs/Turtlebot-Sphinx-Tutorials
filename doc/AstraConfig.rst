Astra Orbec Pro Configuration
==============================

If you've just installed the Turtlebot ISO from scratch, you'll need to do one extra step to configure it to work with your Orbec Astra! Simply download  `this script <http://www.clearpathrobotics.com/assets/downloads/support/melodic-turtlebot.sh>`_ on your Turtlebot netbook, and run this command from the same directory as the download script.


.. code:: bash

	$ bash melodic-turtlebot.sh

That's it! You can now go ahead and launch Turtlebot and it's associated packages using

.. code:: bash

	$ bash roslaunch turtlebot_bringup minimal.launch
