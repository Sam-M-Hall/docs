---
layout: page
title: DHCP - Scope Config
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 9
---

{: .note}
We'll be using the ***Roles*** MMC Profile for this section.  


## Creating a DHCP Scope


Expand the DHCP tree until you can see the items within ***IPv4***.  

Right-click the ***IPv4*** object and choose ***New Scope***.  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-1.png "DHCP - Scope - 1"){:.sc}  

Follow the ***New Scope Wizard*** prompts as guided below.  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-2.png "DHCP - Scope - 2"){:.sc}  

Enter a name for your new scope and click ***Next >***.  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-3.png "DHCP - Scope - 3"){:.sc}  

Enter the range of IP addresses you'd like to distribute on your network.  

I chose `10.10.100-200` which falls within our primary subnet `10.10.100.0/24` for this domain environment.  

Verify the subnet mask is configured with a `/24` subnet. 


{: .highlight-title}
> Pro Tip!
>
> `/24` is the CIDR notation for `255.255.255.0`!  
>
> [Learn more about CIDR Notation.]  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-4.png "DHCP - Scope - 4"){:.sc}  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-5.png "DHCP - Scope - 5"){:.sc}  

Accept the default lease time of 8 Days and click ***Next >***.  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-6.png "DHCP - Scope - 6"){:.sc}  

Accept the default radio button selection so we can configure DHCP options next.  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-7.png "DHCP - Scope - 7"){:.sc}  

Enter the IP Address of the ***Router (Default Gateway)***  
*Which in this scenario is the PFSense LAN Interface IP (10.10.100.1).*  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-8.png "DHCP - Scope - 8"){:.sc}  

Click ***Add*** and the entry will populate within the list.  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-9.png "DHCP - Scope - 9"){:.sc}  

This page will auto-populate with the required information.  

If you have any other DNS servers you'd like to add, enter them now and click ***Add***.  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-10.png "DHCP - Scope - 10"){:.sc}  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-11.png "DHCP - Scope - 11"){:.sc}  

Click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/DHCP/create-scope-12.png "DHCP - Scope - 12"){:.sc}  



---



## DHCP Overview


Expand the newly created scope and click the child objects to review them.  

### Address Pool  
*Overview of created address pools defined within the scope.*  
![](/assets/images/projects/project01/configure-on-prem/DHCP/overview-1.png "DHCP - Overview - 1"){:.sc}  

### Address Leases  
*List of active address leases within the scope.*  
![](/assets/images/projects/project01/configure-on-prem/DHCP/overview-2.png "DHCP - Overview - 2"){:.sc}  

### Reservations  
*List of active reservations within the scope.*  
![](/assets/images/projects/project01/configure-on-prem/DHCP/overview-3.png "DHCP - Overview - 3"){:.sc}  

### Scope Options  
*Overview of scope options defined within the scope.*  
![](/assets/images/projects/project01/configure-on-prem/DHCP/overview-4.png "DHCP - Overview - 4"){:.sc}  

### Policies  
*Overview of policies defined within the scope.*  
![](/assets/images/projects/project01/configure-on-prem/DHCP/overview-5.png "DHCP - Overview - 5"){:.sc}  



---



{: .new-title}
> DHCP Initialized!
>
We've successfully initialized the DHCP Server!  
Please make your way to the [next section], where we'll be configuring the DNS Server!



[next section]: /projects/project01/project01_children/project01_configure-onprem-dns
[Learn more about CIDR Notation.]: https://www.digitalocean.com/community/tutorials/understanding-ip-addresses-subnets-and-cidr-notation-for-networking#cidr-notation