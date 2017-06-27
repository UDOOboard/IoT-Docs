If you have a **UDOObuntu version previous of the 2.1.4** you need to update your system and install the `udoo-iot-cloud-client` package.

Make sure the board is connected to the net via Ethernet or Wi-Fi.

Open a terminal and update the system:
```bash
sudo apt update
```
Upgrade the system packages (last udoo-web-conf and linux kernel are needed):
```bash
sudo apt upgrade
```
Reboot the board

Install the software packages for using UDOO as a gateway in UDOO IoT
```bash
sudo apt install udoo-iot-cloud-client
```
After the system is ready you can start configure the client to register to the UDOO IoT Cloud.
