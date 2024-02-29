---
layout: page
title: Summary
parent: Hybrid Connections
nav_order: 7
---



## Preparation


In preparation, we obtained a domain to be used throughout our project as well as installed and configured VMware Workstation.  



---



## Creation


Creating the environment consisted of joining the M365 Developer program, initializing our M365 tenant and provisioning our on-premise environment.  

### M365
- Join & Initliaze (Join Developer Program and perform initialization of tenant)
- Add Domain (Add the purchased domain as a verified domain connection to the tenant)
- Finalize Account (Adjust account details of admin account)

### On-Prem Environment
- OPNsense - Prepare (Download our ISO and provision the virtual machine)
- OPNsense - Initialize (Perform first-time setup and configuration of the firewall)
- OPNsense - Access (Finalize GUI access setup for administration)
- DC01 - Prepare (Download and provision the virtual machine and basic setup of server)
- DC01 - Initialize (Perform first-time setup and configuration of the server)
- DC01 - Roles (Add all roles to the server as required)



---



## Configuration


Configuring the environment consisted of provisioning all roles for DC01, creating our users in M365, and performing a first-time setup of Azure AD Connect/Entra Connect.  


### On-Prem
- General - MMC (created MMC profiles for ease of administration)
- AD DS - Recycle Bin (Enabled the AD DS Recycle Bin Feature to safeguard objects)
- AD DS - Admin Accounts (Created administrator account for on-prem administration)
- AD DS - Certificate Authority (Configured the Certificate Authority role)
- AD DS - OUs (Created our OU structure for better organization of objects and GPO assignment)
- AD DS - User Accounts (Created domain user accounts for the environment)
- AD DS - Password Policy (Established a fine-grained global password policy)
- AD DS - Shadow Group (Generated a mechanism for performing OU matching to automatically manage our global password policy security group)
- DHCP - Scope Config (Provisioned our DHCP server and created the first scope)
- DNS - Reverse Lookup (Established a reverse lookup zone to provide reverse DNS lookups across our domain's network scope)
- FPS - File Sharing (Generated a file share and delegated permissions)
- GPO - Mapped Drives (Created a GPO to automatically map network drives to delegated users)

### M365

Created matching users within our M365 tenant and assigned M365 licenses to them.  



---



## Synchronization

Established the initial connection between our on-premise environment and M365 tenant.  

- Preparation (Added our purchased domain as a UPN suffix to the on-prem domain)
- Configuration (Performed setup of Azure AD Connect/Entra Connect and verified syncing status)
