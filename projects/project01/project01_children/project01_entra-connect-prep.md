---
layout: page
title: Preparation
parent: Entra Connect
grand_parent: Hybrid Connections
nav_order: 1
---



{: .note}
We'll be using the ***AD DS*** MMC Profile for this section.  


## Preparing for Connection


Right-click ***AD Domains and Trusts*** and select ***Properties***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-prep-1.png "Entra Connect - Prep 1"){:.sc}  

Enter the same domain you added to the M365 environment and click ***Add***.  

You will see it populate in the list below.  
![](/assets/images/projects/project01/entra-connect/entra-connect-prep-2.png "Entra Connect - Prep 2"){:.sc}  



---



## Updating the UPN four ALL Users


Microsoft provides a simple script for us to use in updating global UPN assignments for our users. I made some minor tweaks to print out the output.  

You can read more about it [here].  

Run ***Windows Powershell ISE*** as Administrator.  

Copy and paste the text below into the editor and modify it as needed.  

Click the green ***Run/Play*** button.  

```powershell
$LocalUsers = Get-ADUser -Filter {UserPrincipalName -like '*mydomain.local'} -Properties UserPrincipalName -ResultSetSize $null
$LocalUsers | foreach {$newUPN = $_.UserPrincipalName.Replace("mydomain.local","mydomain.com"); $_ | Set-ADUser -UserPrincipalName $newUPN; Write-Host "$_ UPN has been updated to $newUPN"}
```

As we can see, the script successfully runs and updates our user's UPNs.  
![](/assets/images/projects/project01/entra-connect/entra-connect-prep-3.png "Entra Connect - Prep 3"){:.sc}  



---



{: .new-title}
> Preparation Complete!
>
We've successfully prepared our environment!  
Please make your way to the [next section], where we'll be running through the setup process for Azure AD/Entra Connect!  


[next section]: /projects/project01/project01_children/project01_entra-connect-config
[here]: https://learn.microsoft.com/en-us/microsoft-365/enterprise/prepare-a-non-routable-domain-for-directory-synchronization?view=o365-worldwide