# MRP-2000_rtk_gps_driver

## Hardware Setting
1. Give power MRP-2000 with micro-5pin
1. Connect USB serial port and GNSS & LTE antenas
2. Check that all of LEDs are properly turned on (red LED is blinking)

## Ros Setting
1. Copy all of folders to ~/catkin_ws/src
2. Build with $catkin_make
3. Give permission:

  cd ~/catkin_ws/src/nmea_gps_driver/scripts

  sudo chmod +x nmea_gps_driver.py

  sudo chmod +777 /dev/ttyUSB0

4. Run node:

  roscore
  
  rosrun nmea_gps_driver nmea_gps_driver.py _port:=/dev/ttyUSB0 _baud:=115200

5. Visualization:

  roslaunch rviz_satellite demo.launch
