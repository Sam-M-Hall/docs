---
layout: page
title: OPNsense Setup
parent: Create On-Prem Environment
grand_parent: On-Prem to Azure
nav_order: 2
---

In this section, I will overview the entire setup process for using OPNSense as the firewall for our LAB environment. This will allow us to properly segment our network even further and provide core networking services.  


## Downloading the ISO

Navigate to the download page here and download the ISO for OPNsense by selecting the options displayed below. Choose whatever Mirror Location that best suits you.  
![](/assets/images/projects/project01/create-on-prem/opnsense-download.png "OPNsense Download")  

{: .warning}
You will need to extract the ISO using a program that can handle zipped files, as Windows' Built-In file extractor can't properly interact with the ISO archive file.   

---

## OPNsense VM Creation

Select ***File*** in the ribbon menu and then choose ***New Virtual Machine***.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-1.png "OPNsense - VM Setup 1")  

Accept the default of ***Typical*** and click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-2.png "OPNsense - VM Setup 2")  

Click ***Browse...*** and select the ISO file from earlier.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-3.png "OPNsense - VM Setup 3")  

Name the virtual machine whatever you want, I went with "OPNsense" to keep things simple. Now choose the storage location for *where* you want to store the Virtual Machine. Click ***Next***.  

{: .note}
When choosing a location, be sure to organize the VMs there into separate folders, as VMware Workstation Pro will drop all associated files into the folder you specify ***without*** creating an organizational folder for you.  

![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-4.png "OPNsense - VM Setup 4")  

Select ***Store virtual disk as a single file*** and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-5.png "OPNsense - VM Setup 5")  

Uncheck the ***Power on this virtual machine after creation*** option, as we will be performing more configuration after this.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-6.png "OPNsense - VM Setup 6")  

---

## OPNsense VM Advanced Configuration

Select the virtual machine and on its home page click ***Edit virtual machine settings***.  
![](/assets/images/projects/project01/create-on-prem/vmware-power-edit.png "VMware - Power/Edit")  

Adjust the ***Memory for this virtual machine*** setting to **1024** MB.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-2.png "OPNsense - VM Config 2")  

On the ***Processors*** panel, verify that both options under the ***Virtualization engine*** are checked.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-3.png "OPNsense - VM Config 3")  

On the ***Network Adapter*** panel, match the settings below.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-4.png "OPNsense - VM Config 4")  


Click the ![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-btn-add.png "OPNsense - VM Config Add") button underneath the panel options.  

Select ***Network Adapter*** in the ***Hardware types*** menu, then click ***Finish***.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-5.png "OPNsense - VM Config 5")  

Select the newly added ***Network Adapter 2*** panel entry, then configure it as below.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-6.png "OPNsense - VM Config 6")  

Click ***OK*** at the bottom, then go back into the settings once again. You should now see both Network Adapters reflecting the correct attributes.  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-7.png "OPNsense - VM Config 7")  

---

## OPNsense Initialization

Now that we've configured the Virtual Machine, we can start it and perform the first-time setup.  
![](/assets/images/projects/project01/create-on-prem/vmware-power-edit.png "VMware - Power/Edit")  

Once the OPNsense finishes booting up, you will see the login prompt.  

Login with the following credentials.  
**UN:** `installer`
**PW:** `opnsense`  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-1.png "OPNsense - Install 1")  

After logging in, the installation process will automatically start.  

{: .note}
The below keyboard shortcuts are used to interact with the installer.  

`↑` `↓` `←` `→`  | navigation
`Spacebar` | select an entry
`Enter` | confirm the panel and process to the next
`Tab` | toggle panel confirmation option (ie. **Select** or **Cancel**)

Choose a keymap that's appropriate for your region, or simply accept the defaults. Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-2.png "OPNsense - Install 2")  

Documentation for OPNsense states the recommended format for the partition is **ZFS**, so navigate to the ***Install (ZFS)*** entry and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-3.png "OPNsense - Install 3")  

Since we only have one disk, we'll be accepting the default ***stripe*** partitioning option for our ***ZFS Configuration***.  Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-4.png "OPNsense - Install 4")  

After choosing the filesystem and structure, we now must choose the partition connected to the Virtual Machine.  There is only one option since we only created a single drive in our original configuration. Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-5.png "OPNsense - Install 5")  

This panel is just a warning to inform you that proceeding will erase all contents of the disk, `da0` in our case, which is simply the virtual hard disk associated with this Virtual Machine. Press `Enter`
![](/assets/images/projects/project01/create-on-prem/opnsense-install-6.png "OPNsense - Install 6")  

The installer will now proceed to format the disk and perform some configuration.  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-7.png "OPNsense - Install 7")  

Once finished, we're prompted to either change the root password or simply complete the installation. I ***strongly recommend*** you change the default password to something only **YOU** know.  Press `Enter` to change the password, or navigate to ***Complete Install*** to finalize the installation.  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-8.png "OPNsense - Install 8")  

Set the password you'd like and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-9.png "OPNsense - Install 9")  

Confirm the password you entered and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-10.png "OPNsense - Install 10")  

Navigate to ***Complete Install*** and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-11.png "OPNsense - Install 11")  

You will see a banner message informing you that ***"The installation finished successfully."*** and the machine will be ***Rebooting in 5 seconds.***  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-12.png "OPNsense - Install 12")  


{: .warning} 
Be ready to interact with the Virtual Machine.  

---

## OPNsense Initial Configuration

OPNsense will start and show the splash screen, stating ***Autoboot in 5 seconds.*** so simply wait 5 seconds and **be prepared to interact with the virtual machine!**  
![](/assets/images/projects/project01/create-on-prem/opnsense-1.png "OPNsense - Initial Config 1")  

Shortly after the bootup process begins, you will see a prompt stating ***Press any key to start the manual interface assignment:*** with a count-down from 5 seconds. Press any key to begin the interface configuration.  
![](/assets/images/projects/project01/create-on-prem/opnsense-2.png "OPNsense - Initial Config 2")  

Respond to these two prompts as below with `N`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-3.png "OPNsense - Initial Config 3")  

The next prompt displays the valid interfaces identified as connected to your OPNsense VM.  
![](/assets/images/projects/project01/create-on-prem/opnsense-4.png "OPNsense - Initial Config 4")  

{: .highlight-title}
> PRO TIP
>
We can easily identify how each interface is being assigned within the OPNsense VM by looking at the advanced settings of our **Network Adapter** within the VM's Settings Panel.  
To access this, select the network adapter entry within the Settings panel, then click ![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-btn-advanced.png "VMware - VNet - Advanced")  
Here we can see the MAC Address for the interface and verify how it's being assigned within the OPNsense VM.  
***Network Adapter***  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-mac-1.png "VMware - VNet - Advanced")  
***Network Adapter 2***  
![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-mac-2.png "VMware - VNet - Advanced")  

You will be requested to enter the interface you'd like to assign to the **WAN**. In our case, it is `em0` that we previously identified as ***Network Adapter***.  
![](/assets/images/projects/project01/create-on-prem/opnsense-5.png "OPNsense - Initial Config 5")  

Set the **LAN** interface to `em1`, which we previously identified as ***Network Adapter 2***.  
![](/assets/images/projects/project01/create-on-prem/opnsense-6.png "OPNsense - Initial Config 6")  

We don't need to configure the optional interfaces, as we're only going to utilize the **LAN** and **WAN**. Press `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense-7.png "OPNsense - Initial Config 7")  

Confirm the interface assignment by entering `y`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-8.png "OPNsense - Initial Config 8")  

After assigning the interfaces, you will be brought back to the login page. Login to the `root` account.  
![](/assets/images/projects/project01/create-on-prem/opnsense-9.png "OPNsense - Initial Config 9")  

Enter option `1`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-10.png "OPNsense - Initial Config 10")  

Let's start by configuring the **LAN** interface by entering option `1`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-11.png "OPNsense - Initial Config 11")  

Enter the following information for the below prompts:  

Configure IPv4 address LAN interface via DHCP? `N`  
Enter the new LAN IPv4 address. Press ENTER for none: `10.10.100.1`  
Enter the new LAN IPv4 subnet bit count (1 to 32): `24`  
For a WAN/LAN: `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense-12.png "OPNsense - Initial Config 12")  

Enter the following information for the below prompts:  

Configure IPv6 address LAN interface WAN tracking? `N`  
Configure IPv6 address LAN interface via DHCP? `N`  
Enter the new LAN IPv6 address. Press ENTER for none: `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense-13.png "OPNsense - Initial Config 13")  

Enter the following information for the below prompts:  

Do you want to enable the DHCP server on LAN? `N`  
Do you want to change the web GUI protocol from HTTPS to HTTP? `N`  
Do you want to generate a new self-signed web GUI certificate? `Y`  
Restore web GUI access defaults? `Y`  
![](/assets/images/projects/project01/create-on-prem/opnsense-14.png "OPNsense - Initial Config 14")  

You'll now see a banner stating that you can access the web GUI via the configured LAN IP from earlier.  
![](/assets/images/projects/project01/create-on-prem/opnsense-15.png "OPNsense - Initial Config 15")  

After finalizing the LAN interface configuration, we're brought back to the main menu.  

Enter option `2`.  

Enter the following information for the below prompts:  

Enter the number of the interface to configure: `2`  
Configure IPv4 address WAN interface via DHCP? `Y`  
Configure IPv6 address WAN interface via DHCP6? `N`  
Enter the new WAN IPv6 address. Press ENTER for none: `Enter`  
![](/assets/images/projects/project01/create-on-prem/opnsense-16.png "OPNsense - Initial Config 16")  

Enter the following information for the below prompts:  

Do you want to change the web GUI protocol from HTTPS to HTTP? `N`  
Do you want to generate a new self-signed web GUI certificate? `Y`  
Restore web GUI access defaults? `Y`  
![](/assets/images/projects/project01/create-on-prem/opnsense-17.png "OPNsense - Initial Config 17")  


---

## OPNsense VM Config Cleanup

Open the settings for the Virtual Machine again and navigate to the ***CD/DVD (IDE)*** item.  
![](/assets/images/projects/project01/create-on-prem/opnsense-install-13.png "OPNsense - Install 13")  
Select it and then choose ![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-config-btn-remove.png "OPNsense - Remove Button")  

---

## OPNsense Getting to the Dashboard

Before proceeding with the following directions, we will need to disable the firewall rules by performing a command within the shell.  

Enter option `8`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-disable-1.png "OPNsense - Disable 1")  

Within the shell interface, enter `pfctl -d` to disable the firewall rules.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-disable-2.png "OPNsense - Disable 2")  


Navigate to the assigned WAN IP, which you can find on the main page.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-access-1.png "OPNsense - GUI Access 1")  

If you get this popup, click ***Advanced***.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-access-2.png "OPNsense - GUI Access 2")  

Then click ***Continue***.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-access-3.png "OPNsense - GUI Access 3")  

Login to the OPNsense dashboard by using the same `root` user account from earlier.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-access-4.png "OPNsense - GUI Access 4")  

---

## Enabling WAN Access for OPNsense

{: .warning}
If at any point you get disconnected, or think it's working, close your browser completely to terminate the session.  
If you're locked out, go back to the shell and enter `pfctl -d` to disable the firewall rules again.  


On the main dashboard, select ***Interfaces*** then ***WAN***.  
Uncheck the ***Block private networks***.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-1.png "OPNsense - GUI WAN Access 1")  

Select the ***Firewall*** section and choose ***Rules*** then ***WAN***.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-2.png "OPNsense - GUI WAN Access 2")  

On the banner above the rule section, click the ![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-btn-plus.png "OPNsense - GUI WAN Access - Add Rule") button.  

Within the firewall rule, configure the options in this section as displayed.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-3.png "OPNsense - GUI WAN Access 3")  

Within the firewall rule, configure the options in this section as displayed.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-4.png "OPNsense - GUI WAN Access 4")  

Within the firewall rule, configure the options in this section as displayed.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-5.png "OPNsense - GUI WAN Access 5")  

Once complete, click ![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-btn-save.png "OPNsense - GUI WAN Access - Save") at the bottom of the page.

Back on the ***WAN Rules*** page, we'll see a banner at the top of the page.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-banner.png "OPNsense - GUI WAN Access - banner")

Click ![](/assets/images/projects/project01/create-on-prem/opnsense-config-gui-btn-apply.png "OPNsense - GUI WAN Access - Apply") to apply the newly created rule. This will restart the firewall services.  


Within the shell again, verify the firewall rules are running again by entering `pfctl -e`.  
![](/assets/images/projects/project01/create-on-prem/opnsense-config-disable-3.png "OPNsense - Disable 3")  

Close your browser completely and verify connectivity via the **WAN** interface.  

