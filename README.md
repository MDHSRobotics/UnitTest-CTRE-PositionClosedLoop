UnitTest-CTRE-PositionClosedLoop

# Summary
Example demonstrating the Position closed-loop servo with TalonSRX speed controller

## User Interaction
  Button 1 - Enters Closed Loop Position mode; the target position is proportional to the
             value of the Y-axis of the joystick when button 1 is pressed
  Button 2 - Drives the motor with power percentage based on the Y-axis of the joystick
             when button 2 is pressed

See the comments in robot.java for more details.

## Feedback
  		RoboRio Log - prints the motor output % and the current error (if in closed loop)
  
  		SmartDashboard - Displays motor output, current error, and PID constants
  						 Note: it is preferable to display the error widget as a graph

## PID Tuning
  Tweak the PID gains accordingly. This can be done by:
     1. Changing the values in the calls below to talon.config_kP, talon.config_kI, and talon.config_kD
     2. Use the roboRIO web-based configuration tool to quickly change the gains on the fly
        without having to re-deploy the code.