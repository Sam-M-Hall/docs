---
layout: page
title: General - MMC
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 1
---



# What is MMC?

***Microsoft Management Console*** provides a centralized location to interact with Windows Administrative Tools.  



---



## Creating Initial MMC Profiles


To launch ***MMC***, open ***Run*** by pressing `WIN` + `R` together, type in `mmc` and press `Enter`.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-run.png "General - MMC - Run"){:.sc}  

At the first launch, we will see an empty console.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-1.png "General - MMC - 1"){:.sc}  

Click ***File*** > ***Add/Remove Snap-in...*** to open the ***Add or Remove Snap-ins*** wizard.    
![](/assets/images/projects/project01/configure-on-prem/general/mmc-file-menu-1.png "General - MMC - File Menu"){:.sc}  

There are dozens of ***Available snap-ins*** on the left and an empty ***Selected snap-ins*** tree on the right.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-2.png "General - MMC - 2"){:.sc}  



---



## AD DS Profile


Let's start with creating a profile to manage all of our basic ***AD DS*** snap-ins.  

Click ***OK*** once satisfied with your selections.  

{: .note}
When adding the ***Event Viewer*** snap-in, you will get a ***Select computer*** popup.  
Click ***OK*** to accept the default of ***Local Computer***.  

![](/assets/images/projects/project01/configure-on-prem/general/mmc-3.png "General - MMC - 3"){:.sc}  

Click ***File*** > ***Save As...*** to save the profile.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-file-menu-2.png "General - MMC - File Menu"){:.sc}  

Once the ***Save As*** window appears, choose the ***Desktop*** folder, enter the name of the profile ***AD DS*** and hit `Enter` or click ***Save***.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-4.png "General - MMC - 4"){:.sc}  



---



## Local Profile


This profile will allow us to manage some basic local resources on the server.  


{: .important-title}
> Read before continuing!
>
> When selecting some snap-ins, they require you to to select a source.  
> For the following MMC Console, we will be managing the ***Local Computer***!  
> 
> Example for ***Certificates*** Snap-In.  
> ![](/assets/images/projects/project01/configure-on-prem/general/mmc-certificates.png "General - MMC - Certificates"){:.sc}  
> 
> Example for ***Computer Management*** Snap-In.  
> ![](/assets/images/projects/project01/configure-on-prem/general/mmc-select-computer.png "General - MMC - Select Computer"){:.sc}  


Add the snap-ins you'd like to have for this profile, then select ***OK*** and save the profile.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-5.png "General - MMC - 5"){:.sc}  



---



## Role Profile


This profile will allow us to manage the installed roles on the server.  


Add the snap-ins related to the installed roles, then select ***OK*** and save the profile.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-5.png "General - MMC - 5"){:.sc}  



---


## Quick Review

Once all profiles are set up and saved, they should all be available for you to quickly launch them from your desktop!  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-7.png "General - MMC - 7"){:.sc}  


{: .warning}
You will receive a popup when accessing MMC consoles through non-built-in administrator accounts, as MMC requires elevation.  
![](/assets/images/projects/project01/configure-on-prem/general/mmc-uac.png "General - MMC - UAC"){:.sc}  

---



{: .new-title}
> Efficiency Acheived!
>
We've successfully configured some MMC profiles to more effectively manage resources across the environment!  
Please make your way to the [next section], where we'll be enabling the AD DS - Recycle Bin!  



[next section]: /projects/project01/project01_children/project01_configure-onprem-recycle