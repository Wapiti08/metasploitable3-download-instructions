# metasploitable3-download-instructions
This is the instruction on how to download the metasploitable3 successfully



References include:

``` code ```
**Additional information**

1. Network Setting
  > I use the bridge module to do the experiment. Then it will make sure every virtual machine can communicate with each other.     
  *If I use the NAT model, all the vms will have the same IPs. I have no idea how to fix that.* 
  
  **(1) Restart the networking service: **
  
    default the system uses the eth0 network adapter
    shut the default network adapter down first
    ```  ifdown eth0 ```
    restart the apapter
    ```  ifup etho0 ```
    or:
    restart the networking service
    ``` sudo /etc/init.d/networking restart ```
  



```vagrant plugin install vagrant-cucumber```


