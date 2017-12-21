Choose the UDOO platform you want to use:

<div>
 <ul id="platform-examples" class="nav nav-tabs" role="tablist">
  <li role="presentation" class="active"><a href="#arm-example" aria-controls="arm" role="tab" data-toggle="tab"><b>UDOO NEO & UDOO QUAD/DUAL</b></a></li>
  <li role="presentation"><a href="#x86-example" aria-controls="x86" role="tab" data-toggle="tab"><b>UDOO X86</b></a></li>
 </ul>

 <div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="arm-example">

Install the **UDOO IoT Cloud Client** service packages for using **UDOO NEO** or **UDOO QUAD/DUAL** as a gateway in UDOO IoT Cloud.

Since the packages are available into the UDOO binary distributions repository, simply open a terminal and run the command

```bash
sudo apt update
sudo apt install -y udoo-iot-cloud-client
```

All the dependencies will be installed with the client.  

After the system is ready you can [register the Client into the UDOO IoT Cloud Server](!Client_Registration/Register_the_Client_into_the_UDOO_IoT_Cloud_Server).  

  </div>
  <div role="tabpanel" class="tab-pane" id="x86-example">

Install the **UDOO IoT Cloud Client** service packages for using **UDOO X86** as a gateway in UDOO IoT Cloud.

For now, the packages are compatible with **Ubuntu 17.10 (Artful Aardvark)** and **Ubuntu 17.04 (Zesty Zapus)**.

## Install required packages - curl - Nodejs 6.x

Install `curl` if you don't have it done already

```bash
sudo apt install -y curl
```

<span class="label label-warning">Heads up!</span> You need to have installed **Nodejs 6.x** in your distro to run the UDOO IoT Cloud Client. Nodejs 6.x is preinstalled in **Ubuntu 17.10 (Artful Aardvark)** but you need to install it in the other older distribution as **Ubuntu 17.04**.

#### Ubuntu 17.04 (Zesty Zapus)

To install the **UDOO IoT Cloud Client** in **Ubuntu 17.04** you need to install **Nodejs 6.x** with the following commands or check the [official node documentation](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions) to know how to install it:

```bash
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
sudo apt-get install -y nodejs
```

## UDOO IoT Cloud Client service and UDOO Web Conf

The UDOO IoT Cloud Client packages are available into the UDOO binary distributions repository.
You need to add the UDOO repo as source for `apt` before to install the UDOO IoT Client.

Add the UDOO repository and key

```bash
curl -s -A "Firefox" https://repository.udoo.org/gpg.key | sudo apt-key add -
echo "deb https://repository.udoo.org/ udoox86 main" | sudo tee /etc/apt/source.list.d/udoo.list
```

Now you can update the apt package list and install the **UDOO IoT Cloud Client** service and the **UDOO Web Conf**

```bash
sudo apt update
sudo apt install -y udoo-iot-cloud-client udoo-web-conf
```

The packages are now installed, you can go to the next section to [Register_the_Client_into_the_UDOO_IoT_Cloud_Server](!Client_Registration/Register_the_Client_into_the_UDOO_IoT_Cloud_Server)

  </div>
</div>
<script>
$('#platform-examples a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})
</script>
