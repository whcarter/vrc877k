# vrc877k
This is Ridgefield Robotics Team 877K's full competition code for the 2022-2023 Vex Robotics Competiton season Spin Up.

## Features
1. Our robot uses x-drive rather than tank drive, allowing us to move in any direction with a high degree of manueverability. The left joystick controls movement relative to the robot (forward, right, back, etc.) and the right joystick controls the robot's heading. 
2. We use the Vision sensor to assist in lining up shots. The sensor locates the correct high goal and automatically turns the robot until it is directly on target. The sensor also uses the y-coordinate of the goal (along with known dimensions, such as the height of the goal) to determine how far the robot is from the goal. We use this distance in a trajectory formula to find the necessary speed of the flywheel to hit the center of the goal, and use a PID loop to set the flywheel to the correct RPM.
3. Prior to the start of a match, an on-screen visual autonomous selector determines which autonomous routine will be performed and tells the robot which team it is on, which is used for the Vision sensor goal identification.
4. A custom odometry setup lets the robot know exactly where it is on the field at all times, which is especially important during Programmer Skills. A number of functions use the odometry data to move the robot to a specific position and heading on the field.
5. A pre-match checklist on the controller screen prompts the driver to check all necessary setup processes, such as a charged battery, pressurized pneumatics, and loaded endgame routine. At the end of the match, both the R1 and L1 shoulder buttons must be pressed to launch the endgame routine, preventing accidental premature launches. 
6. All isolated processes are run asynchronously on seperate threads, which allows the robot to perform multiple tasks at once without having to wait.

## Future Plans
Unfortunately, this was the last season before graduation for five of our six team members. However, team 877K will bring on new members from other teams for the 2023-2024 season and continue competitng. Next year, we plan to switch to PROS rather than Vexcode, allowing us to write more complex and cleaner code and to take advantage of already developed tools such as OkapiLib rather than writing everything from scratch. 
