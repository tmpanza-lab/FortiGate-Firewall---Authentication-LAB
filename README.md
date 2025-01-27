# FortiGate Firewall - Authentication LAB

## Objective

The FortiGate FW - Routing & Security Profiles Lab project is aimed to demonstrate and practice configuring various authentication methods available in a FortiGate firewall to authenticate users and manage access to the network resources.


### Skills Learned

- Authentication Configuration Skills
- Access Control Policy Management
- Troubleshooting Authentication Issues
- Network and Security Design
- Practical Experience with FortiOS Features

### Soft-Skills Developed

- Problem-solving: Identifying and addressing authentication issues.
- Critical thinking: Designing secure and efficient authentication solutions tailored to the organization's needs.
- Collaboration: Working with IT teams to integrate authentication systems like LDAP or domain controllers.


### Tools Used

- FortiGate VM: A virtual appliance used in virtualized environments, such as VMware or Hyper-V
- FortiOS Web Interface (GUI)
- FortiOS Command Line Interface (CLI)
- FortiView Dashboard: Built-in monitoring tool for real-time traffic and event analysis.
- Backup and Restore Tools
- FTP/HTTP/HTTPS Servers: For uploading firmware or serving configurations during the lab.
- Traffic Generation Tools
- GNS3 for simulated network devices (e.g., routers, PCs, or switches) to test


*Ref 1: Network Diagram*
![image](https://github.com/user-attachments/assets/fc7eb2f1-c679-43a7-9cb9-d30f936f4a9f)


## STEPS

## Local Users Creation ##
![image](https://github.com/user-attachments/assets/6042513e-b494-4c3e-a8b1-ed07578c6026)
![image](https://github.com/user-attachments/assets/efbcfc0b-988b-452d-9e0f-a71b96ba2c85)
 
 
## Local Groups Creation ##
![image](https://github.com/user-attachments/assets/36841c4f-80f5-4041-95b9-f2055694fc62)
![image](https://github.com/user-attachments/assets/ac806c7a-9aaa-4f36-84f8-955fc673a937)
 
 
Now my users are created and my group is created.
I will go to police and object then firewall policy I will choose my internet group, which my user one is assigned by doing that, only authenticated user can have access to Internet.
![image](https://github.com/user-attachments/assets/0b790616-6340-47a2-9298-20004b38ae32)


 

We can only access to Google if we authenticate.

So here it is, the authentication page.
![image](https://github.com/user-attachments/assets/3ea8782e-bde5-4f6c-bdba-c581a5b1c1d3)
![image](https://github.com/user-attachments/assets/1de1d715-6891-40fe-ba4d-186bdd5e15cf)
 
 

From here we can see that our user1 with this IP here, which assign it to this group here, is connected to Internet.

If we want to integrate it, we need to click on it and we cannot consecrate it if we want.
![image](https://github.com/user-attachments/assets/34c7be6a-d546-4a90-91fc-6a0a72070a66)

 


### LDAP INTEGRATION ###

LDAP Authentication is a type of Active auth, that's means that the user need to type his credentials manually.


In this lab we will see how to connect our FortiGate firewall to a LDAP server and use our remote

users that are in our Active Directory server to authenticate with FortiGate Firewall.

*Ref 1: Network Diagram*
![image](https://github.com/user-attachments/assets/94ba07dc-6de8-4993-a1df-4e8e63ce501a)
 


## LDAP Configuration ##


* Method 1
![image](https://github.com/user-attachments/assets/e5a62e96-6128-41ca-b005-98ab72ec8654)
![image](https://github.com/user-attachments/assets/5ad47602-57c4-45a4-a8e4-eeb387a51657)
![image](https://github.com/user-attachments/assets/9f319095-af50-4bfe-a4f4-2a03477283b7)


* Method 2


## Group Creation ##
![image](https://github.com/user-attachments/assets/0110aa98-463f-4e30-a47d-869aaac47dbb)
 

# LDAP Administrator users’ creation
![image](https://github.com/user-attachments/assets/219c256b-a938-47d9-9999-9192fdc80db5)

* Policy


# Show Authenticated users
![image](https://github.com/user-attachments/assets/4fe1cf34-12fe-4e4a-b84b-9e7aa0272f42)
![image](https://github.com/user-attachments/assets/17d3cbc3-74a4-41cd-853f-9058a9bf3a4d)
![image](https://github.com/user-attachments/assets/1db62abc-1590-48fc-baa3-2c191fdbb220)


FSSO = Fortinet Single Sign on Is an agent (Software) must be installed on a domain controller, the agent collects users’ credentials and send them to our FortiGate unit.
![image](https://github.com/user-attachments/assets/29bfa5cb-efa7-4fc4-bf1c-cee8b7b9b3b9)
![image](https://github.com/user-attachments/assets/2cb94034-3c15-4789-be2a-cdf4c1304764)
 

 

FSSO is a type of passive authentication


## FSSO Configuration ##
![image](https://github.com/user-attachments/assets/9f7c0932-13b4-4c89-b21e-365c0286b692)
![image](https://github.com/user-attachments/assets/a7009d9f-f7d8-45e2-8a38-88505640088a)
![image](https://github.com/user-attachments/assets/1e34f037-aaad-4231-9e53-ff680ce22286)
![image](https://github.com/user-attachments/assets/d7f84269-3a4a-458a-ae51-26457351a28f)
 

## FSSO Group Creation ##
![image](https://github.com/user-attachments/assets/5c54b5e9-e460-42ca-a3b6-1cf9bda2be95)
![image](https://github.com/user-attachments/assets/58910612-02f9-4a13-af9b-aae5d28f0f28)
 
 

## Add Group To Policy ##
![image](https://github.com/user-attachments/assets/a9952fd7-228c-43bd-b18d-65eafd287320)
![image](https://github.com/user-attachments/assets/0a5bb7b7-7afe-4253-8c17-49c34e853ea6)
 
 



## FGT_Captive Portal ##

*Ref 1: Network Diagram*
![image](https://github.com/user-attachments/assets/a9b488f7-4027-49ec-8c3f-feaf5cbcbb8e)


# Create The User
![image](https://github.com/user-attachments/assets/2b44e50c-02a9-4d92-b2cd-a527150e7bad)
 

# Create The Group and Assign Users
![image](https://github.com/user-attachments/assets/9c7d029e-9f25-4aa2-a95a-b30eb3ab11a5)
 

# Create The Address Objects
![image](https://github.com/user-attachments/assets/1413cb9a-5e14-4f01-9103-d883f465f2a7)

 
# Create The Exemption Rules
![image](https://github.com/user-attachments/assets/1e61748a-4d45-4170-8602-c71b109c61ff)
![image](https://github.com/user-attachments/assets/1741b6e4-7547-4903-b97f-b7afa68f8dc5)
 
 
# Enable The Captive Portal
![image](https://github.com/user-attachments/assets/4e8bf311-8b47-4fa6-8a5e-a6433ee3aa57)
 

# Create Captive Portal Policy
![image](https://github.com/user-attachments/assets/6ef5db1d-4514-4930-8e26-8198e88554e0)
![image](https://github.com/user-attachments/assets/b6f57700-8e99-40ca-8e0f-06084d6938ac)

 

 










