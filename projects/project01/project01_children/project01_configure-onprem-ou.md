---
layout: page
title: AD DS - OUs
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 5
---



{: .note}
We'll be using the ***AD DS*** MMC Profile for this section.  


## Establishing the OU Structure


Expand the ***AD Users and Groups*** to see the base structure.   

In the blank space, right-click and hover on ***New*** and select ***Organizational Unit***.  
![](/assets/images/projects/project01/configure-on-prem/AD/ou-initial-1.png "AD DS - OU - 1"){:.sc}  

Enter the name for the first OU of ***Accounts***.  
![](/assets/images/projects/project01/configure-on-prem/AD/ou-initial-2.png "AD DS - OU - 2"){:.sc}  

Continue to create the OUs listed below (skipping the ones that already exist):

mydomain.local
- Accounts
    - Computers
        - Servers
        - Workstations
    - Groups
        - Distribution
        - Security
    - Users
        - !DisabledUsers
        - Admins
        - Users
- Resources
    - Groups
    - Users

Verify that your tree matches what's displayed below.  
![](/assets/images/projects/project01/configure-on-prem/AD/ou-initial-3.png "AD DS - OU - 3"){:.sc}  



---



## User Account Cleanup


Move the following accounts/objects as directed.  

***!DisabledUsers OU***  
Users\Administrator >> Accounts\Users\\!DisabledUsers  
Users\Guest >> Accounts\Users\\!DisabledUsers  

***Admins OU***  
Users\John.Smith >> Accounts\Users\Admins  



---


{: .new-title}
> Organization Complete!
>
We've successfully created our initial Organization Units!  
Please make your way to the [next section], where we'll be configuring User Accounts!



[next section]: /projects/project01/project01_children/project01_configure-onprem-user