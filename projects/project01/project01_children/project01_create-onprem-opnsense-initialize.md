---
layout: page
title: OPNsense - Initialize
parent: Create On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 3
---



# OPNsense - Initialization


In this section, I will overview the initialization of the OPNsense Firewall.  



---



## OPNsense Initialization


Now that we've configured the Virtual Machine, we can start it and perform the first-time setup.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-power-edit.png "VMware - Power/Edit"){:.sc}  

Once the OPNsense finishes booting up, you will see the login prompt.  

Login with the following credentials.  
**UN:** `installer`
**PW:** `opnsense`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-1.png "OPNsense - Install 1"){:.sc}  

After logging in, the installation process will automatically start.  

{: .note}
The below keyboard shortcuts are used to interact with the installer.  

`↑` `↓` `←` `→`  | navigation
`Spacebar` | select an entry
`Enter` | confirm the panel and process to the next
`Tab` | toggle panel confirmation option (ie. **Select** or **Cancel**)

Choose a keymap that's appropriate for your region, or simply accept the defaults. Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-2.png "OPNsense - Install 2"){:.sc}  

Documentation for OPNsense states the recommended format for the partition is **ZFS**, so navigate to the ***Install (ZFS)*** entry and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-3.png "OPNsense - Install 3"){:.sc}  

Since we only have one disk, we'll be accepting the default ***stripe*** partitioning option for our ***ZFS Configuration***.  Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-4.png "OPNsense - Install 4"){:.sc}  

After choosing the filesystem and structure, we now must choose the partition connected to the Virtual Machine.  There is only one option since we only created a single drive in our original configuration. Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-5.png "OPNsense - Install 5"){:.sc}  

This panel is just a warning to inform you that proceeding will erase all contents of the disk, `da0` in our case, which is simply the virtual hard disk associated with this Virtual Machine. Press `Enter`
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-6.png "OPNsense - Install 6"){:.sc}  

The installer will now proceed to format the disk and perform some configuration.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-7.png "OPNsense - Install 7"){:.sc}  

Once finished, we're prompted to either change the root password or simply complete the installation. I ***strongly recommend*** you change the default password to something only **YOU** know.  Press `Enter` to change the password, or navigate to ***Complete Install*** to finalize the installation.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-8.png "OPNsense - Install 8"){:.sc}  

Set the password you'd like and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-9.png "OPNsense - Install 9"){:.sc}  

Confirm the password you entered and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-10.png "OPNsense - Install 10"){:.sc}  

Navigate to ***Complete Install*** and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-11.png "OPNsense - Install 11"){:.sc}  

You will see a banner message informing you that ***"The installation finished successfully."*** and the machine will be ***Rebooting in 5 seconds.***  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-12.png "OPNsense - Install 12"){:.sc}  



---



{: .important} 
Be ready to interact with the Virtual Machine after it reboots!  

## OPNsense Initial Configuration

OPNsense will start and show the splash screen, stating ***Autoboot in 5 seconds.*** so simply wait 5 seconds and **be prepared to interact with the virtual machine!**  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-1.png "OPNsense - Initial Config 1"){:.sc}  

Shortly after the bootup process begins, you will see a prompt stating ***Press any key to start the manual interface assignment:*** with a count-down from 5 seconds. Press any key to begin the interface configuration.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-2.png "OPNsense - Initial Config 2"){:.sc}  

Respond to these two prompts as below with `N`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-3.png "OPNsense - Initial Config 3"){:.sc}  

The next prompt displays the valid interfaces identified as connected to your OPNsense VM.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-4.png "OPNsense - Initial Config 4"){:.sc}  

{: .highlight-title}
> PRO TIP
>
We can easily identify how each interface is being assigned within the OPNsense VM by looking at the advanced settings of our **Network Adapter** within the VM's Settings Panel.  
To access this, select the network adapter entry within the Settings panel, then click ![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-btn-advanced.png "VMware - VNet - Advanced"){:.sc}  
Here we can see the MAC Address for the interface and verify how it's being assigned within the OPNsense VM.  
***Network Adapter***  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-mac-1.png "VMware - VNet - Advanced"){:.sc}  
***Network Adapter 2***  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-mac-2.png "VMware - VNet - Advanced"){:.sc}  

You will be requested to enter the interface you'd like to assign to the **WAN**. In our case, it is `em0` that we previously identified as ***Network Adapter***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-5.png "OPNsense - Initial Config 5"){:.sc}  

Set the **LAN** interface to `em1`, which we previously identified as ***Network Adapter 2***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-6.png "OPNsense - Initial Config 6"){:.sc}  

We don't need to configure the optional interfaces, as we're only going to utilize the **LAN** and **WAN**. Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-7.png "OPNsense - Initial Config 7"){:.sc}  

Confirm the interface assignment by entering `y`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-8.png "OPNsense - Initial Config 8"){:.sc}  

After assigning the interfaces, you will be brought back to the login page. Login to the `root` account.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-9.png "OPNsense - Initial Config 9"){:.sc}  

Enter option `1`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-10.png "OPNsense - Initial Config 10"){:.sc}  

Let's start by configuring the **LAN** interface by entering option `1`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-11.png "OPNsense - Initial Config 11"){:.sc}  

Enter the following information for the below prompts:  

Configure IPv4 address LAN interface via DHCP? `N`  
Enter the new LAN IPv4 address. Press ENTER for none: `10.10.100.1`  
Enter the new LAN IPv4 subnet bit count (1 to 32): `24`  
For a WAN/LAN: `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-12.png "OPNsense - Initial Config 12"){:.sc}  

Enter the following information for the below prompts:  

Configure IPv6 address LAN interface WAN tracking? `N`  
Configure IPv6 address LAN interface via DHCP? `N`  
Enter the new LAN IPv6 address. Press ENTER for none: `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-13.png "OPNsense - Initial Config 13"){:.sc}  

Enter the following information for the below prompts:  

Do you want to enable the DHCP server on LAN? `N`  
Do you want to change the web GUI protocol from HTTPS to HTTP? `N`  
Do you want to generate a new self-signed web GUI certificate? `Y`  
Restore web GUI access defaults? `Y`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-14.png "OPNsense - Initial Config 14"){:.sc}  

You'll now see a banner stating that you can access the web GUI via the configured LAN IP from earlier.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-15.png "OPNsense - Initial Config 15"){:.sc}  

After finalizing the LAN interface configuration, we're brought back to the main menu.  

Enter option `2`.  

Enter the following information for the below prompts:  

Enter the number of the interface to configure: `2`  
Configure IPv4 address WAN interface via DHCP? `Y`  
Configure IPv6 address WAN interface via DHCP6? `N`  
Enter the new WAN IPv6 address. Press ENTER for none: `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-16.png "OPNsense - Initial Config 16"){:.sc}  

Enter the following information for the below prompts:  

Do you want to change the web GUI protocol from HTTPS to HTTP? `N`  
Do you want to generate a new self-signed web GUI certificate? `Y`  
Restore web GUI access defaults? `Y`  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-17.png "OPNsense - Initial Config 17"){:.sc}  



---



## OPNsense VM Config Cleanup


Open the settings for the Virtual Machine again and navigate to the ***CD/DVD (IDE)*** item.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-install-13.png "OPNsense - Install 13"){:.sc}  
Select it and then choose ![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-btn-remove.png "OPNsense - Remove Button"){:.sc}  



---



{: .new-title}
> Initialtization Finished!
>
We've successfully initialized our OPNsense Firewall!
Please make your way to the [next section], where we'll be configuring access to our OPNsense Firewall!



[next section]: /projects/project01/project01_children/project01_create-onprem-opnsense-access