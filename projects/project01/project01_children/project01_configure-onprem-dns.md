---
layout: page
title: DNS - Reverse Lookup
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 10
---



{: .note}
We'll be using the ***Roles*** MMC Profile for this section.  


## Creating a Reverse Lookup Zone


Expand the DNS tree until you can see the items within ***DC01***.

Right-click ***Reverse Lookup Zones*** and click ***New Zone***.  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-1.png "DNS - Reverse Lookup - 1"){:.sc}  

Follow the prompts throughout the ***New Zone Wizard*** as displayed below.  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-2.png "DNS - Reverse Lookup - 2"){:.sc}  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-3.png "DNS - Reverse Lookup - 3"){:.sc}  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-4.png "DNS - Reverse Lookup - 4"){:.sc}  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-5.png "DNS - Reverse Lookup - 5"){:.sc}  

Enter the first three octets of your subnet.  

In this example, I would enter `10.10.100` for the subnet of `10.10.100.0/24`.  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-6.png "DNS - Reverse Lookup - 6"){:.sc}  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-7.png "DNS - Reverse Lookup - 7"){:.sc}  

Click ***Finish***  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-8.png "DNS - Reverse Lookup - 8"){:.sc}  

Once complete, you'll see the reverse lookup zone has been generated and should have data that's being populated.

You can click refresh if you don't see any data.  
![](/assets/images/projects/project01/configure-on-prem/DNS/reverse-lookup-9.png "DNS - Reverse Lookup - 9"){:.sc}  



---



{: .new-title}
> DNS Configured!
>
We've successfully created the Reverse Lookup Zone!  
Please make your way to the [next section], where we'll be configuring a File Share!



[next section]: /projects/project01/project01_children/project01_configure-onprem-FPS