# Pi_Eyes

Added eyes_udp.py to listen on port 31337 for new x, y coordinates replacing the joystick analog input. This is useful if you'd like to control the x, y values of the eyes using something other than a directly connected joystick. Values are between 0 and 1649 for both x and y axis (unmodified from analog input values) and a value of -1 for either x or y will reset the eyes to auto mode. May get around to replacing GPIO wink/blink as well. 

Example:

A UDP datagram containing "100 100\n" will set the x and y coordinates of the eyes to 100, 100.
A UDP datagram containing "-1 -1\n" will set the eyes back into auto mode.
