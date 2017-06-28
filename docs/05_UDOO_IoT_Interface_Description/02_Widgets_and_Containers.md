A **Widget** is a customizable elements you can use to set your dashboard. You can choose a sensor connected to the network to show data inside the Widget.

A **Container** is basically an element that can contains more widgets to have a clear organization of your widgets.

By clicking on the setup icon in the dashboard, you can add widgets and containers.

<img src="../img/15_iot_add_wid_con.png" alt="iot_add_wid_con" class="img-responsive" >

## Adding Widgets

After selecting `Add New Widget`, a popup will appear. Here you need to select:
* the **gateway** that contains the sensor whose data you want to view in the widget.
* the **device** that contains the sensor whose data you want to view in the widget.
* the **sensor** whose data you want to view in the widget.

<img src="../img/16_iot_add_wid.png" alt="iot_add_wid" class="img-responsive" >

So insert the other parameters:
* the **display name** you want to assign to the sensor.
* the **icon** you want to assign to the sensor.
* the **type of the widget**. It could be a *small* or *medium*.
* the **icon and widget colors** combination to give the widget a pleasant look to see.

<img src="../img/17_iot_add_wid_2.png" alt="iot_add_wid_2" class="img-responsive" >

### Widget Types

The Widget can be of two types:
* Small
* Medium

<img src="../img/18_iot_widget_types.png" alt="iot_widget_types" class="img-responsive" >

There are some Bricks that return the values of more than one sensor (e.g. The Humidity Sensor returns data from Humidity sensor and Temperature sensor).
For the Bricks that have more sensors, you can select two kind of visualizations:
* United
* Divided

If you select **United**, a widget will be created that has all the values of the Brick’s sensors, as show in the figures below

<img src="../img/20_iot_widget_united_add.png" alt="iot_widget_united_add" class="img-responsive" >
</br>
<img src="../img/21_iot_widget_united.png" alt="iot_widget_united" class="img-responsive" >

If you choose **Divided**, you can split the sensors of a Brick into different widgets.
In the figure below, is picked just the temperature sensor of the Barometer Brick.

<img src="../img/22_widget_divided_add_one.png" alt="widget_divided_add_one" class="img-responsive" >

In figure below, are picked both

<img src="../img/23_widget_divided_add_two.png" alt="widget_divided_add_two" class="img-responsive" >

## Adding Containers

For adding a container, push on the setup icon in the dashboard, and then select `Add New Container`, a popup will appear. Here you need to select:
* a name for the container
* the icon you prefer

<img src="../img/24_container_add.png" alt="container_add" class="img-responsive" >

Now you have a new container on your dashboard.

<img src="../img/25_container_empty.png" alt="container_empty" class="img-responsive" >

You can drag the small widgets into the container for having an optimal organization of the sensors.

<img src="../img/26_container_full.png" alt="container_full" class="img-responsive" >
