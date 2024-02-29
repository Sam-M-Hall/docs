---
layout: page
title: FPS - File Sharing
parent: Configure On-Prem Environment
grand_parent: Hybrid Connections
nav_order: 11
---



## Installing the File Server Role


Open up ***Server Manager*** and expand the ***File and Storage Services*** drop-down.  
Within ***File and iSCSI Services*** select ***File Server***.  
  

Continue through the remaining windows and accept all defaults.  

Allow the feature to install and then close any menus/windows that popup.  
![](/assets/images/projects/project01/configure-on-prem/FPS/fps-roles-1.png "FPS - Roles - 1"){:.sc}  



---



## Creating the Shared Folder


{: .note}
We'll be operating out of ***Server Manager*** > ***File and Storage Services*** for the following section.  


Click ***Shares*** on the left-hand sidebar.  

Right-click the blank space and choose ***New Share***.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-1.png "FPS - Share - 1"){:.sc}  

Accept the default ***SMB Share - Quick*** and select ***Next >***.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-2.png "FPS - Share - 2"){:.sc}  

On the following page, select the ***Type a custom path*** radio button and click ***Browse...***  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-3.png "FPS - Share - 3"){:.sc}  

Within the popup window, drill down into the folder location that you'd like to share.  

In my example, I've created a folder tree of `data` > `common`.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-4.png "FPS - Share - 4"){:.sc}  

You'll see the path update in the custom path field.  

Verify this is correct and choose ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-5.png "FPS - Share - 5"){:.sc}  

Verify the share name and other fields are correct and click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-6.png "FPS - Share - 6"){:.sc}  

Verify the checkboxes match as below and click ***Next >***  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-7.png "FPS - Share - 7"){:.sc}  



---



## Advanced Permissions Configuration


On the permissions pane, click ***Customize Permissions***.  

In the ***Advanced Security Security Settings*** pane, click the ***Disable inheritance*** button.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-8.png "FPS - Share - 8"){:.sc}  

On the ***Block Inheritance*** popup, select ***Convert inherited permissions...***  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-9.png "FPS - Share - 9"){:.sc}  



Click ***Add*** below the ***Permission entries***  

Click on ***Select a principal*** and in the selection screen, enter the ***Authenticated Users*** object then click ***Check Names*** and click ***OK***.  

Back on the ***Permission Entry*** screen, click the ***Modify*** checkbox under ***Basic permissions***.  

Click ***OK***.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-10.png "FPS - Share - 10"){:.sc}  

In the ***Advanced Security Security Settings*** pane, next to the ***Owner*** entry, click ***Change***.  

In the selection screen, enter the ***Administrators*** object then click ***Check Names*** and click ***OK***.  

Remove all other objects under ***Permission entries*** to match the below config.  

Check the ***Replace all child object permissions entries...*** checkbox.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-11.png "FPS - Share - 11"){:.sc}  

You'll receive a ***Windows Security*** popup requesting confirmation of the changes.  

Click ***Yes***  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-12.png "FPS - Share - 12"){:.sc}  

You'll receive another ***Windows Security*** popup informing you will need to reopen the object for the changes to take effect.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-13.png "FPS - Share - 13"){:.sc}  

Click ***OK*** to close the ***Advanced Security Security Settings*** pane.  

Click ***Next >***
![](/assets/images/projects/project01/configure-on-prem/FPS/share-14.png "FPS - Share - 14"){:.sc}  



---



## Finalizing Creation


Click ***Create***
![](/assets/images/projects/project01/configure-on-prem/FPS/share-15.png "FPS - Share - 15"){:.sc}  

The share has been created.  

Click ***Close*** to close the wizard.  
![](/assets/images/projects/project01/configure-on-prem/FPS/share-16.png "FPS - Share - 16"){:.sc}  




---



{: .new-title}
> File Sharing Complete!
>
We've successfully created a File Share!  
Please make your way to the [next section], where we'll be configuring Group Policy utilizing the new File Share!



[next section]: /projects/project01/project01_children/project01_configure-onprem-gpo