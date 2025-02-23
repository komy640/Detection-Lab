# Soc Home Lab Using Splunk

## Objective

The purpose of this project was to create a controlled lab environment for simulating and identifying cyber threats. The main goal was to collect and analyze logs within a Security Information and Event Management (SIEM) system, generating test data to replicate real-world attack scenarios.

### Skills Learned

- In-depth knowledge of SIEM principles and real-world implementation.
- Expertise in examining and interpreting security logs.
- Ability to detect and analyze attack patterns and indicators.
- Improved understanding of network protocols and system vulnerabilities.
- Strengthened analytical thinking and problem-solving abilities in cybersecurity.

### Tools Used

- SIEM (Splunk Server) – Used for log ingestion and analysis.
- Splunk Universal Forwarder – Installed on endpoints to forward logs.
- Sysmon (System Monitor) – Configured on Windows machines for detailed event logging.
- Atomic Red Team – Simulating cyber threats.
- Kali Linux – Used as an attacker machine for testing security defenses.

 ### Network Diagram
 ![WhatsApp Image 2025-02-23 at 01 30 15_3a5cc757](https://github.com/user-attachments/assets/980d53fb-071e-40e8-88a5-3cb7c6e404c7)


The lab environment consists of:
- Windows Machines (192.168.1.101, 192.168.1.102) running Sysmon and Splunk Universal Forwarder.
- Active Directory Server (192.168.1.100) forwarding security logs.
- Splunk Server (192.168.1.200) acting as the SIEM.
- Attacker Machine (192.168.1.250, Kali Linux) used for simulating attacks.


## Steps
 - Step 1: Configure Windows Machines
Install Sysmon for advanced system logging.
![image](https://github.com/user-attachments/assets/55c5a44d-4fc4-4931-9fc3-9b9d444c53df)
![image](https://github.com/user-attachments/assets/e2b02f54-b47e-4e24-b69b-ccb00d9e945b)


Install Splunk Universal Forwarder to send logs to Splunk.
powershell
Copy
Edit
msiexec /i splunkforwarder.msi AGREETOLICENSE=Yes
- Step 2: Set Up Active Directory
Install Windows Server and configure it as a Domain Controller.
Install Sysmon & Splunk Universal Forwarder to forward security logs.
- Step 3: Deploy Splunk Server
Install Splunk on 192.168.1.200.
Configure Splunk Forwarders on Windows and Active Directory machines to send logs.
- Step 4: Set Up Kali Linux Attacker
Install penetration testing tools.

sudo apt update && sudo apt install -y kali-linux-default
Prepare for attack simulations using Atomic Red Team.

