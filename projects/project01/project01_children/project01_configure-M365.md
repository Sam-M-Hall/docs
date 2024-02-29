---
layout: page
title: Configure M365 Environment
parent: Hybrid Connections
nav_order: 5
---



# Adding User Accounts to M365


## Getting There
This section is going to be quite simple. We're just adding matching user accounts to M365 that are identical to our on-premise users and assigning licenses.  


You can easily add users by navigating to the ***M365 Admin Portal*** > ***Active Users*** and clicking the ***Add a user*** as shown below or click the convenient button!  

[M365 Admin Portal - Add User](https://admin.microsoft.com/Adminportal/Home#/users/:/adduser){: .btn .btn-blue }


![](/assets/images/projects/project01/configure-M365/add-user-basic-1.png "M365 - Add User Basic - 1"){:.sc}  



---



## Adding Our Users

Let's start by adding our first user, by entering their details as required below.  

Verify all boxes are unchecked as below.  

Be sure to create a generic, but strong, password to use for ease of use in this lab.  
![](/assets/images/projects/project01/configure-M365/add-user-basic-2.png "M365 - Add User Basic - 2"){:.sc}  

Accept the default location and assign the available product license to the user!  
![](/assets/images/projects/project01/configure-M365/add-user-basic-3.png "M365 - Add User Basic - 3"){:.sc}  

Accept the default ***Roles*** and ***Profile info***.  
![](/assets/images/projects/project01/configure-M365/add-user-basic-4.png "M365 - Add User Basic - 4"){:.sc}  

Review the user's summary and click ***Finish Adding***.  
![](/assets/images/projects/project01/configure-M365/add-user-basic-5.png "M365 - Add User Basic - 5"){:.sc}  



---



## Creating a Template for Adding Users


Microsoft provides an easy way for us to standardize our user creation, called templates.  

Let's create one so that we can easily create users with similar settings.  

Click the ***User templates*** button and select ***Add template***.  
![](/assets/images/projects/project01/configure-M365/create-user-template-1.png "M365 - Create User Template - 1"){:.sc}  

Name your template and add a description if you'd like.  
![](/assets/images/projects/project01/configure-M365/create-user-template-2.png "M365 - Create User Template - 2"){:.sc}  

Select the domain, which should be the one you added earlier.  

Choose ***Let me create a password*** and verify the box is unchecked.  
![](/assets/images/projects/project01/configure-M365/create-user-template-3.png "M365 - Create User Template - 3"){:.sc}  

Assign the licenses available to your account.  
![](/assets/images/projects/project01/configure-M365/create-user-template-4.png "M365 - Create User Template - 4"){:.sc}  

Accept the default ***Roles*** and ***Profile info***.  
![](/assets/images/projects/project01/configure-M365/create-user-template-5.png "M365 - Create User Template - 5"){:.sc}  

Review the template's summary and click ***Finish Adding***.  
![](/assets/images/projects/project01/configure-M365/create-user-template-6.png "M365 - Create User Template - 6"){:.sc}  



---



## Adding User Accounts via Template


Click the ***User templates*** button and select the template you just created.  
![](/assets/images/projects/project01/configure-M365/add-user-template-1.png "M365 - Add User Template - 1"){:.sc}  

Enter the user's information as desired and click ***Add user***.  
![](/assets/images/projects/project01/configure-M365/add-user-template-2.png "M365 - Add User Template - 2"){:.sc}  

You'll get a verification that the user was created.  
Click ***Add another user using this template*** to repeat the process.  
![](/assets/images/projects/project01/configure-M365/add-user-template-3.png "M365 - Add User Template - 3"){:.sc}  



---


{: .important}
Continue creating all users that you've added to your on-premise environment.  


---



{: .new-title}
> User Accounts Created!
>
We've successfully created our M365 User Accounts!  
Please make your way to the [next section], where we'll be proceeding with establishing the connection between our on-premise environment and M365 Entra!  


[next section]: /projects/project01/project01_children/project01_entra-connect