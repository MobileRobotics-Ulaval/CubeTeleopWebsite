Cube Teleoperation Website
==============================
Reception of live camera steam and teleoperation of the flying cubes via a website interface.


#Installation#
##Cloning the git repertory##
Go to the localhost repertory (by default "/var/www") and clone the website's page:
```shell
$ cd /var/www
$ git clone  https://github.com/MobileRobotics-Ulaval/CubeTeleopWebsite
```

##Installation of ROSlibjs##
```shell
$ sudo apt-get install ros-<insert ros version(Ex:hydro)>-rosbridge-suite ros-hydro-web-video-server

```

##Launching the website##
```shell
$ roslaunch rosbridge_server rosbridge_websocket.launch
$ rosrun mjpeg_server mjpeg_server
```
Then you need to open the html file in a browser (http://localhost/CubeTeleopWebsite/)
