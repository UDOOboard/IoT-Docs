To make the UDOO IoT Client service work on your UDOO board you need the `udoo-iot-cloud-client` package installed on your system.  
The package is available for both ARM or x86 architecture so it can run on UDOO ARM-based boards and UDOO x86-based boards.
This package provides the service and all what you need to make your UDOO board communicate with the UDOO IoT Cloud Server.

## Prepare the IoT Client

Check the right section accordingly with the boad you want to register in the UDOO IoT Cloud.

<div>
 <ul id="intro-examples" class="nav nav-tabs" role="tablist">
  <li role="presentation" class="active"><a href="#arm-example" aria-controls="arm" role="tab" data-toggle="tab"><b>UDOO ARM/based board (UDOO NEO & UDOO QUAD/DUAL)</b></a></li>
  <li role="presentation"><a href="#x86-example" aria-controls="x86" role="tab" data-toggle="tab"><b>UDOO X86 board</b></a></li>
 </ul>

 <div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="arm-example">

First of all you need a microSD with the **UDOObuntu OS** installed, version **2.2.0** and above (a version of UDOObuntu previous of the 2.2.0 could not work with the UDOO IoT Cloud system even if updated/upgraded).  

If you haven't a microSD with UDOObuntu yet, go to one of these pages to know how to download and flash the last version of UDOObuntu (at least **2.2.0**) on a microSD:
* **UDOO NEO**: [Get Started with UDOO NEO](https://www.udoo.org/get-started-neo/)
* **UDOO QUAD/DUAL**: [Get Started with UDOO QUAD/DUAL](https://www.udoo.org/get-started-quaddual/)

<span class="label label-warning">Heads up!</span> You can consider to install the *minimal* version of UDOObuntu to have a minimal lightweight system. You can find the *minimal* versions in the [Donwload images](https://www.udoo.org/downloads/) section of the UDOO Website.

  </div>
  <div role="tabpanel" class="tab-pane" id="x86-example">

You need to run a Linux distro to install the UDOO IoT Client.  
For now, the packages are compatible with **Ubuntu 17.10 (Artful Aardvark)** and **Ubuntu 17.04 (Zesty Zapus)**.
If you haven't an OS installed on one of the drive supported by the UDOO X86 go to the [Get Started with UDOO X86](https://www.udoo.org/get-started-x86/) page and install an Ubuntu distro supported.

  </div>
 </div>
<script>
$('#intro-examples a').click(function (e) {
  e.preventDefault()
  $(this).tab('show')
})
</script>

## Install the UDOO IoT Client service

Once you have a proper OS in your UDOO board you need to install the UDOO IoT Client service. Install it is service is very easy.  
Go to the [Install the UDOO Iot Client service](!Install_the_UDOO_Iot_Client_service) section to see how to do that in your UDOO NEO, QUAD/DUAL or X86 board.
