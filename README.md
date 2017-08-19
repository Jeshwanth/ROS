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
