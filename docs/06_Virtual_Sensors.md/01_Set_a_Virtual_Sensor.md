Following the next steps to create and work with a Virtual Sensor.

### On the client

Create a folder in `/sensors/virtual/` with the name of the virtual sensor yo would create.  
You should use the same name to configure in the next step the IoT cloud.

```bash
mkdir /sensors/virtual/__NAME_OF_THE_SENSOR__/
touch /sensors/virtual/__NAME_OF_THE_SENSOR__/data
```

In this example we'll call the the Virtual Sensor `vstest`:

```bash

mkdir /sensors/virtual/vstest/
touch /sensors/virtual/vstest/data
```

The `data` file must be accessible both by the application that changes values and by the UDOO IoT Client so in this example we change the permissions in this way:

```bash
chmod 666 /sensors/virtual/vstest/data
```

### On the server

Select the gateway and choose the UDOO device.

<img src="../img/vsensor_device.PNG" alt="vsensor_device" class="img-responsive" >

Press on the **New Sensor** drop down menu (not the button) and choose **Virtual**.

<img src="../img/vsensor_new_sensor.PNG" alt="vsensor_new_sensor" class="img-responsive" >

Enter the `__NAME_OF_THE_SENSOR__` as the folder created on the client.  
Enter the **display name** and choose an **icon** to be displayed in the widget, whatever.  
Select an **update time**, because the sensor value will be updated only when the value change.  
Select **online notification**.  
**Value types** provides a description of the sensor and the measure unit if desired.  
Press the **Save** button to save the configuration.

<img src="../img/vsensor_new_sensor_popup.PNG" alt="vsensor_new_sensor_popup" class="img-responsive" >

The Virtual Sensor is shown now in a widget and come DISABLED by default.  
Enable the Virtual Sensor by press the **Enable** button in the 3-dot menu.

<img src="../img/vsensor_widget_disabled.PNG" alt="vsensor_widget_disabled" class="img-responsive" >
</br>
<img src="../img/vsensor_widget_enabled.PNG" alt="vsensor_widget_enabled" class="img-responsive" >

Restart the UDOO IoT Client Service using the button **Restart Service** in the 3-dot menu of the device in top of the page.

<img src="../img/vsensor_restart_service.PNG" alt="vsensor_restart_service" class="img-responsive" >

Now the Virtual Service is up and running listening to the changes in the `data` file.
