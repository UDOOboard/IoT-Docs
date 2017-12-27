From this page you can add logical **Triggers** involving sensors and actuators registered in the Cloud.

You can use the IFTTT-logic (*If This Then That*) conditions to create the triggers you need in the system. This is a very useful tool to create logic actions into your Cloud

In the top of the page you can find the Triggers already created.  

<img src="../img/50_triggers_page.PNG" alt="iot_dashboard_complete" class="img-responsive" >

### Create a new Trigger

You can create two kind of Triggers:
* **Online Trigger**: Triggers involving sensors and actuators from different Gateway. Since the trigger is managed by the Cloud Server, it can works only if all the Gateways involved are connected to Internet and are able to communicate with the Server.
* **Offline Triggers**: Triggers involving sensors and actuators of the same Gateway. Since the trigger is saved in the Gateway involved, it will work also if the Gateway isn't connected to Internet.

<img src="../img/51_triggers_add_new.PNG" alt="iot_dashboard_complete" class="img-responsive" >

To create a new Trigger you need to select the **Sensor** you want to check, in the `If` sector, from the drop down menu.

Select the logic you want to set to the trigger, selecting one of the following, and set the proper value to trigger the trigger:
* **equal to**
* **greater than**
* **greater or equal than**
* **lower than**
* **lower or equal than**
* **not equal to**

In the `Then` sector you can choose using an **Actuator** or/and let the system **send an email notification** when the logic of the trigger is true.

Also for the Actuators, you can choose the behavior to be produced when the condition set is true or false.
