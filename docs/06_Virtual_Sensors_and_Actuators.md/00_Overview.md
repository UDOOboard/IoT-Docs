**Virtual Sensors and Actuators** allow users to extend the UDOO IoT capabilities.  
It allows to create more complex sensors and actuators and exploit the local computational power of every device.

It's possible to create local apps or scripts that perform calculations using local sensors, internet informations, local resources, image and video processing etc., and then publish the result on the cloud as all the other sensors like lights, temperature and so on.

A virtual sensor, for example, write the output value into a file located in a specific location.
By the Cloud it's possible to configure and enable the Client to read this specific file and get the data every time there is a new data available.

## What is a Virtual Sensor?

A Virtual Sensor is an application, that runs on the UDOO Device (UDOO NEO, QUAD/DUAL, X86) connected to the UDOO IoT Cloud.  
It could be developed in any language (c, java, python...) and need to publish the value in a specific file.

    /sensors/virtual/__NAME_OF_THE_SENSOR__/data

### Input File

The format of the file must be:

    __VALUE__

Every time the `__VALUE__` changes the UDOO IoT Cloud Client is notified and upload the data in the UDOO Cloud Server.

## What is a Virtual Actuator?

A Virtual Actuator is a file e, that runs on the UDOO Device (UDOO NEO, QUAD/DUAL, X86) connected to the UDOO IoT Cloud.  
It could be developed in any language (c, java, python...) and can publish the value in a specific file.

    /sensors/virtual/__NAME_OF_THE_SENSOR__/vdata

### Output File

The format of the file written by the UDOO IoT Client is this:

    __FLAG__,__VALUE__

The UDOO IoT Client changes the `__FLAG__` from `0` to `1`, or from `1` to `0` to notify when the `__VALUE__` is updated.  

A listening program can
