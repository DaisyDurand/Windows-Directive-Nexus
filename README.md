# Windows-Directive-Nexus
## Description
This project entails deploying a Windows Server 2022 ISO alongside a Windows 11 ISO within an Oracle VirtualBox environment. The server operates as the domain controller, housing active directory functionalities. Two network adapters are utilized: one interfaces with the internet, while the other connects to the private network. Internal network IP addresses are assigned, while the external network automatically obtains an IP address from the home network. NAT and RAS configurations enable clients on the private network to access the internet via the domain controller. DHCP is implemented on the domain controller to automate IP address allocation for the Windows 11 deployment. A Python script manages user creation and organizational placement. The Windows 11 machine is seamlessly integrated into the server. User accounts are pre-established, facilitating user login to the machine. 

## Environments Used
* Windows Server 2022 ISO
* Windows 11 ISO
* Oracle VM
## Network Diagram

This is based off of Josh Madakor's version. The only thing that has changed is the Server 2022 and the Windows 11 machine.

![Network Diagram](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/8dfc1bf7-649f-478a-a091-c675b98ca3ae)

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
![Project 1 Creating an admin users](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/51d78813-8bfc-4de8-8236-f4502695b42a)
![Project 1 Add user to member of domain admins](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/6a311385-71f1-4d18-8c1b-ac4bab51f85d)
![Project 1 User added ](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/39cea954-f471-4118-abbb-d01f45529398)

## Step 5: Installing Remote Access and Routing
![Project adding remot access](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/591ff34e-f816-475c-87cd-f1312f64cd91)
![Project remote access](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/a3ebbb13-0ac8-48c9-b978-9e0387a4c5a2)

## IMPORTANT COMPUTER NAME IN WRONG PLACE
![Project Computer name](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/19b858b0-6ab9-40f2-9d0d-60bce8826a21)

## Step 6: Network Address Translation (NAT) Installation
![Project configuring remote access server](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/35f7c630-3865-4b3d-ad96-4738e887732f)
![Project configuring remote access summary](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/4949a30c-e25a-4440-bb61-f300be0c35ff)

## Step 7: DHCP Installation
![Project Installing DHCP](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/fc1173ac-4e5d-4164-8b4d-a46c91477881)
![Project Setting up DHCP](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/47a46344-d0fa-4397-b7ac-2f6ba1df1838)
![Project DHCP Scope is now added](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/82d1fd7f-c94e-400e-b743-d158c8efa58d)

## Step 8: Disabling Internet Explorer Enhance Security Configuration
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

## Step 15: Connecting The Windows 11 ISO to the Server (DC-2022)
![connecting win to server](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/cd42c338-9ecf-4dab-a6d9-d09908b7db2c)
![User](https://github.com/DaisyDurand/Windows-Directive-Nexus/assets/147094227/0b1f53ba-0c8a-42af-9c9b-d1fa821300cb)
