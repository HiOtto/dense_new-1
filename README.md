This is the webpage of the open-source packages of our paper submitted to ICRA2016. Our implementation of dense tracking is built on the top of the open-source and vectorized implementation of [1]. Our package is compatible with the standard driver of VI-Sensor and ROS version of indigo. OpenCV is needed. ROS packages related to VI-sensor is needed, too. (https://github.com/ethz-asl/libvisensor and https://github.com/ethz-asl/visensor_node.git)

The high resolution video of our submitted paper is: 
https://onedrive.live.com/redir?resid=907AC500FCC6D19C!256&authkey=!AFx_upC8zphx44w&ithint=video%2cmp4

If you can not visit Microsoft Onedrive, please add 
"
134.170.108.26 onedrive.live.com   
134.170.109.48 skyapi.onedrive.live.com
"
in the end of windows/system32/drivers/etc/hosts. (windows user)

We have uploaded the experimental data shown in the video. All the raw data, estimatior output, UKF smoothing output, control command and etc. are included in the rosbags. To download it, please visit,
https://onedrive.live.com/redir?resid=907AC500FCC6D19C!2972&authkey=!ACEqE_Xtr5aruco&ithint=folder%2c


TODO (to be fixed soon):
There is a problem caused by our internal use of quadrotor_msgs/Odometry.h. If you meet complier problems, please do minor modifications:

quadrotor_msgs/Odometry.h --> nav_msgs/Odometry.h
quadrotor_msgs::Odometry --> nav_msgs::Odometry
quadrotor_msgs --> nav_msgs

modify code that look like odom_msg.curodom.xxxx to odom_msg.xxx, ignore odom_msg.kfodom.xxxx where the message is constructed to be published.




If you use our code, please cite our paper "Aggresive Quadrotor Flight Using Dense Visual-Inertial Fusion", in Proc. of the IEEE Intl. Conf. on Robot. and Autom., 2016. 

For more questions, please contact ylingaa at connect dot ust dot hk .




[1] LSD-SLAM: Large-Scale Direct Monocular SLAM (J. Engel, T. Schöps, D. Cremers), In European Conference on Computer Vision (ECCV), 2014.
