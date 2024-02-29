---
layout: page
title: Finalize Account
parent: Create M365 Environment
grand_parent: Hybrid Connections
nav_order: 3
---



## Final touches before On-Prem setup.


Since we've got the domain set up on our account now, we can modify our admin account with proper information and email domain.  

On the sidebar, navigate to the ***Admin centers*** section and select ***Identity***.  
This will take us to the [Entra ID Dashboard](https://entra.microsoft.com/){: .btn .btn-blue }  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-1.png "M365 - User Setup 1"){:.sc}

Click on the ***Users*** drop-down carrot to expand the options and select ***All users***.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-2.png "M365 - User Setup 2"){:.sc}

You'll be brought to the ***Users Dashboard*** where we can see an overview of all users within the tenant. Let's go ahead and select our admin account so we can enter some basic info and swap our domain. Click the ***FNU LNU*** hyperlink to get into the ***User properties*** screen.
![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-3.png "M365 - User Setup 3"){:.sc}

Once inside the ***User properties*** screen select the ***Edit properties*** button on the ribbon.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-4.png "M365 - User Setup 4"){:.sc}


Inside the ***Edit properties*** pane, we can now modify the details of our account.  
1. Display Name
2. First Name
3. Last Name
4. User principal name - domain


![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-5.png "M365 - User Setup 5"){:.sc}

Enter the details you'd like to configure for fields 1-3, then click the drop-down menu for the domain  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-6.png "M365 - User Setup 6"){:.sc}

and select your newly added domain from the previous section and click ![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-7-1.png "M365 - User Setup 7-1"){:.sc}   at the bottom.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-7.png "M365 - User Setup 7"){:.sc}

You will be brought back to the ***User properties*** page for your account.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-8.png "M365 - User Setup 8"){:.sc}

{: .important}
If the old info is still present, click the ![](/assets/images/projects/project01/create-M365-environment/M365-admin-user-setup-8-1.png "M365 - User Setup 8-1"){:.sc} button to update the screen.  



---



{: .new-title}
> Congratulations!
>
We've successfully finalized our account details!  
Please make your way to the [next section], where we'll be creating the on-premise environment!  



[Microsoft 365 Developer Program]: https://developer.microsoft.com/en-us/microsoft-365/dev-program
[M365 Developer Program dashboard]: https://developer.microsoft.com/en-us/microsoft-365/profile
[next section]: /projects/project01/project01_children/project01_create-onprem/