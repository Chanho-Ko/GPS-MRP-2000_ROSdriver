cd ~/catkin_ws/src/nmea_gps_driver/scripts
sudo chmod +x nmea_gps_driver.py
sudo chmod +777 /dev/ttyUSB0

rosrun nmea_gps_driver nmea_gps_driver.py _port:=/dev/ttyUSB0 _baud:=115200

roslaunch rviz_satellite demo.launch
