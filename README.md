# REAL_lab_info
Information about our lab, the repositories that we use and how we work.

# Repositories that we work with

We want to promote the sharing of code developed in the lab and to increase visibility of which repositories are being actively used, particularly when it comes to the hardware. We want to know what works, so that if a student has an interest in, say, using a particular robot, they know where to start. Minimizing the duplication of work is also desirable. 

We want to keep track of the repositories that we are using for our projects in the lab. When forking from an existing repository, the fork should be made to our organization, newly created repositories should also be added here. To keep track of the repositories so that others can easily re-use and contribute:
 - Add a link to your repo to this README and add some useful details.
 - Ideally repositories that we would typically use together should be grouped, for example, for the UR5 we have the driver, the REAL specific repo and then the ur5/realsense calibration repo.


## Robot repositories

### Universal robots UR5/UR5e
![cobot-universal-robots-ur5e-collaborative-flexible-adaptive-arm-shorr-packaging-2](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/4b9e43f5-71e0-4af9-a2a4-6a16ee49e780)


We have a UR5 and a UR5e in the lab. The UR5 is currently mounted on the Husky and the UR5e is mounted in a cage. We have two robotiq grippers (a 2F-85 and a hand-e) that can be mounted on either of the arms. To work with the robots we suggest using ROS Noetic and Ubuntu 20.04.
We are currently using the following repositories:

&nbsp;&nbsp;&nbsp;&nbsp; **[REAL_ur_robots](https://github.com/montrealrobotics/REAL_ur_robots)**

&nbsp;&nbsp;&nbsp;&nbsp; This repository was created to contain details and configurations specific to our robots, it can be used to run either of the arms in a gazebo simulation or to run the real robots. The repository contains the calibrations for the arms in the lab, as well as files specific to the different hardware combinations such as UR5 and Robotiq hand-e gripper. There are also MoveIt configuration files for each of these combinations.  

&nbsp;&nbsp;&nbsp;&nbsp; **[universal_robot](https://github.com/montrealrobotics/universal_robot)**

&nbsp;&nbsp;&nbsp;&nbsp; This repository is a requirement for REAL_ur_robots, we have cloned it to make some tweaks. The original repo only supports up to ROS Melodic. Our fork uses the newest version of the ROS UR driver and works with ROS Noetic.

&nbsp;&nbsp;&nbsp;&nbsp; **[ur_realsense calibration](https://github.com/montrealrobotics/ur5_realsense_calibration)**

&nbsp;&nbsp;&nbsp;&nbsp; If you wish to use a realsense camera with a UR5/UR5e and wish to calibrate to find the transform between the robot arm and the camera, you can use this repository. The original repository hasn't been updated since over 3 years so we cloned it and updated it to work with ROS Noetic.

&nbsp;&nbsp;&nbsp;&nbsp; **[ur_kinematics](https://github.com/montrealrobotics/ur_kinematics)**

&nbsp;&nbsp;&nbsp;&nbsp; We use this kinematics package for calculating forward and inverse kinematics for the UR5, it is not used in our normal pipeline but is required for [robo-gym](https://github.com/montrealrobotics/robo-gym). This package was cloned and edited to be a catkin package.

### Robotiq Grippers
![robotiq-grippers](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/b2b9339d-33dc-4a91-964c-2125b2a33ed7)


There are three 2F-85 grippers and one hand-e gripper in the lab. The mounting can be used to attach the grippers to either 
a UR5 arm or a Franka Panda/FR3 arm.

The repository that we use with these grippers is:

&nbsp;&nbsp;&nbsp;&nbsp;  **[robotiq](https://github.com/montrealrobotics/robotiq)**

### Franka
![csm_franka_panda_bedienung_6b014be50b](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/6c184aca-bee8-4c85-9e11-2c8d600354b6)

We have three Franka FR3 arms in the lab. 
We currently control them with the [Polymetis](https://github.com/montrealrobotics/fairo) controller.

Other Franka repositories that we use:

&nbsp;&nbsp;&nbsp;&nbsp; **[panda-gym](https://github.com/montrealrobotics/panda-gym)**

### Husky
![A008_C036_0730G1](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/ffb90a84-6e96-405b-8dcc-19c2073284f6)

Repositories that we use for this robot:

&nbsp;&nbsp;&nbsp;&nbsp; **[REAL_Husky_robot](https://github.com/montrealrobotics/REAL_Husky_robot)**

### Jackal
![A008_C100_0730BA](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/a3e0cae1-cb33-466b-a646-a822f20af8d4)

### Unitree Go1
![go1-800x600](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/06779495-8237-4ade-90c1-a176d0b469e7)

Repositories that we use for this robot:

&nbsp;&nbsp;&nbsp;&nbsp;**[REAL_unitree_robots](https://github.com/montrealrobotics/REAL_unitree_robots)**

### Interbotix Arms
![xsarm_family](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/ca5cef23-7b06-4074-877d-3fb171cb468e)

Repositories that we use for this robot:

&nbsp;&nbsp;&nbsp;&nbsp; **[REAL_interbotix_sdk](https://github.com/montrealrobotics/REAL_interbotix_sdk)**

&nbsp;&nbsp;&nbsp;&nbsp; **[REAL_interbotix_udp_to_ros](https://github.com/montrealrobotics/REAL_interbotix_udp_to_ros)**

&nbsp;&nbsp;&nbsp;&nbsp; **[interbotix_ros_core](https://github.com/montrealrobotics/interbotix_ros_core)**

&nbsp;&nbsp;&nbsp;&nbsp; **[interbotix_ros_manipulators](https://github.com/montrealrobotics/interbotix_ros_manipulators)**


### Locobot
![wx200_front](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/d92adabb-6068-4a5c-ae9b-545fc1db8adf)

We have several Locobots in the lab. The documentation for how to get them up and running is [here](https://docs.trossenrobotics.com/interbotix_xslocobots_docs/ros_interface/ros1/software_setup.html)

Repositories that we use for this robot:

&nbsp;&nbsp;&nbsp;&nbsp; **[interbotix_ros_rovers](https://github.com/montrealrobotics/interbotix_ros_rovers)**

&nbsp;&nbsp;&nbsp;&nbsp; This is a fork of the original repository. We use this repo to control the locobots.

### Stella
![Screenshot from 2023-09-07 15-14-24](https://github.com/montrealrobotics/REAL_lab_info/assets/11501425/b4bda192-423b-4f38-82f5-661e8d781e6d)
We have one Stella quadruped from ahead.io in the lab. The robot can be controlled to execute simple commands via a joystick.
For more low level control of the robot, we are waiting for control software for the robot, it is currently still
in development. 

&nbsp;&nbsp;&nbsp;&nbsp; **[acreature-server](https://github.com/AheadIO/acreature-server)**

&nbsp;&nbsp;&nbsp;&nbsp; This is the external repository where the code to control the Stella is being developed. It contains
the server software which should run onboard the robot as well as python examples which can be run on a remote computer.


### Sensors
&nbsp;&nbsp;&nbsp;&nbsp; **[open3d-realsense](https://github.com/montrealrobotics/open3d-realsense)**

## RL packages

&nbsp;&nbsp;&nbsp;&nbsp;**[DeepRLInTheWorld](https://github.com/montrealrobotics/DeepRLInTheWorld)**

### Training toolkits

&nbsp;&nbsp;&nbsp;&nbsp; **[robo-gym](https://github.com/montrealrobotics/robo-gym)**

&nbsp;&nbsp;&nbsp;&nbsp; **[robo-gym-robot-servers](https://github.com/montrealrobotics/robo-gym-robot-servers)**

&nbsp;&nbsp;&nbsp;&nbsp; **[safety-gym](https://github.com/montrealrobotics/safety-gym)**

&nbsp;&nbsp;&nbsp;&nbsp; **[safety-gymnasium](https://github.com/montrealrobotics/safety-gymnasium)**

### RL algorithm repositories 
&nbsp;&nbsp;&nbsp;&nbsp; **[cleanrl](https://github.com/montrealrobotics/cleanrl)**

================================================================================

## Projects
### Robo zoo
&nbsp;&nbsp;&nbsp;&nbsp; **[REAL_robo_zoo](https://github.com/montrealrobotics/REAL_robo_zoo)**

### Pupper fetch
&nbsp;&nbsp;&nbsp;&nbsp; **[pupperfetch](https://github.com/montrealrobotics/pupperfetch)**

### iv_rl
&nbsp;&nbsp;&nbsp;&nbsp; **[iv_rl](https://github.com/montrealrobotics/iv_rl)**

&nbsp;&nbsp;&nbsp;&nbsp; **[iv-rl-experiments](https://github.com/montrealrobotics/iv-rl-experiments)**

### R2D2
&nbsp;&nbsp;&nbsp;&nbsp; **[R2D2](https://github.com/montrealrobotics/R2D2)**

&nbsp;&nbsp;&nbsp;&nbsp; **[fairo](https://github.com/montrealrobotics/fairo)**

### LTVN
&nbsp;&nbsp;&nbsp;&nbsp; **[ltvn](https://github.com/montrealrobotics/ltvn)**

&nbsp;&nbsp;&nbsp;&nbsp; **[ltvn_old](https://github.com/montrealrobotics/ltvn_old)**



================================================================================

# Software development practices

In an effort to enable better software development practices in the lab, we have created some rules that all students should follow when contributing to our group's github organisation. Practicing these skills are very helpful and will be valuable in getting a job after graduate school.

## Contribution guidelines
### Shared repositories that need to be more stable:
Students will not be able to make any kind of commits directly to the main branch  of these repositories.
To contribute to these repositories, students should:
 - Create a new branch with a descriptive name
 - Commit changes to this branch
 - Create a pull request (PR) and have someone from the lab review the PR before merging to main. 
### Repositories that are less critical:
 - If you are creating a new repository, the name should be descriptive and I would advise to add REAL_ to the start to help us differentiate between our repos and forked repos.
 - Commits should be descriptive so that if required, changes can be more easily tracked.
 - Keep changes in new branches so that your main branch is stable. Merge to main once tested.

================================================================================

# Useful tools
