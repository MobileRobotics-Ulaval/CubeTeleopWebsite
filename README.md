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
$ rosrun web_video_server web_video_server _image_transport:="compressed"
```
Then you need to open the index.html file in a browser ([http://localhost/CubeTeleopWebsite/](http://localhost/CubeTeleopWebsite/))

To set the video stream topic and is label. Open index.html and change the following line:
```javascript
  var NAMES_OF_VIDEO_FEED_TOPIC = ['/mamba/ardrone/image_raw', '/king/ardrone/image_raw'];
  var LABELS_OF_VIDEO_FEED_TOPIC = ['robot front camera', 'camera whatever'];
```
To set the ROS namespace, open index.html and change the following line:
```javascript
  var NAMESPACE = '/192_168_10_243';
```
