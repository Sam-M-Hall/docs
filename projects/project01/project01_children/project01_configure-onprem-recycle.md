---
layout: page
title: AD DS - Recycle Bin
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 2
---



# What is the AD DS Recycle Bin?


The Active Directory Domain Services (AD DS) Recycle Bin Feature provides a specialized container within the Active Directory Administrative Center (ADAC) to maintain objects recently deleted from AD DS.  

This container provides an avenue to recover accidental or intentional deletions that could either destroy active account objects or negatively impact the health of the AD DS environment.  

{: .highlight-title}
> Additional Information
> 
> Reference the articles below to learn more about the AD DS - Recycle Bin Feature.  
> 
> - [Microsoft Learn - Enable-ADOptionalFeature]  
> - [The AD Recycle Bin: Understanding, Implementing, Best Practices, and Troubleshooting]  



---



# Enabling AD DS Recycle Bin


Copy the script below to a notepad so you can modify it to meet your needs.  


```powershell
Enable-ADOptionalFeature 'Recycle Bin Feature' -Scope ForestOrConfigurationSet -Target mydomain.local
```

Enter the command into an elevated PowerShell console.  

Press `Enter` to execute the command with the supplied parameters.  

The console returns a warning that enabling Recycle Bin is an irreversible action.  

You're prompted to confirm that you'd like to perform this action.  

Press `Y` and hit `Enter`.  
![](/assets/images/projects/project01/configure-on-prem/AD/ad-recycle-enable-3-1.png "AD DS - Recycle Bin - 3"){:.sc}  

We can verify the configuration was successful by entering the below command.  


```powershell
Get-ADOptionalFeature 'Recycle Bin Feature' | Format-List -Property EnabledScopes
```

This will output all Enabled Scopes for AD DS - Recycle Bin.  
![](/assets/images/projects/project01/configure-on-prem/AD/ad-recycle-enable-4-1.png "AD DS - Recycle Bin - 4"){:.sc}  



---



# Navigating to the Recycle Bin


Open up the Start Menu by pressing the `WIN` key.  

Scroll down to ***Windows Administrative Tools***.  

Expand the drop-down menu and select ***Active Directory Administrative Center***.  
![](/assets/images/projects/project01/configure-on-prem/AD/ad-recycle-enable-5.png "AD DS - Recycle Bin - 5"){:.sc}  

After launching ***ADAC***, we'll be brought to the ***Overview Dashboard***.  
![](/assets/images/projects/project01/configure-on-prem/AD/ad-recycle-enable-6.png "AD DS - Recycle Bin - 6"){:.sc}  

In the sidebar, click the entry that shows your domain.  

In my example, this is ***cmrlabs (local)***.  
![](/assets/images/projects/project01/configure-on-prem/AD/ad-recycle-enable-7.png "AD DS - Recycle Bin - 7"){:.sc}  

We can see the container called ***Deleted Objects*** within the ***cmrlabs (local)*** directory.  
![](/assets/images/projects/project01/configure-on-prem/AD/ad-recycle-enable-8.png "AD DS - Recycle Bin - 8"){:.sc}  

Within the ***Deleted Objects*** container, we can see there are no objects.  

When an object like an Organizational Unit or Account (Computer or User) is deleted, it will populate here.  
![](/assets/images/projects/project01/configure-on-prem/AD/ad-recycle-enable-9.png "AD DS - Recycle Bin - 9"){:.sc}  



---



{: .new-title}
> Recycle Bin Enabled!
>
We've successfully enabled the AD DS - Recycle Bin Feature!  
Please make your way to the [next section], where we'll be configuring Administrator Accounts!  



[next section]: /projects/project01/project01_children/project01_configure-onprem-admin

[Microsoft Learn - Enable-ADOptionalFeature]: https://learn.microsoft.com/en-us/powershell/module/activedirectory/enable-adoptionalfeature?view=windowsserver2022-ps  


[The AD Recycle Bin: Understanding, Implementing, Best Practices, and Troubleshooting]: https://techcommunity.microsoft.com/t5/ask-the-directory-services-team/the-ad-recycle-bin-understanding-implementing-best-practices-and/ba-p/396944