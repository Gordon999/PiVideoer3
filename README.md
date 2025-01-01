# PiVideoer3


A python script to continously capture Videos from Pi v1,2,3 , HQ or GS cameras , Arducam OWLSIGHT or HAWKEYE 64MP AF camera, Arducam 16MP AF camera or Waveshare imx290-83 camera, still captures triggered by motion , external trigger or manually. 
Uses Raspberry OS BULLSEYE or BOOKWORM (for BOOKWORM switch to X11 not Wayland) and Picamera2.

for arducam cameras follow their installation instructions eg. https://docs.arducam.com/Raspberry-Pi-Camera/Native-camera/64MP-Hawkeye/

The waveshare imx290-83 IR filter can be switched (camera 1 connected to gpio26,pin37, camera2 connected to gpio19,pin35) based on sunrise/sunset or set times. IR light can be controlled by gpio13,pin33 (interface required). 

Set your location and hours difference to utc time.

On a Pi5 allows switching of 2 cameras based on sunrise/sunset or set times.

It will capture videos at 25fps at 1920 x 1080, or on a GS camera 1456 x 1088.

## Screenshot

![screenshot](screenshot.jpg)

Pi v3, Arducam HAWKEYE, OWLSIGHT or 16MP cameras can be auto / manually focussed. Pi v3 also can do spot focus.

Makes individual h264s, and can make a FULL MP4 of h264s stored.

Captured stills can be viewed and the video played it comes from.

Can control focus on a pi v3camera, auto, continuous,  manual or spot. For spot click on image when in menu showing focus options.

h264s and jpegs captured in /home/《user》/Videos.  h264s can be converted to a mp4.

To install:

Install latest FULL RaspiOS based on Bullseye or Bookworm (tested with FULL 32bit and 64bit versions)

if using BOOKWORM switch to X11. sudo raspi-config, choose advanced , choose 6A X11 option, reboot.

sudo apt install python3-opencv

sudo pip3 install ephem --break-system-packages (or use venv!!)

Download PiVideoer3.py and copy to /home/《user》

Note buttons with RED text use right mouse click, others left click. Click on left or right part of button as appropriate.

