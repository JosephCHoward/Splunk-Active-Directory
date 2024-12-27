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




