If you have a **UDOObuntu version previous of the 2.1.4** you need to update your system and install the `udoo-iot-cloud-client` package.

Make sure the board is connected to the net via Ethernet or Wi-Fi.

Open the terminal and update the system:

    sudo apt update

Upgrade the udoo-web-conf and the linux kernel packages:

    sudo apt upgrade

Reboot the board

Install the software packages for using UDOO as a gateway in UDOO IoT

    sudo apt install udoo-iot-cloud-client

After the system is ready you can start configure the client to register to the UDOO IoT Cloud.
