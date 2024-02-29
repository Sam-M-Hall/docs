---
layout: page
title: Configuration
parent: Entra Connect
grand_parent: Hybrid Connections
nav_order: 2
---



## Downloading Azure AD Connect

You can visit the site below to get the latest installer.  
[Azure AD Connect V2](https://www.microsoft.com/en-us/download/details.aspx?id=47594){: .btn .btn-blue}



---



## Getting Started with Azure AD Connect


Launch the installer to get started.  

Review the welcome page, read what you desire, and accept the agreement if you so choose.  

Click ***Continue***
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-1.png "Entra Connect - Setup 1"){:.sc}  

Notice the warning at the bottom of this page. This is because when the domain was created, it was done so with a non-routable domain ".local".  

We'll choose ***Customize*** so we can perform advanced configuration.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-2.png "Entra Connect - Setup 2"){:.sc}  

Accept the defaults and click ***Install***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-3.png "Entra Connect - Setup 3"){:.sc}  



---



## Configuring Azure AD Connect


Accept the defaults and click ***Next***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-4.png "Entra Connect - Setup 4"){:.sc}  

Enter the credentials to connect to your M365 Tenant's Azure AD/Entra ID.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-5.png "Entra Connect - Setup 5"){:.sc}  

On this page, we're simply adding the directory we'd like to connect with Azure AD/Entra ID.  

Click ***Add Directory***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-6.png "Entra Connect - Setup 6"){:.sc}  

Enter your domain admin credentials to authorize the wizard to generate a new user for the Sync process.  

Click ***OK***  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-6-1.png "Entra Connect - Setup 6-1"){:.sc}  

The authorized forest has now been added and can be seen as verified under ***Configured Directories***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-7.png "Entra Connect - Setup 7"){:.sc}  

The original domain suffix shows as ***Not Added*** because it's a non-routable domain.  

The newly added UPN for the on-premise AD environment is populating and shows a verified status.  

Accept the default attribute matching selection of ***userPrincipalName***.  

Check the box and click ***Next***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-8.png "Entra Connect - Setup 8"){:.sc}  

Select the ***Sync selected domains and OUs*** radio button.  

Navigate through the OU tree as shown below and choose the ***Users*** OU.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-9.png "Entra Connect - Setup 9"){:.sc}  

Accept the defaults and click ***Next***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-10.png "Entra Connect - Setup 10"){:.sc}  

{: .note}
> If you wanted to use a Security Group instead, this is the page where you'd enter the Security Group you'd like to sync. You'd simply select ***Sync all domains and OUs*** back on the ***Domain/OU Filtering*** page.  
> 
> This could be better for larger environments where you'd like to approach this in rolling stages.  

For this lab environment, we'll stick with syncing our original selection.  

Click ***Next***  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-11.png "Entra Connect - Setup 11"){:.sc}  

Accept the defaults as shown and click ***Next***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-12.png "Entra Connect - Setup 12"){:.sc}  

Accept the defaults and click ***Install***.  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-13.png "Entra Connect - Setup 13"){:.sc}  

Installation and configuration are complete!  

Click ***Exit***  
![](/assets/images/projects/project01/entra-connect/entra-connect-setup-14.png "Entra Connect - Setup 14"){:.sc}  



---



## Checking the Sync Status

Open the ***Synchronization Service Manager*** as an administrator.  

On the default page, we can see the sync progress of our environments.  

I would suggest waiting 15-30 minutes for the initial synchronization to finalize.  
![](/assets/images/projects/project01/entra-connect/entra-connect-sync-1.png "Entra Connect - Sync 1"){:.sc}  

Navigate to the Entra ID portal by clicking below.  
[Microsoft - Entra Identity](https://entra.microsoft.com/){: .btn .btn-blue}  

On the left-hand sidebar, expand the Users section and click ***All users***.  

When the sync has completed, you'll see that a new column has appeared and you can see their ***on-premise sync status***.  

![](/assets/images/projects/project01/entra-connect/entra-connect-sync-2.png "Entra Connect - Sync 2"){:.sc}  

Select ***Alex Adams*** or whatever account you'd like.  

On the primary ***Overview*** pane, click the ***Properties*** tab within the middle-set banner tabs.  

This will open the User's Properties pane.  

On the bottom right of this page, there's a section called ***On-premises*** where you can see all data that are being synced between Entra ID and your on-premise environment.  
![](/assets/images/projects/project01/entra-connect/entra-connect-sync-3.png "Entra Connect - Sync 3"){:.sc}  



---



{: .important-title}
> Configuration Complete!
>
We've successfully configured our environment!  
Please make your way to the [next section], where we'll be reviewing the project overall!


[next section]: /projects/project01/project01_children/project01_summary