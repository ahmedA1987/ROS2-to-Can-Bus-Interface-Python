# ROS2-to-Can-Bus-Interface-Python
This is a ROS2 pkg that contain ROS2 node in python language that recives the messages from the Can bus and publish them to a ROS2 topic with a custom message

# To run this node

1- install the following

A) python 3 and the pip modul using the following commands

$ sudo apt-get install python3

$ sudo apt install python3-pip

B)- install python-can library. This library provide the interface to the can and provide you with the needed tools for sending and receaving the messages. The command to install the library:

$ pip install python-can

source: https://python-can.readthedocs.io/en/stable/

C) Also install serial library using the follwoing command:

$ pip install python-can[serial]

If an error occure because of serial then install pyserial  https://www.geeksforgeeks.org/how-to-install-python-serial-package-on-linux/

$ sudo pip3 install pyserial

D) Install can tools. This python library provides the needed functions to encode and decode the can messages according to the DBC files.
https://cantools.readthedocs.io/en/latest/

$ pip install cantools

2- install the needed drivers for your canbus adapter.

3- Connect the USB to can Adapter and open terminal. In the terminal type the following command. Note that the bitrate have to be sane as your canbus bitrate so that you have to make sure to change it according to your CAN Bus specifications.

$ sudo ip link set can0 up type can bitrate 500000
$ sudo ip link set can0 up type can bitrate 250000

This command is needed every time you start connecting to the CAN network.
set the bitrate to the value you need and you can use the can0 or change the name to be preffared name. In the link below you can see also how to set virtual CAN port if you dont need to connect to real device.

Source: https://python-can.readthedocs.io/en/stable/interfaces/socketcan.html
