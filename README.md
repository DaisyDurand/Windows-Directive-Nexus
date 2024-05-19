# Windows-Directive-Nexus
## Description
This project entails deploying a Windows Server 2022 ISO alongside a Windows 11 ISO within an Oracle VirtualBox environment. The server operates as the domain controller, housing active directory functionalities. Two network adapters are utilized: one interfaces with the internet, while the other connects to the private network. Internal network IP addresses are assigned, while the external network automatically obtains an IP address from the home network. NAT and RAS configurations enable clients on the private network to access the internet via the domain controller. DHCP is implemented on the domain controller to automate IP address allocation for the Windows 11 deployment. A Python script manages user creation and organizational placement. The Windows 11 machine is seamlessly integrated into the server. User accounts are pre-established, facilitating user login to the machine. 

This project is based off of Josh Madakor's Active Directory tutorial.

## Environments Used
* Windows Server 2022 ISO
* Windows 11 ISO
* Oracle VM
## Network Diagram

![Network Diagram](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/2fd47e12-0dd7-44fc-9cb1-46114696962e)

## Step 1: - Assigning IP addresses

The first network connection is connected to the internet, hence the name. The second network was automatically assigned an ip address which is how I knew it was connected to the internal network.

![Project Network Connections](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/33ccfa58-b779-4a14-8387-e3309fc3aa5e)

Assigned an IP address. DC-2022 is going to serve as the default gateway which is why one was not assigned.

![Project IPV4](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/e9313be1-09d4-41ac-a081-207f4ddc3d8a)

## Step 2: - Active Directory Domain Services Installation

![Project Installing AD Domain Services](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/2e3a3ab6-bc39-495b-85b5-558f9c659e9d)

## Step 3: Creating the Domain
![Project doploying th ADDS](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/d92fdec5-5836-43ee-9367-3515e403c5ce)
![Project 1 NetBIOS domain name](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/7441adf8-cfe2-4099-a1cf-e4a99adc5beb)

## Step 4: Creating an Administrative User
![creating admin unit](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/9df4bd75-9671-45c9-b3e9-d57b969b5afb)
![Project 1 Creating an admin users](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/51d78813-8bfc-4de8-8236-f4502695b42a)
![Project 1 Add user to member of domain admins](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/6a311385-71f1-4d18-8c1b-ac4bab51f85d)
![Project 1 User added ](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/39cea954-f471-4118-abbb-d01f45529398)

## Step 5: Installing Remote Access and Routing
![Project remote access](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/a3ebbb13-0ac8-48c9-b978-9e0387a4c5a2)
![Project adding remot access](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/591ff34e-f816-475c-87cd-f1312f64cd91)

## IMPORTANT COMPUTER NAME IN WRONG PLACE
![Project Computer name](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/19b858b0-6ab9-40f2-9d0d-60bce8826a21)

## Step 6: Network Address Translation (NAT) Installation
![Project configuring remote access server](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/35f7c630-3865-4b3d-ad96-4738e887732f)
![Project configuring remote access summary](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/4949a30c-e25a-4440-bb61-f300be0c35ff)

## Step 7: DHCP Installation
![Project Installing DHCP](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/fc1173ac-4e5d-4164-8b4d-a46c91477881)
![Project Setting up DHCP](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/47a46344-d0fa-4397-b7ac-2f6ba1df1838)
![Project DHCP Scope is now added](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/82d1fd7f-c94e-400e-b743-d158c8efa58d)

## Step 8: Disabling Internet Explorer Enhanced Security Configuration
![Project Disabling IE enhanced security config](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/ed300a96-810d-43ea-96e3-d5986656657a)

## Step 9: Creating Users
![Project Creating users](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/5138af55-fa6a-479b-87ab-cf1925980317)
![Project AD  Users success](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/bb5363bd-305e-418d-ac5f-3806b90c5679)

## Step 10: Adding Users to an Organizational Unit Named Finance
![Project Finance](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/c100a15a-41e6-46f9-95a7-fc99c8fcf63a)
![Project Finance users added](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/c9e9155b-95a2-4d15-acc8-db2662046d90)

## Step 11: Adding Users to an Organizational Unit Named HR
![Project HR](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/0204ace6-b0e9-4f20-8f5f-a95a6564dc5b)
![Project HR user added](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/625d4799-7913-42e1-957d-06039042d8f7)

## Step 12: Adding Users to an Organizational Unit Named IT
![Project IT success](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/3d9457a7-61e2-4bfd-9f43-9aa6ae0f5a07)
![Project IT users](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/d23e43e1-a55c-463d-9267-957c826bcc00)

## Step 13: Adding Users to an Organizational Unit Named Marketing
![Project Marketing powershell](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/034eeb20-696f-4be4-85a4-59b340847753)

![Project Marketing users](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/6264548b-bf1f-4b7a-86cc-5742263fb049)

## Step 14: Adding Users to an Organizational Unit Named Sales
![Project Sales success](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/8c226bf7-a824-4e20-bd89-c8736f3606ac)
![Project Sales users](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/f4c4f808-5dc1-4923-abda-ab5d002c3fa0)

## Step 15: Renaming the PC and Connecting it to the Domain(DC-2022)
![joining the domain](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/011cd3a6-cc68-4f19-8e15-98f74a74148c)
![proof of connection between the devices](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/f501add9-b167-45b5-b360-bc26b84e8a1f)
![proof in AD](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/bdea3fec-9506-46bf-b7ff-30a27791ad76)
![proof of user success](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/501495cc-d9bc-40a5-85f5-32d84980b58c)

## GPO
# Enabling User Accounts
![PScript_Enable](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/fdb596bd-a96b-49ab-ad46-6607806756f9)
![Account_Enabled](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/5c933df5-8b40-4242-8bc9-0bc6046a8ca3)

# GPO for Password Management
![Password_Man](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/f36860fe-5f52-411d-8969-5f93affd2fb4)

# GPO for Account Lockout
![Account-Lockout-Policies](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/afd64cba-4993-4c17-b365-225f87a798be)

# All GPOs
![GPO](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/6a18fbb4-3de4-4ab5-8300-d7d789dafd88)

# Powershell Script
![enum_acls ps1](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/44282eeb-c0d3-444f-ac4b-431a2163f067)
