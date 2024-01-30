# Robot Ignite Code Foundation for ROS Prerequisites Exam
This repository contains the tasks  related to the Linux for Robotics course and Python for Robotics Course in The Construct

# Part 1: Linux for Robotics
**Task 0**:
Inside your workspace (~/catkin_ws/src/), create a new folder named linux_exam. Inside this folder you will place all the files required for the exam. The full path has to be like this:
![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/ff93c108-26b0-4581-8d57-f338c59364f1)

Specifications
The new folder created has to be a regular folder, NOT A ROS PACKAGE.

**Task 1**:
Inside the linux_exam folder, create a new bash script named task1.sh, that does the following:

a) First, it moves inside the linux_exam folder.

b) Once it is there, it generates a folder structure like the following one: this->is->my->linux->exam (check Specifications)

c) Inside the final folder, named exam, it creates a new file named my_file.py

d) Finally, it prints to the screen the following string:
![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/b6b94bf6-1963-4603-a175-1da31d6931ca)

Specifications
The string printed at the end MUST be exactly the same as the one showed above.
The full folders structure has to be like this:
![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/50e1198e-1fb5-4b33-b749-96c1dce2e4ce)



**Task 2**:
Given the following ROS commands:

To make the Turtlebot robot perform a small square movement:

![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/66b398c8-9243-4b94-ae2d-6f018cec340e)



To make the Turtlebot robot perform a medium square movement:

![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/395ad310-b546-4e24-8c23-eaf6bba57645)





To make the Turtlebot robot perform a big square movement:

![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/aabe0173-03ab-41e5-8317-dc1dfa7dc6c2)


Inside the linux_exam folder, create a new bash script, named task2.sh, that does the following:

It receives one parameter, which can contain one of the following values:

small_square

medium_square

big_square

If the parameter is small_square, the bash script will make the Turtlebot robot perform the small square movement.
If the parameter is medium_square, the bash script will make the Turtlebot robot perform the medium square movement.
If the parameter is big_square, the bash script will make the Turtlebot robot perform the big square movement.
Specifications
The name of the parameters received by your bash script MUST be exactly the same as the ones specified above.

**Task 3**:
Inside the linux_exam folder, create a new bash script, named task3.sh, that does the following:

a) First, it goes to the folder named exam, which you created in Task 1.

b) Once there, it removes any existing file, and it creates 3 new ones, named like this: exam1.py, exam2.py and exam3.py.

c) Finally, it assigns to each file the following permissions:

exam1.py:

Owner: Read, Write and Execute

Group: Read and Execute

All others: Read

exam2.py:

Owner: Read and Execute

Group: None

All others: Execute

exam3.py:

Owner: Write

Group: Read

All others: Execute

#  Part 2: Python for Robotics

**Task 0:**
1. Inside your workspace (~/catkin_ws/src/), create a new folder named python_exam. Inside this folder you will place all the files required for the exam. The full path has to be like this:

![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/196c31c0-b339-4cfb-a799-ab681d812794)

**Task 1:**
Inside the python_exam folder, create a new Python script named task1.py. Inside this script, create a function named get_highest_lowest. This function does the following:

a) First, it creates an instance of the RobotControl class.

b) Second, it gets all the values of the laser readings and it stores them into a list.

c) Then, it compares all these laser values that you have stored in the list in order to detect the highest value and the lowest one.

d) Finally, it returns the position in the list of the highest and lowest values (check Specifications).

Specifications
The name of the function MUST BE the one specified above: get_highest_lowest
Bear in mind that the function doesn't have to return the values (highest and lowest), but the position in the list of those values.
Your final (after you have tested that it works properly) program MUST contain the get_highest_lowest function, but MUST NOT contain any call to this function.
The function has to return the position values in an specific order: first, it returns the position of the highest value and second, it returns the position of the lowest value.
The laser readings list may contain some values that are expressed as inf. You MUST NOT take these values into account when calculating the highest and lowest value. Only take into account the numeric values.

**Task 2:**
Inside the python_exam folder, create a new Python script, named task2.py, that does the following:

a) First, it starts moving the robot forwards while it captures the laser readings in front of the robot.

b) When the laser readings detect that there's an obstacle (the wall) at less than 1 meter in front of the robot, the robot will stop its movement.

c) After it stops, the robot will turn 90 degrees to his right, facing the opening corner in the room (check Specifications).

Specifications
After turning 90 degrees, the robot MUST end in the orientation showed below (facing the opening corner):
![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/2284a8a9-93c8-4bf3-b8bc-a95b13445d4b)

Expected behaviour:
![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/4fbb709e-3308-4a74-9d64-7c024e60e8ae)

**Task 3:**
Inside the python_exam folder, create a new Python script, named task3.py. Inside this script, create a Python class named ExamControl.

The ExamControl class has to contain, at least, the following 2 methods:

get_laser_readings: This method, when called, returns the values of the laser readings of the right and left side of the robot (check Specifications).
main: This method, when called, makes the Turtlebot robot start the behavior described below:
Initially, the robot starts moving forward, towards the opening in the room.

While moving forward, your program keeps checking the values of the laser readings at the right and left sides of the robot.

When these laser values indicate that there are no obstacles detected at the left or at the right side, the robot will stop its movement.

Check the Example section for more details on the expected behavior.

Specifications
The names of the class and the methods MUST BE exactly the same as the ones specified above.
Your final program (after you have tested that it works properly) MUST contain the ExamControl class, but MUST NOT contain any instance of the class.
The initial position of the robot for this exercise it's the end position of the robot in the previous Exercise (check Fig. 1).
The get_laser_readings method has to return the values in an specific order: first, it returns the value of the left side and second, it returns the value of the right side.
We consider as laser readings from the left and right sides of the robot, the ones at the extremes of the laser values array. Remember the following image:
All the code of the class has to be contained INSIDE the class. This means, do not declare any variable or function outside the class.

![image](https://github.com/Poo-09/CodeFoundationForROS/assets/100222055/0f2021a0-5017-4b9e-983b-a34846142ebf)



