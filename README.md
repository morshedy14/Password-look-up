# Password-look-up
this a simple program that write some command in the CMD and catch up the result 
Python allows us to run system commands by using a function provided by the subprocess module (subprocess.run(<list of command line arguments goes here>, <specify the second argument if you want to capture the output>))
# The script is a parent process and creates a child process which runs the system command, and will only continue once the child process has completed.
# To save the contents that gets sent to the standard output stream (the terminal) we have to specify that we want to capture the output,
so we specify the second argument as capture_output = True. 
This information gets stored in the stdout attribute.
The information is stored in bytes and we need to decode it to Unicode before we use it as a String in Python.

