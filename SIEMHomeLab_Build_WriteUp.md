# SIEM Home Lab Build & Setup Writeup

## Overview
I built a small SIEM home lab using Security Onion in order to get familiar with SIEM environments and their associated tools. 
In addition, I plan to use this lab as a foundation for any additional projects that may require the use of a SIEM environment, or to test new tools that I am unfamiliar with. 
Finally, this experience will better prepare me for SOC and other cybersecurity roles that I will be applying to, and assist me in passing the CompTIA Security+ exam.

## Goal
- VM Management and SIEM skills
- Familiarity with SIEM environments and simulating traffic via a separate VM

## Tools & Environment
- Hypervisor/OS: VMWare Workstation Pro w/ Security Onion 3.1.0
- Key software/tools: Security Onion

## Build Steps
1. Downloaded the latest Security Onion distribution and verified the SHA256 hash against the official Security Onion Solutions website.<br>
2. I then followed the official installation guide from the Security Onion Solutions website and configured the VM to the recommended hardware/network settings.<br>

![VMWare Settings](/images/01-VMWare_Settings.png)
3. After VM configuration was complete, I began the setup process, choosing the Evaluation installation configuration due to the lab's small size.<br>

![Evaluation Installaion Selection](/images/02-Installation_Mode.png)
4. I then configured my network interfaces, chosing ens160 as the NIC used for the management interface and ens192 for the monitor interface.<br>

![NIC Configuration](/images/03-NIC_Config.png)
5. Configured the management interface to use a static IP, verifying there were no other hosts on that IP range, and added credentials to access the web portal later.<br>

![Setup Overview](/images/04-Setup_Overview.png)
6. After completing the setup process, I signed in to the web portal via the IP address I configured earlier.<br>

![Completed Setup](/images/05-Setup_Complete.png)
![Security Onion Webportal](/images/06-Security_Onion_Webportal.png)

## Challenges & How I Solved Them

- One problem that I ran into during the final install process was the VM not being able to reach sigs.securityonion.net while completing setup. 
  The main cause for this was a misconfiguration of the network adapters in the VM settings within VMWare being NAT. 
  In order to fix this I changed both network adapters connection type to Bridged and rebooted Security Onion, fixing the issue. 

## Key Takeaways
From this project I learned how to set up a SIEM environment, familiarized myself with the environment, and prepared the lab for traffic simulation and analysis — covered in the following testing write up.
