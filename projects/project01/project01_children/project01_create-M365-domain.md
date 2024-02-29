---
layout: page
title: Add Domain
parent: Create M365 Environment
grand_parent: Hybrid Connections
nav_order: 2
---



## Adding your domain to the M365 Developer Program environment.


Now that we've signed up for and initialized the M365 Environment, let's add our purchased domain within the ***Domains*** section. This will allow us to fully utilize the domain across M365.  

If you've just signed into your account, or accessed the account through the ***Go to subscription*** hyperlink from the last section, you can access the admin dashboard by clicking the Admin Portal button on the sidebar.  
It looks like this -> 
![](/assets/images/projects/project01/create-M365-environment/M365-admin-icon.png "M365 - Admin Icon"){:.sc}<- and will be located on the sidebar to the left.

Alternatively, simply click the button below.  
[M365 Admin Portal](https://admin.microsoft.com/){: .btn .btn-blue }

Alright, now that we're at the admin dashboard, expand all the settings by clicking ![](/assets/images/projects/project01/create-M365-environment/M365-admin-siebar-showall.png "M365 - Admin Sidebar Show All"){:.sc}

Expand the ***Settings*** section and select ***Domains***.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-sidebar-domains.png "M365 - Admin Sidebar Domains"){:.sc}

At the top of the page, click ![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add.png "M365 - Domains Add Button"){:.sc} to initiate the wizard.

Now enter the domain you'd like to connect, then click ![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-1-1.png "M365 - Domains Add Page 1 Button"){:.sc} below.   
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-1.png "M365 - Domains Add Page 1"){:.sc}

After submitting the info for the domain we want to add, we must go through the verification process. I'm using Cloudflare so I'm able to simply sign into my Cloudflare account.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-2.png "M365 - Domains Add Page 2"){:.sc}

Once you've selected your verification option, click ![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-2-1.png "M365 - Domains Add Page 2 Button"){:.sc} to initiate the process.  

After clicking verify, I'm prompted with a login panel for Cloudflare.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-2-2.png "M365 - Domains Add Page 2 - Cloudflare"){:.sc}

After logging in, I was presented with a screen to *"Authorize DNS records from Microsoft"*, which will be used by Microsoft to validate ownership of the domain.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-2-3.png "M365 - Domains Add Page 2 - Authorize"){:.sc}

After authorizing through whatever method you've chosen, you will see the following screen while Microsoft goes through the domain validation process.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-2-4.png "M365 - Domains Add Page 2 - Verifying Phase"){:.sc}

After the validation process is complete, we're brought to the next step of setup.  

We need to connect our validated domain to our M365 Environment.  
Again, since I'm using Cloudflare, I can use the built-in process to append the required records. Once you've made your selection for how you'd like to connect your domain, click ![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-3-1.png "M365 - Domains Add Page 3 - Continue"){:.sc} to proceed.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-3.png "M365 - Domains Add Page 3"){:.sc}

Microsoft now wants us to verify whether or not it should be adding the required DNS records for Exchange services.  
  
For this project, we will not be utilizing any on-premise Exchange Servers, so we can accept the defaults and click ![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-3-3.png "M365 - Domains Add Page 3 - Add DNS Records"){:.sc} to continue.  

Microsoft is once again asking for authorization to append DNS records on our behalf for functionality between the domain and M365 services. Select ![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-3-5.png "M365 - Domains Add Page 3 - Authorize Button"){:.sc} to continue.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-3-4.png "M365 - Domains Add Page 3 - Authorize"){:.sc}

After authorization is confirmed, we're met with another loading screen.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-3-6.png "M365 - Domains Add Page 3 - Checking DNS Records"){:.sc}

After some time, we're brought back to the overview of adding our domain, where we should receive a message stating *"Domain setup is complete"*. Click ![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-4-1.png "M365 - Domains Add Page 4 - Done"){:.sc} to exit the setup.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-add-4.png "M365 - Domains Add Page 4 - Complete"){:.sc}



---



## Congratulations!  
We've successfully added a domain to our M365 Environment and can see it in the ***Domains*** section.  
![](/assets/images/projects/project01/create-M365-environment/M365-admin-domains-overview.png "M365 - Domains Overview"){:.sc}



---



{: .new-title}
> On a roll!
>
We've successfully added our custom domain to the M365 Environment!  
Please make your way to the [next section], where we'll be finalizing some account details!



[Microsoft 365 Developer Program]: https://developer.microsoft.com/en-us/microsoft-365/dev-program
[M365 Developer Program dashboard]: https://developer.microsoft.com/en-us/microsoft-365/profile
[next section]: /projects/project01/project01_children/project01_create-M365-finalize