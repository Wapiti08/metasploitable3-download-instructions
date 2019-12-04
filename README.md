# metasploitable3-download-instructions
This is the instruction on how to download the metasploitable3 successfully



References include:


**Additional information**

1. Networking Setting
  > I use the bridge module to do the experiment. Then it will make sure every virtual machine can communicate with each other.     
  If I use the NAT model, all the vms will have the same IPs. I have no idea how to fix that. 
  
 (1) Restart the networking service: 
  
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

reference is(https://github.com/hashicorp/vagrant/issues/8054)

```vagrant plugin install vagrant-cucumber```

If you meet notice like that:

> --> vmware-iso: Failed creating VMware driver: Unable to initialize any driver for this platform. The errors
from each driver are shown below. Please fix at least one driver
to continue:
>* exec: "vmware": executable file not found in $PATH
>* exec: "vmware": executable file not found in $PATH
>* exec: "vmrun": executable file not found in $PATH
>* exec: "vmrun": executable file not found in $PATH

> ==> Builds finished. The artifacts of successful builds are:
--> virtualbox-iso: 'virtualbox' provider box: /home/newt/VirtualBox VMs/Metasploitable3/metasploitable3/packer/templates/../builds/windows_2008_r2_virtualbox_0.1.0.box

It means it goes well.

```vagrant up```

If you meet this error:
>There was an error while executing `VBoxManage`, a CLI used by Vagrant
>for controlling VirtualBox. The command and stderr is shown below.

>Command: ["hostonlyif", "create"]

>Stderr: 0%...
>Progress state: NS_ERROR_FAILURE
>VBoxManage: error: Failed to create the host-only adapter
>VBoxManage: error: VBoxNetAdpCtl: Error while adding new interface: failed to open /dev/vboxnetctl: No such file or directory
>VBoxManage: error: Details: code NS_ERROR_FAILURE (0x80004005), component HostNetworkInterfaceWrap, interface >IHostNetworkInterface
>VBoxManage: error: Context: "RTEXITCODE handleCreate(HandlerArg*)" at line 94 of file VBoxManageHostonly.cpp

You can follow instructions here:
[VBoxManage: error: Failed to create the host-only adapter](https://stackoverflow.com/questions/21069908/vboxmanage-error-failed-to-create-the-host-only-adapter/59177386#59177386)

