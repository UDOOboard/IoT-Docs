Once the UDOO IoT Cloud Client service is installed on your UDOO you can register the board as a gateway in the UDOO Cloud.  
To register the Client to the IoT Server open the WebConf(guide [here](https://www.udoo.org/docs-neo/Basic_Setup/Web_Control_Panel.html)) on the NEO with desktop, mouse and keyboard or VNC or USB Direct Connection.

</br>

<img src="../img/04_neo_webconf_dashboard.png" alt="neo_webconf_dashboard" class="img-responsive" >

</br>

Next step, is connecting the board to the net and going to the IoT System Configuration page.
For going there, click on Configuration and select **IoT Configuration** item, as shown in the figure.


<img src="../img/05_webconf_menu.png" alt="webconf_menu" class="img-responsive" >

</br>

The board will recognize as **Unregistered**.
A login form is shown to allow you insert the UDOO IoT Account credential.

</br>

<img src="../img/07_unregistered_board_alert.png" alt="unregistered_board_alert" class="img-responsive" >

</br>

Once you click the **Sign in** button an automatic registration procedure will start.
The UDOO device will be registered into the UDOO IoT Cloud and will keep the auth token to connect to the Cloud and communicate with it.

Once the registration is finished, the board will automatically connect to the UDOO IoT Server, and, when ìt’s ready, you’ll see the **Connected** string in the box.  

</br>

<img src="../img/13_board_registration_complete.png" alt="board_registration_complete" class="img-responsive" >

</br>

Now you can go directly go to the [UDOO IoT Cloud](https://udoo.cloud) page to see the device connected.
