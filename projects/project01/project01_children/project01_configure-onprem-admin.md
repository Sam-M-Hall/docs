---
layout: page
title: AD DS - Admin Accounts
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 3
---



{: .note}
We'll be using the ***AD DS*** MMC Profile for this section.  


## Creating our Administrator Account


Expand ***Active Directory User and Groups*** > ***mydomain.local*** and select ***Users***.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-1.png "AD DS - Admin - 1"){:.sc}  

In the blank area, right-click to open the context menu.  

Hover on ***New*** to expose the sub-menu and click ***User***.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-2.png "AD DS - Admin - 2"){:.sc}  

Fill out the fields as displayed below with whatever you'd like.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-3.png "AD DS - Admin - 3"){:.sc}  

Enter a password for the account and ensure the boxes are ticked as below.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-4.png "AD DS - Admin - 4"){:.sc}  

Review the page and click ***Finish***.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-5.png "AD DS - Admin - 5"){:.sc}  

You'll now see the object created in the ***Users*** Organizational Unit.  

Double-click the user object to open the properties screen and choose ***Members Of*** to expand the user's current Group Memberships.  

Click ***Add...*** to add group membership to this account.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-6.png "AD DS - Admin - 6"){:.sc}  

In the ***Select Groups*** pane, add the following groups:  
- Domain Admins  
- Enterprise Admins  
- Group Policy Creator Owners  

Click ***Check Names*** after typing each entry to verify it resolves correctly.  

Click ***OK***.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-7.png "AD DS - Admin - 7"){:.sc}  

Now the groups will show under the ***Member Of*** section.  

Click ***OK*** to apply all changes and close the Properties window.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-8.png "AD DS - Admin - 8"){:.sc}  



---



## Transferring Your MMC Profiles


{: .important}
Save a copy of your MMC Profiles to the root of `C:\` so that you can copy them to your new Administrator Account after you sign in!  



---



## Disabling the Built-In Administrator


{: .warning}
**SIGN INTO THE NEWLY CREATED ADMINISTRATOR ACCOUNT BEFORE CONTINUING.**  


{: .highlight-title}
> MORE INFORMATION
> 
> I didn't go in-depth with configuring the Built-In Adminsitrator Account, however you can reference the following article to dive deeper into proper configuration of the account.    
> [Securing Built-in Administrator Accounts in Active Directory]  


Right-click the ***Administrator*** account and choose ***Disable Account***.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-9.png "AD DS - Admin - 9"){:.sc}  

You will get a popup confirming the account has been disabled.  
![](/assets/images/projects/project01/configure-on-prem/AD/admin-account-10.png "AD DS - Admin - 10"){:.sc}  



---



{: .new-title}
> God Mode Enabled!
>
We've successfully configured our Administrator Accounts!  
Please make your way to the [next section], where we'll be configuring the AD CS - Certificate Authority role!  



[next section]: /projects/project01/project01_children/project01_configure-onprem-ca
[Securing Built-in Administrator Accounts in Active Directory]: https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/appendix-d--securing-built-in-administrator-accounts-in-active-directory