This guide is only for the **UDOO ARM** boards (**NEO** and **QUAD/DUAL**).  

Follow this guide to update/upgrade a **UDOObuntu version previous of the 2.2.0** (e.g. 2.1.4) to make it work with the UDOO IoT Cloud system.

<span class="label label-warning">Heads up!</span> We suggest to always use the latest UDOObuntu version.

To fit the new Ubuntu authentication key guidelines, we introduced a new repository where host the UDOO packages. The new repo is already used in the UDOObuntu 2.2.0 version.  

If you are using an older UDOObuntu image you need to update your system to point to the new repository and key.  
Use this procedure:
* Open the file `/etc/apt/sources.list.d/udoo.list` with your favorite text editor, in this case vim:
```bash
sudo vim /etc/apt/sources.list.d/udoo.list
```
Change the repository address from `deb http://repository.udoo.org udoobuntu main` to the new one
```bash
deb http://repository.udoo.org/trusty udoobuntu main
```
and save.

* Add the new authentication key
```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys EA42CD5882D3D324
```

* Update the apt source and install the totally new **UDOO WebConf**
```bash
sudo apt update
sudo apt install --reinstall udoo-web-conf
```

Once you have updated the UDOObuntu OS of your UDOO ARM board you need to install the UDOO IoT Client service. Install it is service is very easy.  
Go to the [Install the UDOO Iot Client service](!Install_the_UDOO_Iot_Client_service) section to see how to do that in your UDOO NEO or UDOO QUAD/DUAL.
