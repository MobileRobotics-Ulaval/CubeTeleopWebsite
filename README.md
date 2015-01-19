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
$ sudo apt-get install apache2 ros-<insert ros version(Ex:hydro)>-rosbridge-suite ros-<same here>-web-video-server

```

##Launching the website##
On two differents terminal inputs the following command line:
```shell
$ roslaunch rosbridge_server rosbridge_websocket.launch
$ rosrun mjpeg_server mjpeg_server
```
Then you need to open the index.html file in a browser (http://localhost/CubeTeleopWebsite/)

To set the video stream topic, open index.html and change the following line:
```javascript
 var NAME_OF_VIDEO_FEED_TOPIC = '/my_topic/for_in_browser/video_feed/';

```
To set the position topic output, open index.html and change the following line:
```javascript
  var NAME_OF_POSITION_TOPIC = '/cube_position_js';

```
