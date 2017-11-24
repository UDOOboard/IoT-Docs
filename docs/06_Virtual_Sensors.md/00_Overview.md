**Virtual Actuators** allow users to extend the UDOO IoT sensing capabilities.  
It allows to create more complex sensors and exploit the local computational power of every device.

It's possible to create local apps or scripts that perform calculations using local - sensors, internet informations, local resources - and then publish the result on the cloud as all the other sensors like lights, temperature and so on.

The UDOO IoT Client periodically reads the I2C environmental sensors values provided by linux driver. It reads the value from the device file.

A virtual sensor write the output value from a file located in a specific location.
By the Cloud it's possible to configure and enable the Client to read this specific file and get the data every time there is a new data available.

## What is a Virtual Sensor?

A Virtual Sensor is an application, written in every language, that runs on the UDOO Device (UDOO neo, Quad or Dual, x86) connected to the UDOO IoT Cloud.  
It could be developed in any language (c, java, python...) and can publish the value in a specific file.

    /sensors/__NAME_OF_THE_SENSOR__/data

### Output File

The format of the file must be:

    __FLAG__,__VALUE__

The `__FLAG__` is used to notify the client when the sensor value is changed.  
Every time the `__VALUE__` changes and have to be updated on the IoT cloud, the Virtual Sensor have to change the `__FLAG__` from `0` to `1`, or from `1` to `0`.
