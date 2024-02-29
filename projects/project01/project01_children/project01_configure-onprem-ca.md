---
layout: page
title: AD CS - Certificate Authority
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 4
---



# Continuing from our installation!


{: .important}
Reference [DC01 - Roles - Certificate Authority] as needed to refamiliarize yourself with this role's installation.  



---



## Initial Configuration


Within Server Manager, click the Flag icon to view Task notifications.  

Click the ***Configure Active Directory Certificate Services*** hyperlink.  
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-sm.png "AD DS - CA - SM"){:.sc}  

Within the ***AD CS Configuration*** Wizard follow the prompts as guided below.  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-1.png "AD DS - CA - 1"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-2.png "AD DS - CA - 2"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-3.png "AD DS - CA - 3"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-4.png "AD DS - CA - 4"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-5.png "AD DS - CA - 5"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-6.png "AD DS - CA - 6"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-7.png "AD DS - CA - 7"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-8.png "AD DS - CA - 8"){:.sc}  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-9.png "AD DS - CA - 9"){:.sc}  

Click ***Configure***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-10.png "AD DS - CA - 10"){:.sc}  

Click ***Close***
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-11.png "AD DS - CA - 11"){:.sc}  



---


## Verifying the Certificate Authority Status

{: .warning-title}
***Reboot the server.***  

Within the ***Roles*** MMC Console, navigate to the ***Certificate Authority*** Snap-in.  

Expand the menu tree as displayed below and verify the Certificate for DC01 exists.  
![](/assets/images/projects/project01/configure-on-prem/AD/ca-setup-12.png "AD DS - CA - 12"){:.sc}  



---



{: .new-title}
> Authority Established!
>
We've successfully configured the AD DS - Certificate Authority!  
Please make your way to the [next section], where we'll be creating Organizational Units!



[next section]: /projects/project01/project01_children/project01_configure-onprem-ou
[DC01 - Roles - Certificate Authority]: /projects/project01/project01_children/project01_create-onprem-dc01-roles/#certificate-authority