# OS-Hardening-Strengthening-a-Linux-System-s-Defences

<h2>Description</h2>

This project involved taking a standard Ubuntu Linux installation and applying various hardening techniques to significantly improve its security posture. OS hardening is the process of reducing a system's attack surface by removing unnecessary features, configuring secure settings, and applying best practices. This hands-on experience demonstrates my ability to proactively protect operating systems from common threats, a crucial skill for any Junior Security Analyst.

<h2>Objective</h2>

This project involved setting up a fresh Ubuntu Linux virtual machine and applying essential security configurations to harden the system. Key tasks included disabling unnecessary services to reduce the attack surface, securing remote access (particularly SSH), enabling automatic updates for ongoing maintenance, and documenting each step with explanations of its security benefits.

<h2>Tools & Technologies Used</h2>

* **Virtualization Software: Oracle VirtualBox, Google Cloud.**
* **Operating System: Ubuntu Desktop server.**
* **Linux Commands: sudo, apt, ufw, passwd, useradd, deluser, systemctl, sshd_config, crontab (and basic text editors like nano).**
* **SSH Client: For remote connection.**

<h2>Program walk-through:</h2>

<p align="center">
Step 1: Setting Up Your Safe Lab Environment <br/>
Created an Ubuntu Desktop VM in Oracle VirtualBox.

<img src="https://github.com/user-attachments/assets/a0a27619-d02e-42de-8d7a-87292d655c84" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
Step 2: Secure Shell (SSH) Hardening <br/>
SSH is often the primary method for remotely managing Linux servers. Hardening it prevents unauthorized remote access. 
  
<img src="https://github.com/user-attachments/assets/025ecfd5-3a14-412f-a9ae-881f641a6aab" width="653" alt="Step 1 Screenshot"/>
<br />
Change Default SSH Port.Find the line #Port 22. Uncomment it (remove #) and change 22 to a non-standard port
  
<img src="https://github.com/user-attachments/assets/43840b21-b5ea-472c-91c1-f9720b733b5d" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
2.1 Disable Root Login via SSH <br/>
In the same sshd_config file, find PermitRootLogin. Change its value to no.
<img src="https://github.com/user-attachments/assets/4a2eab64-6566-4384-bb46-86e5b0db10dc" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
Step 3: Save and Restart SSH Service. <br/>
Restart the SSH service for changes to take effect. Reduces the risk of brute-force attacks and unauthorised remote access.
<img src="https://github.com/user-attachments/assets/f7d4ec45-7fc0-4a6f-9d9b-998fae0cd7d1" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
Step 4: Firewall Configuration (UFW) <br/>
Enabled and configured the Uncomplicated Firewall (UFW) to only allow necessary network traffic, blocking everything else by default.
<img src="https://github.com/user-attachments/assets/f9067d9f-099b-4bfe-92e6-58716886f894" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
4.1 Set Default Policies (Deny All Incoming, Allow All Outgoing)<br/>
<img src="https://github.com/user-attachments/assets/73e50d05-c3e0-4fc4-8827-d9f49a5fccdf" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
4.2 Allow SSH (Crucial! Use your NEW SSH port if you changed it): <br/>
<img src="https://github.com/user-attachments/assets/b451ea47-47ec-4ba5-b3c0-1a42c80c1b48" width="653" alt="Step 1 Screenshot"/>
<br />
  
<p align="center">
4.3 Enable UFW <br/>
<img src="https://github.com/user-attachments/assets/a8fbc73a-5703-43c9-b055-49e1ec07f16c" width="653" alt="Step 1 Screenshot"/>
<br />  


<p align="center">
4.4 Check UFW Status <br/>
<img src="https://github.com/user-attachments/assets/8a13d7e3-9058-45e0-b704-555ff4f0a8ce" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
Step 5:Removing Unnecessary Services <br/>
Identified and disabled services that are not required for the VM's purpose, as every running service is a potential vulnerability.
<img src="https://github.com/user-attachments/assets/322aa2ad-3b98-46cd-8bab-fd674eec4299" width="653" alt="Step 1 Screenshot"/>
<br />

<p align="center">
Step 6:Automating Security Updates <br/>
Configured the system to automatically install security updates, ensuring the VM remains patched against new threats.
<img src="https://github.com/user-attachments/assets/df37e19f-808b-4d22-a217-5294a1aca29c" width="653" alt="Step 1 Screenshot"/>
<br />
---


<h2>Key Learnings & Takeaways:</h2>

* **Proactive Security Mindset: Understood that hardening is a proactive approach to cybersecurity, reducing risks before an attack occurs.**
* **Attack Surface Reduction: Learned the importance of minimising the number of open ports, running services, and unnecessary software to limit potential entry points for attackers.**
* **Layered Security: Recognised how OS hardening forms a critical layer of defence, complementing network firewalls and other security controls.**
* **Linux Security Fundamentals: Gained practical experience with essential Linux commands and configuration files (sshd_config, ufw) for securing a system.**
* **Principle of Least Privilege in Action: Applied this principle by restricting user access and disabling unnecessary features.**
* **Importance of Updates: Reinforced the continuous need for patching and updating systems to maintain security.**
* **Controlled Environment Practice: Developed skills in safely experimenting with security configurations in an isolated VM.**
