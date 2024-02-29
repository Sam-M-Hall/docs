---
layout: page
title: DC01 - Initialize
parent: Create On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 6
---



# DC01 - Initialize


Time to start diving into the initialization process for DC01!  



---



## Getting Logged In!


Windows will go through its initialization process upon rebooting.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-1.png "DC01 - Initial - 1"){:.sc}  

Once complete, you'll see the ***Customize settings*** screen appear, where you configure the password for the Local Administrator account ***Administrator***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-2.png "DC01 - Initial - 2"){:.sc}  

Once you've entered the password you desire, click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-3.png "DC01 - Initial - 3"){:.sc}  

We're now brought to the lock screen after creating the admin password.  
Press `CTRL` + `ALT` + `INSERT` at the same time to unlock the screen.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-4.png "DC01 - Initial - 4"){:.sc}  

Sign in to the ***Administrator*** account.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-5.png "DC01 - Initial - 5"){:.sc}  

When you sign into Windows Server 2022, ***Server Manager*** automatically launches.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-6.png "DC01 - Initial - 6"){:.sc}  


{: .note}
You'll see a popup concerning ***Windows Admin Center*** which can be permanently dismissed by clicking the ***Don't show this message again*** checkbox and closing the window.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-7.png "DC01 - Initial - 7"){:.sc}  


On the sidebar, click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-7-1.png "DC01 - Initial  - 7-1"){:.sc}  

We're brought to the server's properties page, where we can see details like Computer Name, Ethernet info, OS Version, Time Zone and more.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-8.png "DC01 - Initial - 8"){:.sc}  



---



## Renaming the Server


Click the ***Computer Name***, so that we can change it.  
Mine has been set to **WIN-EDLNHF2F8OF** by default.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-8-1.png "DC01 - Initial  - 8-1"){:.sc}  

We're now brought to the ***System Properties*** Panel.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-9.png "DC01 - Initial - 9"){:.sc}  
Click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-9-1.png "DC01 - Initial  - 9-1"){:.sc} to change the name.  

I'll be naming this server ***DC01*** as it will be serving as the primary Domain Controller in this environment. Name it whatever you like, then click ***OK***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-10.png "DC01 - Initial - 10"){:.sc}  

We received a message stating a restart is required for the changes to take effect.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-11.png "DC01 - Initial - 11"){:.sc}  

You'll also notice a warning on the ***System Properties*** Panel.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-12.png "DC01 - Initial - 12"){:.sc}  

Press **OK** to save the configuration.  

After closing the ***System Properties*** Panel, we receive another notice that a restart is required.  
Choose ***Restart Later***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-13.png "DC01 - Initial - 13"){:.sc}  



---



## Configuring the Network Interface


Within the below section, click on the ***Ethernet0*** entry ***IPv4 address assigned by DHCP, IPv6 enabled***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-14.png "DC01 - Initial - 14"){:.sc}  

This will open the ***Network & Sharing Center***.  
Double-click the network interface ***Ethernet0*** to configure it.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-15.png "DC01 - Initial - 15"){:.sc}  

As we can see, there is no network access due to the interface being unconfigured. This is because there is no DHCP Server in our environment yet.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-16.png "DC01 - Initial - 16"){:.sc}  
Click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-16-1.png "DC01 - Initial - 16-1"){:.sc} to open the ***Properties*** Panel for this interface.  

First, we'll disable IPv6 by unchecking the entry displayed below.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-17.png "DC01 - Initial - 17"){:.sc}  

Next, let's configure the IPv4 settings. Select the ***Internet Protocol Version 4 (TCP/IPv4)*** entry.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-18.png "DC01 - Initial - 18"){:.sc}  
Click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-18-1.png "DC01 - Initial - 18-1"){:.sc}  to open the config page.  

On the IPv4 Properties Panel, select the ***Use the following IP address*** radio button.  

Enter an IPv4 address that falls within the previously configured network (`10.10.100.0/24`).  
I've chosen `10.10.100.20` as an example.  

For the ***Subnet mask*** field, type in the Subnet Mask associated with the previously created network, which is `/24` or `255.255.255.0`.  

Lastly, enter the OPNsense IP address (`10.10.100.1`) into the ***Default gateway*** field and click ***OK***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-19.png "DC01 - Initial - 19"){:.sc}  

Click ***OK*** until you've fully closed the ***Ethernet0 Properties*** Panel.  

You'll most likely see a banner like this one popup after configuring the network interface. Simply click ***No***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-20.png "DC01 - Initial - 20"){:.sc}  

Click ![](/assets/images/projects/project01/create-on-prem/dc01/srv-mgr-btn-refresh.png "Server Manager - Button - Refresh"){:.sc} in the top right of the ribbon bar to refresh the Local Server info.  

We'll now see the updated IPv4 address assigned to ***Ethernet0*** which verified the configuration.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-21.png "DC01 - Initial - 21"){:.sc}  



---



## Verifying Connectivity


Let's verify our connectivity to the internet.  

Open Run by pressing `WIN` + `R` at the same time, type in `cmd` and press `Enter`.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-22.png "DC01 - Initial - 22"){:.sc}  

On the command line, enter `ipconfig /all` and hit `Enter` to display the full interface configuration.  

Now, type `ping 10.10.100.1` and hit `Enter` to verify we can reach OPNsense, our configured ***Default Gateway***.  

You should see ***Reply from 10.10.100.1*** with some associated metrics.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-23.png "DC01 - Initial - 23"){:.sc}  

Since we can see our gateway, let's try reaching outside our network!  

Type in `ping 8.8.8.8 -t` to start an endless ping to Google's DNS Server.  
You can terminate the ping by pressing `CTRL` + `C` at once.  
*You may have to do so a few times to interrupt the process.*  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-24.png "DC01 - Initial - 24"){:.sc}  



---



## Changing the Time Zone


Next up, let's change the time zone!  

Click the entry for ***Time zone***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-25.png "DC01 - Initial - 25"){:.sc}  

Within the ***Date and Time*** Panel, click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-26.png "DC01 - Initial - 26"){:.sc}  

Within the ***Time Zone Settings*** Panel, select your timezone from the drop-down menu.  
Mine is ***(UTC-06:00) Central Time (US & Canada)***.  
Click ***OK***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-27.png "DC01 - Initial - 27"){:.sc}  

Click the ***Internet Time*** tab and click the ***Change Settings...*** button.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-28.png "DC01 - Initial - 28"){:.sc}  

Here, we can update our time server to whatever we want.  
I prefer to choose ***time.nist.gov*** which is already an entry in the drop-down menu.  

Click ***Update now*** to update your time server and synchronize.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-29.png "DC01 - Initial - 29"){:.sc}  

Click ***OK*** on the ***Internet Time Settings*** & ***Date and Time*** Panels to close them out and save the changes.  



---



## Performing Initial Updates


Back to the ***Server Manager*** dashboard, let's check out some Windows Updates options.  

By default, Windows Server is set to only ***download*** the updates *without* applying them, which is perfect for our use case and generally recommended for servers.  

Let's click the ***Last checked for updates*** entry. This will take us to the Windows Update page.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-30.png "DC01 - Initial - 30"){:.sc}  

Within Windows Update, we should see updates ready to be installed. If not, simply click ***Check*** to get the latest updates downloaded.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-31.png "DC01 - Initial - 31"){:.sc}  
Click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-31-1.png "DC01 - Initial  - 31-1"){:.sc} to install the pending updates.  
Once the installation is complete, click 
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-31-2.png "DC01 - Initial  - 31-2"){:.sc} to reboot the server.  



---



## Wrapping Up


After the server reboots, let's review some of the changes we've made!  

Navigate back to the ***Local Server*** properties by selecting it from the sidebar.  

We can see below that our Computer name has changed, and there's a new entry ***Azure Arc Management***.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-32.png "DC01 - Initial - 32"){:.sc}  

We can also see our Updates and Time Zone entries are updated and accurate.  
![](/assets/images/projects/project01/create-on-prem/dc01/initial/dc01-initial-setup-33.png "DC01 - Initial - 33"){:.sc}  



---



{: .new-title}
> Initialtization Finished!
>
We've successfully initialized our Windows Server!
Please make your way to the [next section], where we'll be configuring Roles & Features!



[next section]: /projects/project01/project01_children/project01_create-onprem-dc01-roles