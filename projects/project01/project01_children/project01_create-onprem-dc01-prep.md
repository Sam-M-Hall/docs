---
layout: page
title: DC01 - Prepare
parent: Create On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 5
---



# DC01 - Preparation


In this section, I will overview the preparation of the DC01 Virtual Machine to be used within the on-prem environment. We will be configuring it in later sections.


{: .highlight-title}
> PRO TIP
>
*'DC'* means *'Domain Controller'*



---



## Download Windows Server 2022 ISO


Navigate to the [Microsoft Evaluation Center] page for Windows Server 2022 and click the appropriate download link that meets your localization preferences.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/WS2022-download-1.png "DC01 - ISO Download"){:.sc}  


{: .important}
Remember where you're saving this as we'll be using it in the next step.  



---



## Virtual Machine Creation


Diving right in, let's create the virtual machine for our first Windows Server, DC01!  

In the top left of VMware Workstation, click ***File*** > ***New Virtual Machine...*** to enter the wizard.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-1.png "DC01 - VMware - 1"){:.sc}  

Accept the default configuration type of, ***Typical (recommended)***, and select ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-2.png "DC01 - VMware - 2"){:.sc}  

Next, choose ***I will install the operating system later.*** radio button and select ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-3.png "DC01 - VMware - 3"){:.sc}  

Now choose the ***Microsoft Windows*** radio button and select ***Windows Server 2022*** in the drop-down menu.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-4.png "DC01 - VMware - 4"){:.sc}  

Let's name our virtual machine and set the location.  


{: .important}
When choosing a location, be sure to organize the VMs there into separate folders, as VMware Workstation Pro will drop all associated files into the folder you specify ***without*** creating an organizational folder for you.  


![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-5.png "DC01 - VMware - 5"){:.sc}  

Specify the disk capacity to be 64GB and the ***Store virtual disk as a single file*** radio button.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-6.png "DC01 - VMware - 6"){:.sc}  

Now, let's customize the hardware associated with our VM before creation.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-7.png "DC01 - VMware - 7"){:.sc}  

Set the memory to 4GB by selecting ***Memory***, clicking **4GB** on the selector and verifying it's ***4096 MB*** in the numerical assignment field.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-8.png "DC01 - VMware - 8"){:.sc}  

Set the processors to within reason as compared to the maximum logical processors for your PC.  


{: .highlight-title}
> PRO TIP
>
You can find this info by simply pressing `WIN` + `R` to open ***Run*** and typing `msinfo32` and pressing `Enter`.  
![](/assets/images/projects/project01/create-on-prem/dc01/sys-info-1.png "DC01 - Sys-Info - 1"){:.sc}  
Look for the line that says ***Processor***, at the end it states ***X Logical Processors***.  
![](/assets/images/projects/project01/create-on-prem/dc01/sys-info-2.png "DC01 - Sys-Info - 2"){:.sc}  


Select ***Processors***, then select the number of ***physical CPU sockets*** for ***Number of processors*** you'd like to assign to DC01.  

{: .note}
**One is fine**, but Windows Server 2022 can handle up to 64 sockets, so you can play around with this setting as you see fit.  

Select the number of ***logical CPU cores*** you'd like to assign. I went with **4** for now.  


{: .warning}
Don't assign all your resources to one VM! Leave resources for your host machine and other VMs!  


Lastly, verify both boxes under the ***Virtualization engine*** section are selected.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-9.png "DC01 - VMware - 9"){:.sc}  

Up next, let's add our installation disk. Select ***New CD/DVD (SATA)*** then click the ***Use ISO image file:*** radio button and browse to the previously downloaded Windows Server 2022 ISO from Microsoft.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-10.png "DC01 - VMware - 10"){:.sc}  

For the final step, assign ***VMnet10*** to the ***Network Adapter***. Select ***Network Adapter***, choose the ***Custom: Specific virtual network*** radio button and lastly choose ***VMnet10*** from the drop-down menu.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/vmware-dc01-11.png "DC01 - VMware - 11"){:.sc}  



---



## Installation of Windows Server 2022


{: .important} 
Be ready to interact with the Virtual Machine after it boots!  
Make sure you ***click into the VM*** after powering it on!  


Alright, let's start the installation of Windows Server! Simply power on the Virtual Machine and press any key to initiate the boot from the ISO we have attached. 
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-1.png "DC01 - Install - 1"){:.sc}  

Once the ISO loads, we're met with the localization page for the installer. Select whatever preferences you desire and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-2.png "DC01 - Install - 2"){:.sc}  

On the following page, simply click 
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-3.png "DC01 - Install - 3"){:.sc}  

I'll be choosing ***Standard Evaluation (Desktop Experience)*** as my OS version. Make your selection and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-4.png "DC01 - Install - 4"){:.sc}  

Review the ***Applicable notices and license terms*** page, check the box at the bottom if you decide to accept, and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-5.png "DC01 - Install - 5"){:.sc}  

Select ***Custom***.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-6.png "DC01 - Install - 6"){:.sc}  

Since we don't have more than one disk available for our Virtual Machine, select ***Drive 0*** and click ***Next***.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-7.png "DC01 - Install - 7"){:.sc}  

Patiently wait for the installation process to finish. The system will automatically reboot once complete.  
![](/assets/images/projects/project01/create-on-prem/dc01/setup/dc01-install-8.png "DC01 - Install - 8"){:.sc}   



---



{: .new-title}
> Preparation Finished!
>
We've successfully prepared the VM for DC01!
Please make your way to the [next section], where we'll be initializing DC01!



[next section]: /projects/project01/project01_children/project01_create-onprem-dc01-initialize

[Microsoft Evaluation Center]: https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022