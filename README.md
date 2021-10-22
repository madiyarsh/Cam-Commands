Launch Camera

`roslaunch flea3 stereo_node.launch left:=20509412 right:=20509408`

`ROS_NAMESPACE=stereo rosrun stereo_image_proc stereo_image_proc`

RUN ALGORHITM

`roslaunch uvc_camera orb_slam2_logitech_stereo.launch`

Launch Lidar

`rosrun urg_node urg_node H1301993`


Transformation matrix for lidar

`rosrun tf static_transform_publisher 0 0 0 0 0 0 1 map laser 100`

LAUNCH Hector Slam

`roslaunch hector_slam_launch tutorial.launch`

Single camera:

`roslaunch flea3 single_node.launch device:=20509408`

GAZEBO:
`roslaunch jackal_gazebo jackal_world.launch config:=front_laser

JACKAL RVIZ:
`roslaunch jackal_viz view_robot.launch
