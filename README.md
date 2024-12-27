# Splunk, Active Directory & Atomic Red Team Lab

Instructional videos for this project can be found in a 5-part series on the <a href = "https://www.youtube.com/@MyDFIR">MyDFIR YouTube channel</a>. The video for part 1 is <a href = "https://www.youtube.com/watch?v=5OessbOgyEo&list=PLG6KGSNK4PuBWmX9NykU0wnWamjxdKhDJ&index=13"> here</a>. 

This project was done using VirtualBox and 4 virtual machines in a NAT network. The main components of the project are:
- Windows Server 2022
  - Install Active Directory services on a Windows 2022 server and create users.
  - Install and configure Splunk Universal Forwarder.
  - Install and configure Sysmon to forward events to Splunk.
- Splunk Server
  - Install and configure Splunk to receive logs from the Windows server and Windows workstation.
  - Use Splunk to identify attacks in forwarded logs.
- Windows 10 Workstation
  - Add the Windows 10 workstation to the Active Directory domain.
  - Install and configure Splunk Universal Forwarder.
  - Install and configure Sysmon to forward events to Splunk.
  - Install Atomic Red Team to simulate MITRE ATT&CK techniques.
- Kali Linux
  - Conduct brute force attack on Windows 10 workstation using Crowbar.

## Network Topology

![image](https://github.com/user-attachments/assets/836ee6c5-181e-44c7-a3c9-177003537912)

## Project Highlights

### Splunk Server

Splunk was installed and configured on a VM running Ubuntu Server 24.04.1. A static IP of 10.0.10.10 was set by modifying the /etc/netplan/50-cloud-init.yaml file. NOTE: Indentations in the yaml file are important!

![image](https://github.com/user-attachments/assets/cb062583-c9ab-4cc9-b6dd-a8ea7624ae40)

The static IP address is applied to the server:

![image](https://github.com/user-attachments/assets/6577b496-4ac2-46f4-821c-6c0d8f072b0a)

Splunk is configured to listen on port 9997 and the Splunk interface is accessed on port 8000. An "endpoint" index is created to receive logs forwarded from the Active Directory server and the Windows workstation.




### Active Directory Server
Active Directory services were installed and a domain created (lab.local). A "Workstations" organizational unit was created and the Windows 10 workstation added to it.

![image](https://github.com/user-attachments/assets/b56fad45-ac03-4667-b439-9df2b56c34cc)

Organizational units were created for IT and HR and two users added to each unit.

![image](https://github.com/user-attachments/assets/8d8d0250-283f-402a-b5bd-87b3bead550d)



