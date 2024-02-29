---
layout: page
title: OPNsense - Prepare
parent: Create On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 2
---



# OPNsense - Preparation
 

In this section, I will overview the preparation of the OPNsense Virtual Machine to be used within the on-prem environment. We will be configuring it in later sections.  



---



## Downloading the ISO


Navigate to the download page here and download the ISO for OPNsense by selecting the options displayed below. Choose whatever Mirror Location that best suits you.  
![](/assets/images/projects/project01/create-on-prem/opnsense/opnsense-download.png "OPNsense Download"){:.sc}  


{: .warning}
You will need to extract the ISO using a program that can handle zipped files, as Windows' Built-In file extractor can't properly interact with the ISO archive file.   



---



## OPNsense VM Creation


Select ***File*** in the ribbon menu and then choose ***New Virtual Machine***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-1.png "OPNsense - VM Setup 1"){:.sc}  

Accept the default of ***Typical*** and click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-2.png "OPNsense - VM Setup 2"){:.sc}  

Click ***Browse...*** and select the ISO file from earlier.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-3.png "OPNsense - VM Setup 3"){:.sc}  

Name the virtual machine whatever you want, I went with "OPNsense" to keep things simple. Now choose the storage location for *where* you want to store the Virtual Machine. Click ***Next***.  


{: .important}
When choosing a location, be sure to organize the VMs there into separate folders, as VMware Workstation Pro will drop all associated files into the folder you specify ***without*** creating an organizational folder for you.  


![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-4.png "OPNsense - VM Setup 4"){:.sc}  

Select ***Store virtual disk as a single file*** and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-5.png "OPNsense - VM Setup 5"){:.sc}  

Uncheck the ***Power on this virtual machine after creation*** option, as we will be performing more configuration after this.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-6.png "OPNsense - VM Setup 6"){:.sc}  



---



## OPNsense VM Advanced Configuration


Select the virtual machine and on its home page click ***Edit virtual machine settings***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-power-edit.png "VMware - Power/Edit"){:.sc}  

Adjust the ***Memory for this virtual machine*** setting to **1024** MB.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-2.png "OPNsense - VM Config 2"){:.sc}  

On the ***Processors*** panel, verify that both options under the ***Virtualization engine*** are checked.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-3.png "OPNsense - VM Config 3"){:.sc}  

On the ***Network Adapter*** panel, match the settings below.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-4.png "OPNsense - VM Config 4"){:.sc}  


Click the ![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-btn-add.png "OPNsense - VM Config Add"){:.sc} button underneath the panel options.  

Select ***Network Adapter*** in the ***Hardware types*** menu, then click ***Finish***.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-5.png "OPNsense - VM Config 5"){:.sc}  

Select the newly added ***Network Adapter 2*** panel entry, then configure it as below.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-6.png "OPNsense - VM Config 6"){:.sc}  

Click ***OK*** at the bottom, then go back into the settings once again. You should now see both Network Adapters reflecting the correct attributes.  
![](/assets/images/projects/project01/create-on-prem/opnsense/vmware-opnsense-config-7.png "OPNsense - VM Config 7"){:.sc}  



---



{: .new-title}
> Preparation Finished!
>
We've successfully prepared the VM for OPNsense!
Please make your way to the [next section], where we'll be initializing our OPNsense Firewall!



[next section]: /projects/project01/project01_children/project01_create-onprem-opnsense-initialize