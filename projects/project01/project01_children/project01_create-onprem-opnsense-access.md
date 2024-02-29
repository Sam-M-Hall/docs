---
layout: page
title: OPNsense - Access
parent: Create On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 4
---



# OPNSsense - Access


In this section, I will explain how to properly enable access to the OPNsense Management Dashboard via the WAN Interface.  



---



## OPNsense Getting to the Dashboard


Before proceeding with the following directions, we will need to disable the firewall rules by performing a command within the shell.  

Enter option `8`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-disable-1.png "OPNsense - Disable 1"){:.sc}  

Within the shell interface, enter `pfctl -d` to disable the firewall rules.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-disable-2.png "OPNsense - Disable 2"){:.sc}  


Navigate to the assigned WAN IP, which you can find on the main page.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-access-1.png "OPNsense - GUI Access 1"){:.sc}  

If you get this popup, click ***Advanced***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-access-2.png "OPNsense - GUI Access 2"){:.sc}  

Then click ***Continue***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-access-3.png "OPNsense - GUI Access 3"){:.sc}  

Login to the OPNsense dashboard by using the same `root` user account from earlier.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-access-4.png "OPNsense - GUI Access 4"){:.sc}  



---



## Enabling WAN Access for OPNsense


{: .warning}
If at any point you get disconnected, or think it's working, close your browser completely to terminate the session.  
If you're locked out, go back to the shell and enter `pfctl -d` to disable the firewall rules again.  


On the main dashboard, select ***Interfaces*** then ***WAN***.  
Uncheck the ***Block private networks***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-1.png "OPNsense - GUI WAN Access 1"){:.sc}  

Select the ***Firewall*** section and choose ***Rules*** then ***WAN***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-2.png "OPNsense - GUI WAN Access 2"){:.sc}  

On the banner above the rule section, click the ![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-btn-plus.png "OPNsense - GUI WAN Access - Add Rule"){:.sc} button.  

Within the firewall rule, configure the options in this section as displayed.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-3.png "OPNsense - GUI WAN Access 3"){:.sc}  

Within the firewall rule, configure the options in this section as displayed.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-4.png "OPNsense - GUI WAN Access 4"){:.sc}  

Within the firewall rule, configure the options in this section as displayed.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-5.png "OPNsense - GUI WAN Access 5"){:.sc}  

Once complete, click ![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-btn-save.png "OPNsense - GUI WAN Access - Save"){:.sc} at the bottom of the page.

Back on the ***WAN Rules*** page, we'll see a banner at the top of the page.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-banner.png "OPNsense - GUI WAN Access - banner"){:.sc}

Click ![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-gui-btn-apply.png "OPNsense - GUI WAN Access - Apply"){:.sc} to apply the newly created rule. This will restart the firewall services.  

Within the shell again, verify the firewall rules are running again by entering `pfctl -e`.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-config-disable-3.png "OPNsense - Disable 3"){:.sc}  

Close your browser completely and verify connectivity via the **WAN** interface.  



---



{: .new-title}
> On to bigger things!
>
We've successfully setup and configured our OPNsense Firewall!
Please make your way to the [next section], where we'll be setting up our first Windows Server, DC01!




[next section]: /projects/project01/project01_children/project01_create-onprem-dc01-prep