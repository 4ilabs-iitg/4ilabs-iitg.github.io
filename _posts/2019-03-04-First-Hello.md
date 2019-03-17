---
layout:     post
title:      ARLE Mini SLAM 
author:     Abhay Pratap Singh
tags: 		4ilabs arle rosbot slam
category:   arle
subtitle:  	Using ROSbot SLAM
visualworkflow: true
---
<!-- Start Writing Below in Markdown -->

# Using SLAM for ARLE Mini

<hr class="style-one">

<br>

### ARLE Mini :
 
 ARLE Mini is an autonomous open source robot capable of navigating using RPLidar powered by Intel NUC

 ARLE Mini is a miniature version of ARLE(Autonomous Robot for Library Enhancement) being developed for managing books in the institute library of Indian Institute of Technology, Guwahati. ARLE is aimed to be able to navigate autonomously in the library, identify books and racks using RFIDs, pick and place the books in the correct rack using an arm mounted on the bot.

<div class="row">
	<div class="col-lg-6">
		<img src="/img/arle_mini1.jpg" width="500px" alt="ARLE Mini top view"/>	
	</div>

	<div class="col-lg-6">
		<img src="/img/arle_mini2.jpg" width="500px"/>
	</div>

	<p class="col-lg-12" style="text-align: center; margin: 20px 0px; font-size: 15px;">ARLE Mini first build</p>

</div>


<br>
<br>


<hr class="style-one">

### Modules used for Autonomous Movement

-	**Tf (tf2)**: Coordinate the transform library. It's one of the most important packages for ROS. Thanks to tf, you can manage all coordinate values, 	 including the position of the robot or relations between the camera and wheels. For treating various categories of coordinates, several distinctive concepts such 		as frame and tree are adopted.

- **slam_gmapping**: ROS wrapper for OpenSlam's Gmapping. gmapping is one of the most famous SLAM algorithms. While still popular, there are also several alternatives now for this function.

- **move_base**: Core module for autonomous navigation. This package provides various functions, including planning a route, maintaining cost maps, and issuing speed and direction commands for motors.
    Robot_state_publisher. Publishes the 3D poses of the robot links, which are important for a manipulator or humanoid. In the case of SAWR, the most important data maintained by this module is the position and orientation of the robot and the location of the camera relative to the robot’s position.

- **Robot_state_publisher**: Publishes the 3D poses of the robot links, which are important for a manipulator or humanoid. In the case of SAWR, the most important data maintained by this module is the position and orientation of the robot and the location of the camera relative to the robot’s position.

<br>
<br>

![sawr_graph]


[sawr_graph]: https://software.intel.com/sites/default/files/managed/5e/8c/Build-Autonomous-Mobile-Robot-Intel-RealSense-Camera-ROS-SAWR-fig13.png "SAWR ROS node graph viewed by rqt_graph"
{: width="1100px" style="float: none;"}

 <p class="col-lg-12" style="text-align: center; margin: 10px 0px; font-size: 15px;">SAWR ROS node graph viewed by rqt_graph</p>



<br>

Find some useful content on SLAM & Mapping for autonomous robots [here][intel_sawr]

[intel_sawr]: https://software.intel.com/en-us/articles/build-an-autonomous-mobile-robot-with-the-intel-realsense-camera-ros-and-sawr