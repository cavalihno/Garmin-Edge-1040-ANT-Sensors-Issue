
# Garmin-Edge-1040-ANT-Sensors-Issue

Garmin Edge 1040 problem description regarding disconnection of sensors connected in ANT+ protocol.

Below is a description of the ANT+ connectivity problem of the new Garmin devices (Edge 1040, Edge 840, Fenix 7, Forerunner 955 and possible other devices) with power meters.

# Test 1

Facts:
    
    1. the test used INPEAK POWERCRANK V3 fw power measurement. version 3.15
    2. one copy of the power meter for the test (same electronics, unchanged software). 
    3. garmin Edge 1040 fw. verison 16.13
    4. Garmin Edge 520 Plus fw. version 5.70

Activities:

    The sensor is assigned ANT+ ID number "11101"
    1. attempt to add power measurement to Edge 520 and Edge 1040 
    2. observing the stability of the connection 
    3. attempting to read the sensor data
    4. attempting to perform zero offset calibration
    
    Sensor sensor was renumbered ANT+ ID "45264"
    5. attempting to add power measurement to Edge 520 and Edge 1040 
    6. observing the stability of the connection 
    7. attempting to read the sensor data
    8. attempting to perform zero offset calibration

Conclusions, according to the action number:
    
    1. Edge 520 finds power measurement ANT+ ID "11101", Edge 1040 finds power measurement but takes much longer 
    2. Edge 520 maintains a stable connection with ANT+ ID "11101", Edge 1040 connects, and after a while breaks the connection, the situation repeats periodically
    3. Edge 520 reads serial number, software version, battery status, ANT+ sensor manufacturer ID "11101", Edge 1040 does not read serial number, software version, battery status, sensor manufacturer 
    4. the Edge 520 calls the calibration of the sensor ANT+ ID "11101" and returns success with the value "0", Edge 1040 calls the calibration of the sensor ANT+ ID "11101" but it takes a very long time and ends with an error each time 

    5. the Edge 520 finds ANT+ power measurement ID "45264", Edge 1040 finds ANT+ power measurement ID "45264"
    6. Edge 520 maintains stable connection with ANT+ ID "45264", Edge 1040 maintains stable connection with ANT+ ID "45264"
    7. Edge 520 reads serial number, software version, battery status, ANT+ sensor manufacturer ID "45264", Edge 1040 reads serial number, software version, battery status, ANT+ sensor manufacturer ID "45264"
    8. the Edge 520 calls the calibration of the ANT+ sensor ID "45264" and it returns success with the value "0", the Edge 1040 calls the calibration of the ANT+ sensor ID "45264" and it returns success with the value "0"

<a href="https://www.dropbox.com/s/0glv9oq6ury0g5t/VID20230116152940.mp4?dl=0"><img src=images/scrsht_1.png></a>
    

# Test 2
