---
layout: page
title: GPO - Mapped Drives
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 12
---



{: .note}
We'll be using the ***AD DS*** MMC Profile for this section. 


## Mapping a Network Drive via GPO


Expand the Group Policy Management tree until you can see the items within ***mydomain.local***.  

Expand then right-click ***Group Policy Objects***.  

Select ***New***  
![](/assets/images/projects/project01/configure-on-prem/GPO/gpo-1.png "GPO - Mapped Drives - 1"){:.sc}  

Name the GPO ***U_NetworkDrives***.  
![](/assets/images/projects/project01/configure-on-prem/GPO/gpo-2.png "GPO - Mapped Drives - 2"){:.sc}  

Right-click the newly created GPO and click ***Edit...***  
![](/assets/images/projects/project01/configure-on-prem/GPO/gpo-3.png "GPO - Mapped Drives - 3"){:.sc}  

Navigate through the ***User Configuration*** tree.  

***Preferences*** > ***Windows Settings*** and select ***Drive Maps***.  

Right-click the open space and select ***New*** > ***Mapped Drive***  
![](/assets/images/projects/project01/configure-on-prem/GPO/gpo-4.png "GPO - Mapped Drives - 4"){:.sc}  


The ***New Drive Properties*** pane will appear.  

Enter the ***Location*** as the UNC Path to your created share.  

Configure the remaining options to mirror the config below.  
![](/assets/images/projects/project01/configure-on-prem/GPO/gpo-5.png "GPO - Mapped Drives - 5"){:.sc}  

Select the ***Common*** tab and mirror the configuration below.  
![](/assets/images/projects/project01/configure-on-prem/GPO/gpo-6.png "GPO - Mapped Drives - 6"){:.sc}  



---



## Associating the GPO with an OU

Expand ***Accounts*** > ***Users***


Within the ***Users*** OU, right-click the ***Users/Users*** OU and select ***Link and existing GPO***.  

Double-click the newly created GPO ***U_NetworkDrives***.  
![](/assets/images/projects/project01/configure-on-prem/GPO/gpo-7.png "GPO - Mapped Drives - 7"){:.sc}  



---



{: .important-title}
> THE END
>
> Congratulations, you've reached the end for now!  
> Thanks for reading through the documentation!  
> --- 02 FEB 2024
