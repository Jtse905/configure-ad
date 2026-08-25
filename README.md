# configure-ad
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- Configured Azure Virtual Machines
 - Created a Domain Controller Server virtual machine 
 - Created a Client virtual machine 


<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Active Directory
- Join a computer to the domain
- Create users
- Log in with a created user

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1603" height="833" alt="1GrabDomainControllerVMPublicIP" src="https://github.com/user-attachments/assets/256a93a6-9c9f-4436-a5af-5a3fdbf205c0" />
</p>
<p>
The first step is to log into the Domain Controller Virtual Machine. Copy its public IP address. 
</p>
<br />

<p>
<img width="449" height="302" alt="2LogIntoDomainController" src="https://github.com/user-attachments/assets/e2a0b02e-8f27-4ad9-a7ce-4edabef9f4a2" />
</p>
<p>
Using the Domain Controllers public IP address, connect to it remotely. 
</p>
<br />

<p>
<img width="2560" height="1440" alt="3InServerManagerClickOnAddRolesAndFeaturesinthemiddle" src="https://github.com/user-attachments/assets/69c9000d-bcec-4a24-be7d-ddfa080ab1e0" />
</p>
<p>
In the Domain Controller virtual machine, in the Server Manager Dashboard click "Add roles and features".
</p>
<br />

<p>
<img width="1665" height="1087" alt="4HitNext" src="https://github.com/user-attachments/assets/1b4dd17c-385b-47b9-994e-8d85dae501f5" />
<img width="1666" height="1111" alt="5HitNextAgain" src="https://github.com/user-attachments/assets/258dcb6b-41be-416f-8ca8-789c2cfab118" />

</p>
<p>
Click next, and make sure the "role based" option is selected and click next. 
</p>
<br />

<p>
<img width="1121" height="1023" alt="6Thereshouldonlybveoneserverhitnext" src="https://github.com/user-attachments/assets/56884e0a-15a2-460b-bee9-0a1eaa1c2e1a" />
</p>
<p>
There should only be one option available in the server pool list. Make sure your server is selected and click next. 
</p>
<br />

<p>
<img width="1105" height="1019" alt="7Clicktheboxnexttoactivedirectoryservices" src="https://github.com/user-attachments/assets/f0f3469b-ba55-4c21-8b5c-d84102fdb10d" />
</p>
<p>
In the next screen, check the box next to "Active Directory Domain Services" option. 
</p>
<br />

<p>
<img width="1177" height="1073" alt="8CCLickAddFeatures" src="https://github.com/user-attachments/assets/ebaf3372-6949-4d37-b3f0-a484c664b1ae" />
</p>
<p>
Click on the "Add features box" to enable Active Directory Domain Services. Then click next. 
</p>
<br />

<p>
<img width="1111" height="1018" alt="10Checktheboxthatsaysrestartifrequiredandhitinstall" src="https://github.com/user-attachments/assets/59e04638-ed6a-4130-a16c-e25b6cf64f8c" />
</p>
<p>
Click the box at the top to allow the process to restart the destination server if needed. Then click on install to install Active Directory. 
</p>
<br />

<p>
<img width="2073" height="1017" alt="11Clicktheyellowflagandclickaddasdomaincontroller" src="https://github.com/user-attachments/assets/62e918f9-d7e0-4ea4-980d-855ba041281a" />
</p>
<p>
Now that Active Directory is installed, in the Server Manager Dashboard click on the flag on the top right corner. Then click on "Promote this server to a domain controller". 
</p>
<br />

<p>
<img width="1426" height="1017" alt="12UncheckDNSDelegationAndClickNextandnext" src="https://github.com/user-attachments/assets/a40e615d-2b0b-4247-98b2-8f1c9d4a0206" />
</p>
<p>
Inside the box for "NetBIOS Domain Name" create your domain name. For this lab, I used mydomain.com. Once its named click next. 
</p>
<br />

<p>
<img width="1526" height="1020" alt="13next" src="https://github.com/user-attachments/assets/b85061c0-64a2-451c-9a03-0eb9e11aee50" />
<img width="1480" height="1014" alt="14nexttt" src="https://github.com/user-attachments/assets/de73a5ea-c498-4d2c-826e-2a93dc1827d9" />

</p>
<p>
Click next and next. 
</p>
<br />

<p>
<img width="1345" height="1014" alt="15installactivedirectory" src="https://github.com/user-attachments/assets/7c592cc9-08f7-4de6-b520-7872274a1054" />
</p>
<p>
When the perquisite check list passes, go ahead and click install. 
</p>
<br />

<p>
<img width="473" height="588" alt="16LogBackIntoDCAsDomaiNUser" src="https://github.com/user-attachments/assets/dfde1c2f-1bc2-4029-a763-cd4604af83e2" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1083" height="1247" alt="17OpenADUsersAndComouters" src="https://github.com/user-attachments/assets/1062eb6c-900d-401e-8189-ec64e0244d21" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1144" height="804" alt="18RightClickmyDomainAndClickNewThenOrganizaitonalUnit" src="https://github.com/user-attachments/assets/c7619f92-3fb2-4011-ac28-02bbb8c6073e" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1131" height="814" alt="19NameitUnderscoreEmployees" src="https://github.com/user-attachments/assets/a74b5608-9ef3-4e71-a3f5-7f3fdfb592d9" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1132" height="791" alt="20CreateNewOUCalledUnderscoreAdmins" src="https://github.com/user-attachments/assets/baa2ee36-d1b5-4480-948f-81bdb35f32e2" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1117" height="814" alt="21CreateNewUserInAdminGroupCalledJaneDoe" src="https://github.com/user-attachments/assets/edd76686-149c-43c0-88e6-6178abed70a4" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1113" height="790" alt="22CreateJaneDoeAccount" src="https://github.com/user-attachments/assets/e0630f3f-054f-4287-98ff-29ee52e4b441" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1106" height="789" alt="23RightClickJaneDoeAndCLickProperties" src="https://github.com/user-attachments/assets/0346bbb2-e1d1-462c-a081-a5396357c7e0" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1114" height="771" alt="24GoToMemberOfAndClickAdd" src="https://github.com/user-attachments/assets/c5bf01ca-59ff-4550-b2ca-c0a417568e76" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1111" height="792" alt="25TypeinDomainAdminsAndClickCheckNamesThenOkayThenApplyAndOkay" src="https://github.com/user-attachments/assets/6025070b-4c46-4346-b42e-0edf93e7578c" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="494" height="587" alt="26LogIntoDC1AsJaneAdminAccountYouCreated" src="https://github.com/user-attachments/assets/01ef7672-e503-4c06-b6c7-4500990174ca" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="423" height="273" alt="27OnceLoggedIntoJaneAdminAccountRemoteDesktopIntoCLIENT1VM" src="https://github.com/user-attachments/assets/0733493a-7189-498e-a895-91f6a512b694" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="634" height="723" alt="28RightClickStartbuttonAndClickSystem" src="https://github.com/user-attachments/assets/9475722f-df58-40d6-8120-8bed6dc47bdc" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1277" height="980" alt="29ClickRenameThisPCAdvancedontherightside" src="https://github.com/user-attachments/assets/bc72f337-d59b-4eb0-b886-997543756f71" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1276" height="997" alt="30UnderCOmputerNameTabClickChange" src="https://github.com/user-attachments/assets/df8dd714-31c0-43e1-ad91-f6acddb7a95b" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1234" height="976" alt="31enterthedomainyoucreatedinthislabitsmydomaincom" src="https://github.com/user-attachments/assets/0b337f76-027c-4cdf-bf4f-5086173482dc" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1233" height="962" alt="32LogIntoJaneAdminAccountWhenPrompted" src="https://github.com/user-attachments/assets/499f70d6-2e72-4640-90b0-d98599a8e22e" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1225" height="966" alt="33ShouldBeScucessful" src="https://github.com/user-attachments/assets/88ab2de4-4345-411a-90ac-288dd8935b55" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="865" height="756" alt="34InDC1GoToADUsers" src="https://github.com/user-attachments/assets/b019bc33-0591-41de-b4cf-2c0d2cc153a3" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1949" height="1066" alt="35ClickComputersinMyDomaiNAndYouCanseeTheClient1MachineWeAdded" src="https://github.com/user-attachments/assets/4e291b3e-3adf-4a54-9ad4-dd3b34dbe7c0" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

