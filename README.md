#Launch Camera

roslaunch flea3 stereo_node.launch left:=20509412 right:=20509408

`<roslaunch flea3 stereo_node.launch left:=20509412 right:=20509408>`

ROS_NAMESPACE=stereo rosrun stereo_image_proc stereo_image_proc

#RUN ALGORHITM

roslaunch uvc_camera orb_slam2_logitech_stereo.launch

#Launch Lidar

rosrun urg_node urg_node H1301993

#Transformation matrix for lidar

rosrun tf static_transform_publisher 0 0 0 0 0 0 1 map laser 100
