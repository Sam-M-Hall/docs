---
layout: page
title: VMware Workstation Setup
parent: Preparation
grand_parent: Hybrid Connections
nav_order: 2
---



# VMware Workstation Setup


In this section, I will guide you through the setup process for VMware Workstation.  
This will be used to host the virtual machines within our on-prem environment.  



---



## Download
You can download VMware Workstation Pro from [here](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html).  

Scroll down on the page and click ***Download Now***.
![](/assets/images/projects/project01/prepare/vmware/vmware-download-1.png "VMware Download"){:.sc}  



---



## Installation Process


Run the installer and follow along with the guide below.  

On the first panel of the wizard, simply click ***Next***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-1.png "VMware Install - 1"){:.sc}  

Accept the terms if you so choose, and click ***Next***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-2.png "VMware Install - 2"){:.sc}  

Ensure that both boxes on this screen are selected and click ***Next***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-3.png "VMware Install - 3"){:.sc}  

Choose your preferences for the ***User Experience Settings*** panel and click ***Next***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-4.png "VMware Install - 4"){:.sc}  

Choose your preferences for the ***Shortcuts*** panel and click ***Next***. 
![](/assets/images/projects/project01/prepare/vmware/vmware-install-5.png "VMware Install - 5"){:.sc}  

Click ***Install***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-6.png "VMware Install - 6"){:.sc}  

You'll see the installer proceed with the installation process. Wait for it to finish.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-7.png "VMware Install - 7"){:.sc}  

If you'd like to enter a license, click the ***License*** button, if not click ***Finish***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-8.png "VMware Install - 8"){:.sc}  



---



## Licensing (optional)


If you have chosen to enter a license, do so on this page.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-9.png "VMware Install - 9"){:.sc}  

Once you've entered the license, click ***Enter***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-install-10.png "VMware Install - 10"){:.sc}  



---



## Initial Setup


On the initial launch of VMware Workstation Pro, we'll have to either enter a licensing key or continue without one by accepting the trial option. Click ***Continue***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-setup-1.png "VMware Initial - 1"){:.sc}  

Click ***Finish***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-setup-2.png "VMware Initial - 2"){:.sc}  



---



## Virtual Network Editor Config


Before we continue with creating anything within VMware Workstation, we need to perform the initial setup of our Virtual Network.  

Click on ***Edit*** on the ribbon menu, then click ***Virtual Network Editor***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-1.png "VMware VNet - 1"){:.sc}  

Within the ***Virtual Network Editor***, select ![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-btn-change-settings.png "VMware VNet - Change Settings"){:.sc}  
![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-2.png "VMware VNet - 2"){:.sc}  

For ***VMnet1*** & ***VMnet8***, select the entry in the table and click ![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-btn-remove-net.png "VMware VNet - Remove Net"){:.sc}  
![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-3.png "VMware VNet - 3"){:.sc}  

Select ***VMnet0*** and click the drop-down menu. Select the primary interface you're using on your machine. This will force all connections on this virtual interface to utilize the physical connection you've chosen, which will be used later to provide internet services to an OPNsense firewall.  
![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-4.png "VMware VNet - 4"){:.sc}  

Now let's add a new interface and assign it to ***VMnet10***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-5.png "VMware VNet - 5"){:.sc}  

Now, select ***Host-only*** under the ***VMnet Information*** section, this will force this network to ***ONLY*** be available on the newly created virtual interface.  

Enter the ***Subnet IP*** information you'd like to use for this virtual network and click ***OK***.  
![](/assets/images/projects/project01/prepare/vmware/vmware-vnet-6.png "VMware VNet - 6"){:.sc}  



---



{: .new-title}
> On a roll!
>
We've successfully installed VMware Workstation Pro and configured the Virtual Network.  
Please make your way to the [next section], where we'll be creating our M365 environment!




[next section]: /projects/project01/project01_children/project01_create-M365