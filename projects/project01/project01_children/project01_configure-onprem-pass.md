---
layout: page
title: AD DS - Password Policy
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 7
---



{: .note}
We'll be using the ***AD DS*** MMC Profile for this section.  


## Enforcing a Fine-Grained Password Policy


Open ***Active Directory Users and Groups*** and navigate through the Organizational Units.  
***mydomain.local*** > ***Resources*** > ***Groups***.  

Within the ***Groups*** OU, create a security group called ***SG_GlobalPasswordPolicy***.  
![](/assets/images/projects/project01/configure-on-prem/AD/password-policy-1.png "AD DS - User - 1"){:.sc}  

Open ***Active Directory Administrative Center***  
Navigate through the menus ***mydomain (local)*** > ***System*** and select ***Password Settings Container***.  
![](/assets/images/projects/project01/configure-on-prem/AD/password-policy-2.png "AD DS - User - 2"){:.sc}  

On the right-hand sidebar, select ***New*** > ***Password Settings***.  
![](/assets/images/projects/project01/configure-on-prem/AD/password-policy-3.png "AD DS - User - 3"){:.sc}  



---



## Configuring the Policy

Adjust the settings of the policy as below ***OR*** create your own password policy.  

{: .note}
These settings follow the minimum and recommended password guidelines as defined by [Microsoft's Password Policy] and [NIST SP800-63-3] (subsection [SP800-63B]).  

![](/assets/images/projects/project01/configure-on-prem/AD/password-policy-4.png "AD DS - User - 4"){:.sc}  



---



{: .new-title}
> Password Policy Enforced!
>
We've successfully created a Fine-Grained Password Policy!  
Please make your way to the [next section], where we'll be associating our Password Policy with a Shadow Group!



[next section]: /projects/project01/project01_children/project01_configure-onprem-shadow
[Microsoft's Password Policy]: https://learn.microsoft.com/en-us/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide
[NIST SP800-63-3]: https://pages.nist.gov/800-63-3/sp800-63-3.html
[SP800-63B]: https://pages.nist.gov/800-63-3/sp800-63b.html