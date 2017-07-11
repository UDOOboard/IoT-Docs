If you already have a **UDOObuntu** version previous of the **2.1.4** on your UDOO board you need to update your system and install the `udoo-iot-cloud-client` package.

Power up the system and use the UDOO NEO:
* as a [Lightweight Desktop PC](https://www.udoo.org/docs-neo/Getting_Started/Use_as_a_Lightweight_Desktop_PC.html) with mouse, keyboard and desktop environment, and your UDOO board
* via [VNC](https://www.udoo.org/docs-neo/Getting_Started/Use_as_a_headless_IoT_Device.html)
* via [USB direct connection](https://www.udoo.org/docs-neo/Basic_Setup/Usb_Direct_Connection.html)

Make sure the board is connected to the net via Ethernet or Wi-Fi.

Open a terminal and update the system:
```bash
sudo apt update
```
Upgrade the system packages (last udoo-web-conf and linux kernel are needed):
```bash
sudo apt upgrade
```
Reboot the board.

Now you can [install the UDOO IoT Cloud Client service](!Install_the_UDOO_Iot_Client_service) in the next section.
