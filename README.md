# wallPainter
This is an app which identifies a wall given a video stream. 

# Initialisation
BeeWare is a Python library used to create cross-platform applications. It serves as an alternative to other app-building libraries such as Kivy. This app relies on beeware for cross platform compatibility.
Beeware needs to be installed on your device to run, the instructions can be found at :
https://docs.beeware.org/en/latest/tutorial/tutorial-1.html

# How to use
src > helloworld > app.py contains relevant code for the application to run. However, note that as of now, beeware does not support numpy compatibility, and hence the app will only be able to be run in developer mode. 

Navigate to the app folder helloworld, and use briefcase dev to run the application. A window should pop up. Click on "Show camera feed" and allow permissions to access the camera. A new window should then pop up, which shows the wall mask.

The wall mask can be further refined by changing canny parameters based on the environment.

## color.py
This is a file which includes the algorithm to detect the wall. It uses a canny filter for wall segmentation, then proceeds to overlay a mask on the wall. This algorithm is passed through the video stream for the masking of the wall.

## pyproject.toml
Includes a list of beeware dependencies for compatibility
