# metasploitable3-download-instructions
This is the instruction on how to download the metasploitable3 successfully



References include:


**Additional information**

1. Networking Setting
  > I use the bridge module to do the experiment. Then it will make sure every virtual machine can communicate with each other.     
  If I use the NAT model, all the vms will have the same IPs. I have no idea how to fix that. 
  
 **(1) Restart the networking service: **
  
   default the system uses the eth0 network adapter
    
   shut the default network adapter down first
    ```  ifdown eth0 ```
   restart the apapter
    ```  ifup etho0 ```
   or:
   restart the networking service
    ``` sudo /etc/init.d/networking restart ```
  

If you meet problem like that:

>Unable to resolve dependency: user requested 'vagrant-share (> 0)'

```vagrant plugin install vagrant-cucumber```

If you meet notice like that:

> --> vmware-iso: Failed creating VMware driver: Unable to initialize any driver for this platform. The errors
from each driver are shown below. Please fix at least one driver
to continue:
* exec: "vmware": executable file not found in $PATH
* exec: "vmware": executable file not found in $PATH
* exec: "vmrun": executable file not found in $PATH
* exec: "vmrun": executable file not found in $PATH

> ==> Builds finished. The artifacts of successful builds are:
--> virtualbox-iso: 'virtualbox' provider box: /home/newt/VirtualBox VMs/Metasploitable3/metasploitable3/packer/templates/../builds/windows_2008_r2_virtualbox_0.1.0.box

It means it goes well.
