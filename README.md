
![image](https://github.com/user-attachments/assets/4af18c7d-5a55-496e-b5cb-1d8c120bde1f)



<h1>Network File Shares and Permissions </h1>
In this tutorial, we observe sharing resources over the network. Creating File Shares to allow Read, Write, or Deny access to individual users or groups.  <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- connect/log on dc-1 as "Jane Doe" our admin user
- connect/log on client 1 as any normal user
- on dc-1 as your admin user create 4 folders "read-access", "write-access", "no-access" and "accounting"
- create different group access for all of the folders

<h2>Actions and Observations</h2>

![image](https://github.com/user-attachments/assets/ed50af62-d732-483a-9246-0bb045177259)
![image](https://github.com/user-attachments/assets/f09aa3ab-dc91-4777-a4ee-811abb5bd41b)


<p>
Log into DC-1, and grab a random employee under the "_employee" OU. Find their password and write it down. Then log on to that specific log-in and password on Client-1. Once logged into the DC-1 and Client 1 VMs in DC-1 create four folders in File Explorer under Windows C: drive. The four folder titles should be "read-access", "write-access", "no-access" and "accounting". On each folder that was created right click on the folder go to properties-> sharing -> share and in the search bar type domain users and select the different folder access you want to give the "read-access" folder read-only properties and with "write-access" you want to provide the domain with users read/write properties. For the "no-access" folder give read/write properties to the domain admin group only. Skip the accounting folder for right now.
    
</p>
<br />

![image](https://github.com/user-attachments/assets/5242e0b4-8beb-4220-b523-3d5d83e680c1)
![image](https://github.com/user-attachments/assets/ea716ae5-1287-430f-ac3a-fa85414efcc4)




<p>
Once all the folder permissions are granted, go to Client-1 and attempt to access all the folders as a normal user. With the "read-access" folder try to create a new folder after accessing it, the same with the "write-access" folder, and "no-access" folder. You should receive errors noting that you can't edit the read-only folder, and do not have the correct permission to access the "no-access" folder. While, being able to open and create text files in the "write-acccess" folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
