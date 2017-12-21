**Virtual Sensors and Actuators** allow users to extend the UDOO IoT capabilities.  
It allows to create more complex sensors and actuators and exploit the local computational power of every device.

It's possible to create local apps or scripts that perform calculations using local sensors, internet informations, local resources, image and video processing etc., and then publish the result on the cloud as all the other sensors like lights, temperature and so on.

A virtual sensor, for example, write the output value into a file located in a specific location.
By the Cloud it's possible to configure and enable the Client to read this specific file and get the data every time there is a new data available.

## What is a Virtual Sensor?

A Virtual Sensor is an application, that runs on the UDOO Device (UDOO NEO, QUAD/DUAL, X86) Gateway connected to the UDOO IoT Cloud.  

For example, imagine to have a camera connected on you gateway client UDOO board. From the camera you can analyze photo picked by the camera to recognize how old is a person in the photo with OpenCV. The recognition software can write the return of his photo analysis in a file to upload the data on the UDOO Cloud and see it as a sensor. A Virtual Sensor actually.  
Or imagine to collect the data of another remote sensor in the UDOO board client. You can send all the data collected to the UDOO Cloud to use the available infrastructure and check the data by the Cloud. 

It could be developed in any language (c, java, python...) and need to publish values in a specific file in the system.

    /sensors/virtual/__NAME_OF_THE_SENSOR__/data

### Input File

The format of the file must be:

    __VALUE__

Every time the `__VALUE__` changes the UDOO IoT Cloud Client is notified and upload the new data in the UDOO Cloud Server.

## What is a Virtual Actuator?

A Virtual Actuator is a file in a specific path of the system. The UDOO IoT Cloud Client changes the values written inside the file using it as Virtual Actuator set up by the Cloud.  

    /sensors/virtual/__NAME_OF_THE_SENSOR__/vdata

### Output File

The format of the file written by the UDOO IoT Client is this:

    __FLAG__,__VALUE__

The UDOO IoT Client changes the `__FLAG__` from `0` to `1`, or from `1` to `0` to notify when the `__VALUE__` is updated.  

Any software, written in any languages, running in the client, can read the file of the Virtual Actuator to react to the changes sent by the Cloud.
