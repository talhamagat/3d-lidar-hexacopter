## 4iLabHexacopter_SLAM

# ``` Project - Hexacopter SLAM(Simultaneous Localization and Mapping) ``` 
## ```Organization - 4i Labs IIT Guwahati ```


### About the Project - 
Hexacopter SLAM is one of the projects of 4i Labs under IIT Guwahati. The aim of the project is to develop a Hexacopter which is capable of sensing about the unknown environment and then contructing the map online. With the help of a lidar(here RP Lidar A3) we will be able to fetch the data about the unknown environment. The lidar uses laser triangulation ranging principle with high-speed RPVision ranging engine which measures distance data nearly 16000 times per second and keep its excellernt performane in a long distance.In this project we are using Hector SLAM package for the analyzing the data from the lidar and then creating a local map of the environment. The package works independently whether lidar is installed upon a drone or land robot or water vehicle. Our main goal here is to install the lidar on a drone and make sure that proper construction of map happens when the lidar is used while the lidar being on a drone. This goal requires some adjustments to the SLAM package as well as ROS which is used to control the Hexacopter. 
                    
                    
 ## Instructions to run the lidar on a system
 
 - Clone this repository on your system
 - Change directory to the workspace and execute "catkin_make" in the terminal 
 - Source  setup the file by executing the below commands
     i.source ~/{workspace_name}/devel/setup.bash
 - Now run the following command to see the visual input(also compulsory for the hector slam) fetched by the lidar
       roslaunch rplidar_ros view_rplidar_a3.launch
 - In new terminal type the below command to construct the map 
        roslaunch hector_slam_launch tutorial.launch
        
 Some suggestions - 
 - While executing the commands be sure to give full priviledges to the USB through which the Lidar is connected, the below command helps in the case if terminal       shows timeout
        sudo chmod 777 ttylUSB0
        
 ### Further Instructions for linking to Mavros will be updated        
 
