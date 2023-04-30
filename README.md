# Robothon23_Team_RoboPig
This repository is the submission of team RoboPig of THWS for the Robothon 2023 competition 

For a more detailed overview, please take a look at the [pdf version](https://github.com/Usaali/Robothon23_Team_RoboPig/blob/main/Submission%20for%20Robothon%202023.pdf)

## Hardware dependencies
- General Equipment
  - UR5e robot arm
  - Robotiq Hand E Gripper with IO coupling
  - 3D printed gripper jaws
  - Azure Kinect camera
- Taskboard
  - 3D printed cable hook
- BYOD Transferability Task
  - Tektronix TDS 2002B
  - Custom PCB
  - Custom plug for robot
  - Computer

## Software dependencies
- ROS
  - Realsense-ros
- C++
  - Eigen
  - ur_rtde
  - IDS-peak
  - open_cv
- Python
  - open_cv
  - numpy
  - usb_tmc

## Quick start guide
### 1. Launch core driver depending on task (eg. taskboard_core.launch for taskboard)
#### a. This will:
- Start cameras and begin publishing images
- Start the robot driver and begin publishing robot positions
- Start a pose management node and publish all relevant poses
		
#### b. System is now ready and waits for task scheduler
	
### 2. Run task scheduler and input order of tasks
#### a. This will:
- Generate the desired task sequence 
- Run the image processing pipeline depending on what task is chosen
- Update all positions depending on the camera detection

## Submission videos
- The 5 minute video containing a video of our team explaining the solution to the taskboard and a BYOD demo of our robot platform can be found [here](https://cloud.fhws.de/s/XMiiNnsXjnTxfKD)
- The 10 minute video showing our solution doing the Taskboard challenge 5 times can be found [here](https://cloud.fhws.de/s/nXWnQFLCZbzyewY)
