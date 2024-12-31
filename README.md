# Garbage Sorting Robot Project
Variables:
distanceToWall (float)
const lengthOfBin (length of bin) (float)
distanceToBin (float) (Distance from each bin to origin)
binColor (color)
numDegrees (int)
colorFound (bool)
timeSpent (float)
shutDown (bool)
Functions:
void setSensorSetup() - initialize and calibrate sensors, zero motor encoders and gyro
Will test by using sensors in other functions
Gyro[], MotorEncoder[], Platform[], 
void giveInstructions() - ask user to put garbage on platform
Will test by viewing the message on the display
color getBinColor() - Button pushing - return color of bin
Will test by stating the colour as a message on the display to ensure the input works 
float driveToWall() - Driving to wall (returns distance to the wall)
Will test by making it drive to the wall, display the distance and measure said distance
void spinXDegrees(int numDegrees): Turning specified degrees to the bin (no parameter)
Will test by making it rotate and measuring the specified rotation degrees
void awayFromWall(int numDegrees) - Reverse and use spinXDegrees to spin away from the wall (parameter: distance to the wall) 
Will test by running the code and ensuring it moves the correct distance and turns the correct amount of degrees
bool checkBinColor(color binColor) - Bool function: Differentiating the bins (checking colour) (parameter: appropriate color) (returns true or false)
Will test through the driveToBin function
float driveToBin(color binColor) - returns distance driven to bin, uses checkBinColor function)
Will test by running the function and seeing if it stops and turns at right bin
void tipPlatform() - Tip platform spin medium motor
Will test by running the function and see if it tips the platform correctly and throws the item out
void reverse(float distanceToWall) - Reverse then turn (uses distance from wall to the bin, subtracts width from the distance to the wall of the bins (= distanceToBin) which is the distance from origin to bin or the distance the robot needs to reverse
Will test by seeing if the robot moves the correct distance back
void returnToStart(float distanceToBin, color binColor) - Driving back to the origin
Will test by seeing if the robot moves the correct distance back to the start
void displayTime(float timeSpent) - displays final timer to console
Will test through the askForFeedback function 
void askForFeedback(color binColor) - Ask for feedback and accuracy
Will test by viewing the message on the display and testing the input
Unexpected Input:
What if user presses wrong button? (double check they pushed right button)
What is user presses a button not corresponding to a colour? (no input received/error message/fail program)
What to do for unexpected environmental changes? (Place the bins and robot in a controlled environment with controlled color of ground and size of bins)
Procedure:
(main function)
Setup sensors
Ask user to put garbage on platform
Wait for button push and un-push, register button push as color (int)
Get time
Drive to wall, touch sensor sensing when wall is touched
Reverse and spin(based on distances)
Drive to colors, checking if color seen = color according to button pressed
Turn to bin
Tip platform
 Drive back to starting point
Display final time
Ask if user wants to shut down or restart

