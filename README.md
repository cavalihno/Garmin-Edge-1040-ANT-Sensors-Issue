
# Garmin-Edge-1040-ANT-Sensors-Issue

Garmin Edge 1040 problem description regarding disconnection of sensors connected in ANT+ protocol.

Below is a description of the ANT+ connectivity problem of the new Garmin devices (Edge 1040, Edge 840, Fenix 7, Forerunner 955 and possible other devices) with power meters.

# Test 1

Facts:
    
    1. the test used the INPEAK POWERCRANK V3 power meter fw. version 3.15
    2. the same power meter was used for the test (same electronics, same software version). 
    3. garmin Edge 1040 fw. verison 16.13
    4. Garmin Edge 520 Plus fw. version 5.70

Actions:

    The sensor has ANT+ ID number "38980"
    1. attempt to add power measurement to Edge 520 Plus and Edge 1040 
    2. observing the stability of the connection 
    3. attempting to read the sensor data
    4. attempting to perform zero offset calibration
    
    Sensor has changed ANT+ ID number "34835"
    5. attempting to add power measurement to Edge 520 Plus and Edge 1040 
    6. observing the stability of the connection 
    7. attempting to read the sensor data
    8. attempting to perform zero offset calibration

Conclusions, according to the action number:
    
    1. Edge 520 finds power meter ANT+ ID "38980", Edge 1040 finds power meter ANT+ ID "38980" but takes much longer 
    2. Edge 520 maintains a stable connection with ANT+ ID "38980", Edge 1040 connects, and after a while breaks the connection, the situation repeats periodically with ANT+ ID "38980"
    3. Edge 520 reads serial number, software version, battery status, ANT+ sensor manufacturer, Edge 1040 does not read serial number, software version, battery status, sensor manufacturer 
    4. the Edge 520 calls the calibration of the sensor ANT+ ID "38980" and returns success with the value "0", Edge 1040 calls the calibration of the sensor ANT+ ID "38980" but it takes a very long time and ends with an error each time 


Below you will find a video showing the problem with ANT+ ID "38980":

<a href="https://www.dropbox.com/s/0glv9oq6ury0g5t/VID20230116152940.mp4?dl=0"><img src=images/scrsht_1.png></a>
    

    5. Edge 520 finds ANT+ power meter ID "34835", Edge 1040 finds ANT+ power meter ID "34835"
    6. Edge 520 maintains stable connection with ANT+ ID "34835", Edge 1040 maintains stable connection with ANT+ ID "34835"
    7. Edge 520 reads serial number, software version, battery status, ANT+ sensor manufacturer, Edge 1040 reads serial number, software version, battery status, ANT+ sensor manufacturer
    8. the Edge 520 calls the calibration of the ANT+ sensor ID "34835" and it returns success with the value "0", the Edge 1040 calls the calibration of the ANT+ sensor ID "34835" and it returns success with the value "0"

    
Below you will find a video showing that the problem does not occur (ANT+ ID "34835"):
<a href="https://www.dropbox.com/s/ney4zsucbjsupgp/VID20230116152536.mp4?dl=0"><img src=images/scrsht_2.png></a>

