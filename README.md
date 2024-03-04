# Window Server 2022 AD Setup
There are two ways that we can set this up via Windows Powershell or Graphical User Interface. In this setup, we'll be setting it up via Graphical User Interface. 

Step 1: Start up your Windows Server in Oracle VM VirtualBox Manager or any VM you choose. If you haven't set this up yet, please take a look at this x. 

![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/0cbb0eaa-51c5-4e08-8d33-f11d3ecfd6a7)

Step 2: Start up your Server Manager and on the top right, click Manage -> Add Roles and Features. 

![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/40b314ff-a940-4f45-92cb-ce60aee8b45e)

Step 3: Run through the Wizard. 

- Step 3a: "Role-based or feature-based" or "Remote Desktop Services Installation". Which one should you select?
  
Role-based or feature-based installation is for setting up specific server roles or features. So, in this case, we are selecting specific server roles or features that you want the system to perform or have. This cloud includes Web hosting, DNS Servers, or file sharing. On the other hand, Remote Desktop Services installation is used to set up the server to allow remote users to access applications and services. This would enable a user to interact with the system from a different location as if they were physically present at the system. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/386abc51-8a02-4f19-ad7d-ecde9103426a)
- Step 3b: Select the Server you're working with and one you'd like to install AD & DNS Server on. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/0af9d17b-c7d7-40b7-80b0-c94941a31cd8)
- Step 3c: Select the Server Roles Active Directory Domain Services & DNS Server 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/7267b753-9b7a-4b0b-b779-deb288f4d6cb)
- Step 3d: By default Group Policy Management and .NET Frame 4.8 Features (2 of 7 installed) are selected. If they're not please select them. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/3b9851df-a50a-4307-9a9c-b14027a59a28)
- Step 3e: Select Next. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/bffda8d8-4f5c-4950-8bfe-e5e5cb1b5e2e)
- Step 3f: Select Next. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/d70efb7f-e1e3-4005-90bc-cf63574404b7)
- Step 3g: Select Next. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/476bc5d4-a9e8-4f36-9c6f-dfb15de0c928)
- Step 3h: Wait for the Feature installation to finish. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/c151d6d4-51f7-48f1-99eb-96cb75bc7bd2)

Step 4: Now that the installation of AD and DNS Server is finished follow the Deployment Configuration. Go back to Server Manager and to get to Deployment Configuration Click on the Flag with a yellow icon at the top right, on the left side of "Manage". This will bring up the Active Directory Domain Services Configuration Wizard. 

- Step 4a: Select new forest & give it a Root domain name.

Root domain name format: [prefix].[name].[suffix] and we going to select "Add a new forest" because the first domain you deploy in an Active Directory forest is called the forest root domain. This domain remains the forest root domain for the life cycle of the AD DS deployment. 

More information on creating the Root domain name: "https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/selecting-the-forest-root-domain"

![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/d2fc82cd-ee55-47f5-8b23-2298ca608924)
- Step 4b: Give it a DSRM password

Forest & Domain functional levels select Windows Server 2016. Why? Functional levels determine the available Active Directory Domain Services (AD DS) domain or forest capabilities. They also determine which Windows Server operating systems you can run on domain controllers in the domain or forest. However, functional levels do not affect which operating systems you can run on workstations and member servers that are joined to the domain or forest. 

When you deploy AD DS, set the domain and forest functional levels to be the highest value that your environment can support. This way, you can use as many AD DS features as possible. When you deploy a new forest, you are prompted to set the forest functional level and then set the domain functional level. You can set the domain functional level to a value that is higher than the forest functional level, you cannot set the domain functional level to a value that is lower than the forest functional level. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/733401c1-242f-4fd8-9b7d-e6e9d2d067b3)
- Step 4c: Next, don't worry about creating DNS delegation. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/bdccf290-a3bf-45d4-bd65-111fc063839b)
- Step 4d: By default the NetBIOS domain name is AD, and this can be changed. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/158ec483-e82d-4746-baae-88240eab7671)
- Step 4e: This shows the Database folder, Log files, and SYSVOL Folder locations. Click Next. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/e9ffc81c-1a2e-4101-ad49-8cbcf47b422e)
- Step 4f: Review the Options you selected. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/90810765-49a6-4485-86e6-d60cbeef30f5)
- Step 4g: If you click on review script, this is useful if you're setting up via the command line. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/19714b08-b025-4814-8ea2-a2efc3e7d114)
- Step 4h: Run the installation. 
![image](https://github.com/Kokimchi/Window-Server-2022-AD-Setup/assets/23605674/a4dc4cc9-3287-41f8-a332-aee334bec557)















