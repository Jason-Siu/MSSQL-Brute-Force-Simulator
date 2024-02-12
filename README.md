# MSSQL-Brute-Force-Simulator

## Overview
This PowerShell script demonstrates a simulated brute force attack against an MS SQL Server instance. It intentionally tries incorrect passwords in order to create an incident in Microsoft Sentinel (SIEM), showcasing security vulnerabilities and the importance of robust authentication practices.

## Features
 - Brute Force Simulation: The script attempts to log in multiple times.
 - Customizable Parameters: Easily modify server name, database name, username, and password.
 - Ethical Use: Intended for ethical hacking and educational purposes.

## Implementation
I used an attacker virtual machine located in India. To create this, I simply just created a new VM from within Azure to use. The Attacker VM's IP address is 98.70.13.69, which will be shown inside of Microsoft Sentinel, which is our SIEM.

Upon running the brute force script multiple times, we can observe the incidents occurred here:
![image](https://github.com/Jason-Siu/MSSQL-Brute-Force-Simulator/assets/34889726/493310ff-6a41-40cc-80e2-b3fdac8ae958)

And by going into more detail by running KQL on our workspace (it's the same rules as our incident), we can see that there are more entities than just my attack VM, indicating other hackers have tried to logon to the system.
![image](https://github.com/Jason-Siu/MSSQL-Brute-Force-Simulator/assets/34889726/b8ea277d-8c1d-4ced-aa26-d8a373f1fbc1)

## Threat Map

![image](https://github.com/Jason-Siu/MSSQL-Brute-Force-Simulator/assets/34889726/9c07a8b5-cddc-4c23-b936-f484992c1727)

## Conclusion

In conclusion, this MSSQL Brute Force Script serves as a powerful demonstration of the security vulnerabilities that can exist within an organization’s authentication systems. By intentionally attempting incorrect passwords before successfully logging in, it highlights the importance of robust security measures and the need for continuous monitoring and improvement.
