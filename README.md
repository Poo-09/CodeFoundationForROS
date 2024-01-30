# Robot Ignite Code Foundation for ROS Prerequisites Exam
This repository contains the tasks  related to the Linux for Robotics course and Python for Robotics Course in The construct

# Part 1: Linux for Robotics
 Task 0
Inside your workspace (~/catkin_ws/src/), create a new folder named linux_exam. Inside this folder you will place all the files required for the exam. The full path has to be like this:


/home/user/catkin_ws/src/linux_exam
Specifications
The new folder created has to be a regular folder, NOT A ROS PACKAGE.
 Task 1
Inside the linux_exam folder, create a new bash script named task1.sh, that does the following:

a) First, it moves inside the linux_exam folder.

b) Once it is there, it generates a folder structure like the following one: this->is->my->linux->exam (check Specifications)

c) Inside the final folder, named exam, it creates a new file named my_file.py

d) Finally, it prints to the screen the following string:


This bash script has finished!
Specifications
The string printed at the end MUST be exactly the same as the one showed above.
The full folders structure has to be like this:

/home/user/catkin_ws/src/linux_exam/this/is/my/linux/exam/my_file.py
 Task 2
Given the following ROS commands:

To make the Turtlebot robot perform a small square movement:


rosrun linux_exam small_square.py


To make the Turtlebot robot perform a medium square movement:


rosrun linux_exam medium_square.py


To make the Turtlebot robot perform a big square movement:


rosrun linux_exam big_square.py


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
 Task 3
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


