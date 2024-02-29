---
layout: page
title: DC01 - Roles
parent: Create On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 7
---



# DC01 - Roles


Time to start the basic roles for DC01!  



---



## Adding Roles and Features


Let's start by adding our basic roles and features for the domain environment.  

In the top right of the ribbon menu in ***Server Manager***, select ***Manage***, then ***Add Roles and Features***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-1.png "DC01 - Roles - 1"){:.sc}  

Review the ***Before you begin*** screen.  

If you never want to see it again, simply check the ***Skip this page by default*** checkbox at the bottom.  

Click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-2.png "DC01 - Roles - 2"){:.sc}  

Accept the default selection of the ***Role-based or feature-based installation*** radio button and click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-3.png "DC01 - Roles - 3"){:.sc}  

Accept the default selection of the current server and click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-4.png "DC01 - Roles - 4"){:.sc}  

On the ***Server Roles*** page, click the checkbox for ***Active Directory Domain Services***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-5.png "DC01 - Roles - 5"){:.sc}  

In the popup, accept the screen by clicking ***Add Features***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-6.png "DC01 - Roles - 6"){:.sc}  

On the ***Server Roles*** page, click the checkbox for ***DHCP Server***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-7.png "DC01 - Roles - 7"){:.sc}  

In the popup, accept the screen by clicking ***Add Features***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-8.png "DC01 - Roles - 8"){:.sc}  

On the ***Server Roles*** page, click the checkbox for ***DNS Server***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-9.png "DC01 - Roles - 9"){:.sc}  

In the popup, accept the screen by clicking ***Add Features***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-10.png "DC01 - Roles - 10"){:.sc}  

We're done adding roles. Click ***Next >***.  

On the ***Features*** page, click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-11.png "DC01 - Roles - 11"){:.sc}  

On the ***AD DS*** page, click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-12.png "DC01 - Roles - 12"){:.sc}  

On the ***DHCP Server*** page, click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-13.png "DC01 - Roles - 13"){:.sc}  

On the ***DNS Server*** page, click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-14.png "DC01 - Roles - 14"){:.sc}  

On the ***Confirmation*** page, click 
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-15.png "DC01 - Roles - 15"){:.sc} to initiate installation.  



---



## Promoting to Domain Controller


Once the installation process is complete, we can continue our setup.  

Click ***Promote this server to a domain controller***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-roles-16.png "DC01 - Roles - 16"){:.sc}  

Select the ***Add a new forest*** radio button and enter the domain you've previously purchased and configured, followed by `.local` in the ***Root domain name*** field.  

I've entered `cmrlabs.local` as an example.  

Click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-1.png "DC01 - AD DS - 1"){:.sc}  

Accept the defaults for the Domain & Forest functional levels.  

Enter a different and secure password for the ***Directory Services Restore Mode (DSRM)*** password field.  


{: .warning}
It's ***HIGHLY SUGGESTED*** to store this password somewhere secure and available.  


Click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-2.png "DC01 - AD DS - 2"){:.sc}  

On the ***DNS Options*** page, click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-3.png "DC01 - AD DS - 3"){:.sc}  

On the ***Additional Options*** page, wait for the NetBIOS domain to configure itself.  
It should just be the domain ***without*** `.local` in all caps. 

Click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-4.png "DC01 - AD DS - 4"){:.sc}  

On the ***Paths*** page, accept the default folder paths by clicking ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-5.png "DC01 - AD DS - 5"){:.sc}  

Scroll through the ***Review Options*** page to review the configuration for any errors.  
Click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-6.png "DC01 - AD DS - 6"){:.sc}  

On the ***Prerequisites Check*** page Windows will automatically perform a check against to verify the proper conditions are met for promoting itself to a Domain Controller.  
If it finds any issues it will let you know.  

All warnings received below are expected and informative only.  

Click ***Install***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-7.png "DC01 - AD DS - 7"){:.sc}  

After the installation process completes, you will see a popup stating ***You're about to be signed out***, which is a nice way of telling you the server will be rebooting in one minute.  

You can simply wait and let Windows do its thing.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-8.png "DC01 - AD DS - 8"){:.sc}  

Once the machine reboots, you may see the below message. Just wait patiently.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-9.png "DC01 - AD DS - 9"){:.sc}  

Once the machine is done finalizing changes, you'll be brought back to the login screen.  

Immediately, things look a bit different!  
We now have the domain prefix before our ***Administrator*** account, and we can even select ***Other user*** as a login option!  

For now, just log in with the *now* ***DOMAIN\Administrator*** account!  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-10.png "DC01 - AD DS - 10"){:.sc}  

Back on the ***Server Manager*** page, we see a caution symbol next to the flag icon in the top right ribbon menu. Click on the flag icon.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-11.png "DC01 - AD DS - 11"){:.sc}  

We're presented with a ***Post-deployment Configuration Task*** stating there is ***Configuration required for DHCP Server at DC01***.  

Click ***Complete DHCP configuration*** to get started.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-ad-initial-12.png "DC01 - AD DS - 12"){:.sc}  

Read the ***Description*** page as it explains to you what this wizard does.  
Click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-dhcp-initial-1.png "DC01 - DHCP - 1"){:.sc}  

Accept the default radio button ***Use the following user's credentials*** and click ***Commit***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-dhcp-initial-2.png "DC01 - DHCP - 2"){:.sc}  

Review the summary page if you'd like and hit ***Close***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/dc01-dhcp-initial-3.png "DC01 - DHCP - 3"){:.sc}  



---



# Certificate Authority


Back in ***Add Roles & Features Wizard***, add the ***AD Certificate Authority*** Role by clicking the checkbox and accepting the default features options by clicking ***Add Features***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/ca-role-1.png "DC01 - CA - 1"){:.sc}  

On the next screen, click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/ca-role-2.png "DC01 - CA - 2"){:.sc}  

Select ***Certificate Authority*** and click ***Next >***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/ca-role-3.png "DC01 - CA - 3"){:.sc}   



Once the feature is installed, click ***Close***.  
![](/assets/images/projects/project01/create-on-prem/dc01/roles/ca-role-4.png "DC01 - CA - 4"){:.sc}  

{: .important}
Configuration will be completed in the [AD CS - Certificate Authority] sub-section.  



---



## Well Done!


And just like that, we've laid the foundation for our on-premise domain environment!



---



{: .new-title}
> On-Prem Created!
>
We've successfully created our On-Prem Environment!
Please make your way to the [next section], where we'll be configuring all previously installed roles and more!



[next section]: /projects/project01/project01_children/project01_configure-onprem
[AD CS - Certificate Authority]: /projects/project01/project01_children/project01_configure-onprem-ca