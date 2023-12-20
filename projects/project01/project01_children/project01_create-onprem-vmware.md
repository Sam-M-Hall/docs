---
layout: page
title: VMware Workstation Setup
parent: Create On-Prem Environment
grand_parent: On-Prem to Azure
nav_order: 1
---

## Download
You can download VMware Workstation Pro from [here](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html).

Scroll down on the page and click ***Download Now***.
![](/assets/images/projects/project01/create-on-prem/vmware-download-1.png "VMware Download")

---

## Installation Process

Run the installer and follow along with the guide below.  

On the first panel of the wizard, simply click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-1.png "VMware Install - 1")

Accept the terms if you so choose, and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-2.png "VMware Install - 2")

Ensure that both boxes on this screen are selected and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-3.png "VMware Install - 3")

Choose your preferences for the ***User Experience Settings*** panel and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-4.png "VMware Install - 4")

Choose your preferences for the ***Shortcuts*** panel and click ***Next***. 
![](/assets/images/projects/project01/create-on-prem/vmware-install-5.png "VMware Install - 5")

Click ***Install***.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-6.png "VMware Install - 6")

You'll see the installer proceed with the installation process. Wait for it to finish.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-7.png "VMware Install - 7")

If you'd like to enter a license, click the ***License*** button, if not click ***Finish***.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-8.png "VMware Install - 8")

---

## Licensing (optional)

If you have chosen to enter a license, do so on this page.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-9.png "VMware Install - 9")

Once you've entered the license, click ***Enter***.  
![](/assets/images/projects/project01/create-on-prem/vmware-install-10.png "VMware Install - 10")

---

## Initial Setup

On the initial launch of VMware Workstation Pro, we'll have to either enter a licensing key or continue without one by accepting the trial option. Click ***Continue***.  
![](/assets/images/projects/project01/create-on-prem/vmware-setup-1.png "VMware Initial - 1")

Click ***Finish***.  
![](/assets/images/projects/project01/create-on-prem/vmware-setup-2.png "VMware Initial - 2")

---

## Virtual Network Editor Config
Before we continue with creating anything within VMware Workstation, we need to perform the initial setup of our Virtual Network.  

Click on ***Edit*** on the ribbon menu, then click ***Virtual Network Editor***.  
![](/assets/images/projects/project01/create-on-prem/vmware-vnet-1.png "VMware VNet - 1")

Within the ***Virtual Network Editor***, select ![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-vnet-btn-change-settings.png "VMware VNet - Change Settings")  
![](/assets/images/projects/project01/create-on-prem/vmware-vnet-2.png "VMware VNet - 2")

For ***VMnet1*** & ***VMnet8***, select the entry in the table and click ![](/assets/images/projects/project01/create-on-prem/vmware-opnsense-vnet-btn-remove-net.png "VMware VNet - Remove Net")  
![](/assets/images/projects/project01/create-on-prem/vmware-vnet-3.png "VMware VNet - 3")

Select ***VMnet0*** and click the drop-down menu. Select the primary interface you're using on your machine. This will force all connections on this virtual interface to utilize the physical connection you've chosen, which will be used later to provide internet services to an OPNsense firewall.  
![](/assets/images/projects/project01/create-on-prem/vmware-vnet-4.png "VMware VNet - 4")

Now let's add a new interface and assign it to ***VMnet10***.  
![](/assets/images/projects/project01/create-on-prem/vmware-vnet-5.png "VMware VNet - 5")

Now, select ***Host-only*** under the ***VMnet Information*** section, this will force this network to ***ONLY*** be available on the newly created virtual interface.  

Enter the ***Subnet IP*** information you'd like to use for this virtual network and click ***OK***.  
![](/assets/images/projects/project01/create-on-prem/vmware-vnet-6.png "VMware VNet - 6")

---

{: .new-title}
> On a roll!
>
We've successfully installed VMware Workstation Pro and configured the Virtual Network.  
Please make your way to the [next section], where we'll be adding our custom domain!

[next section]: /projects/project01/project01_children/project01_create-onprem-opnsense