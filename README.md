# Implementing-Inverse-Kinematics-Modelling-and-Simulation-of-a-Bipedal-Exoskeleton


The project involved developing a bipedal exoskeleton using Inverse
kinematics to map the trajectory of human gait in the gazebo
environment. This is a rehabilitation robot intended to confront
mobility challenges arising from conditions such as paralysis,
hemiplegia, cerebral palsy, Rett syndrome, Parkinson's, and more.
Unfortunately, many of these patients find themselves bedridden for a
significant portion of their lives due to the inability to walk.Our
future work will involve adding sufficient control to evolve a
self-balancing robot in a gazebo environment which would further
enhance exoskeleton functionality.

Steps involved :
1. Created a URDF model
   
![all0](https://github.com/robosac333/Implementing-Inverse-Kinematics-Modelling-and-Simulation-of-a-Bipedal-Exoskeleton-/assets/143353582/15d96a00-ab30-4fe6-8ffa-9e758ea9240e)

2.  Validated DH Parameters using Peter-Corke toolbox on MATLAB and changing ref axes related to joints on DDS Solidworks
   
![image](https://github.com/robosac333/Implementing-Inverse-Kinematics-Modelling-and-Simulation-of-a-Bipedal-Exoskeleton-/assets/143353582/54462437-c2ba-42c4-9f39-215bbd9e2d20)

3. Create an algorithm using DH Parameter (Forward Kinematics) to implement Inverse Kinematics and complete the leg trajectory for both legs

![image](https://github.com/robosac333/Implementing-Inverse-Kinematics-Modelling-and-Simulation-of-a-Bipedal-Exoskeleton-/assets/143353582/1d7aa0b9-f4b8-479e-9a88-d082873c73cf)

4. Added Position Controllers for specified joint limit in each loop to implement Inverse Kinematics changing the joint positions at a frequency to imitate human gait.

ros2 control load_controller --set-state start joint_state_broadcaster

ros2 control load_controller --set-state start velocity_controller

ros2 control load_controller --set-state start position_controller

![2](https://github.com/robosac333/Implementing-Inverse-Kinematics-Modelling-and-Simulation-of-a-Bipedal-Exoskeleton-/assets/143353582/f1b3e9ec-304a-416b-8ebd-11a6991e0907)

Setup and installation:
1. Create a ROS2 Workspace along with a src folder
2. paste the above package in the src folder
3. Launch the urdf model using ros2 launch exo_vone gazebo.launch.py
4. Run the script using ros2 run exovone control_script.py

Enjoy!!
   
