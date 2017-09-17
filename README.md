# ROS
Learning ROS


Some commands:

docker run -v /home/susanootux/mywork/ros:/jeshros -it ros_basic


docker exec -it 25a3b809c165 bash


docker run -v /home/susanootux/mywork/ros:/jeshros -i -t --net=host -e DISPLAY -v /tmp/.X11-unix  ros_basic


rosrun turtlesim turtle
rosrun turtlesim turtlesim_node __name:=my_turtle

rosrun turtlesim turtle_teleop_key


rosrun rqt_graph rqt_graph

rostopic echo /turtle1/cmd_vel

rostopic list -v

rostopic type [topic]

rostopic pub -1 /turtle1/cmd_vel geometry_msgs/Twist -- '[2.0, 0.0, 0.0]' '[0.0, 0.0, 1.8]'

rostopic hz /turtle1/pose


rostopic type /turtle1/cmd_vel | rosmsg show

rosrun rqt_plot rqt_plot

rosservice list
rosservice call /clear

rosparam get /

rosparam dump [file_name] [namespace]
rosparam load [file_name] [namespace]


rosrun rqt_console rqt_console

rosrun rqt_logger_level rqt_logger_level

rosed [package_name] [filename]




Notes:

ros node: Its an indivisual program which runs for its own purpose.

ros topic: topic is the communication identifier the nod recognize, where the nodes can publish or subscribe to topics.

rkt graph: Its a tool to visualize the connections like who subscribed to which topic and who published to where. 

rostopic: Its a command where u can communicate with the topics, like publish, subscribe, list, info etc ( Refer http://wiki.ros.org/ROS/Tutorials/UnderstandingTopics for more details on how to use rostopic)

rqt_plot: Plots the graps for messages or data.

rosservice: Its also used for communication between nodes, but also can send requests and wait for response. 

rosparam: rosparam allows you to store and manipulate data on the ROS Parameter Server

rqt_console and rqt_logger: used to see the logs rom the nodes and set the diferent log level.

roslaunch: we can use roslaunch to group and launch the multiple nodes.

rosed: rosed can be used to edit the ros files/packages.

ros msg: Ros messages are stored in the msg directory of the package and it will store all the messages for the package in the form of type name in a line. Example: int8 num

ros srv: srv file contains the fields for request and response. 

rosbag: can be used to record and play the data.

