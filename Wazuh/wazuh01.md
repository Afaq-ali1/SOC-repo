
AFAQ ALI	SOC ANALYST INTERNSHIP	TASK 3
SOC – Task 1: Install SIEM & Collect Logs 
What is SOC?
A Security Operations Center (SOC) is a centralized team responsible for monitoring, detecting, analyzing, and responding to cybersecurity threats within an organization.
The SOC continuously monitors systems, networks, and applications to identify suspicious activities, security incidents, and potential attacks. Security analysts use specialized tools to investigate alerts and respond quickly to reduce the impact of cyber threats.
The main goals of a SOC include:
•	Monitoring security events
•	Detecting cyber threats
•	Responding to incidents
•	Protecting organizational data and systems
SOC teams work 24/7 to ensure the security and availability of critical infrastructure.

Why Organizations Use SIEM for Monitoring
A SIEM (Security Information and Event Management) system collects and analyzes logs from multiple sources such as servers, applications, network devices, and security tools.
SIEM helps organizations by:
•	Centralizing logs from different systems
•	Detecting suspicious activity
•	Identifying security incidents
•	Providing real-time monitoring
•	Supporting incident response
For example, a SIEM can detect:
•	Multiple failed login attempts
•	Unauthorized access attempts
•	Malware activity
•	Suspicious system behavior
By analyzing logs and generating alerts, SIEM tools help SOC analysts quickly identify and respond to security threats.
https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html
Screenshots
1.	Wazuh Dashboard Overview
•	Wazuh Login Page
 
•	Wazuh dashboard home page.
 




2.	Agents Page (showing Windows agent status: Active)
 
3.	Threat Hunting → Events page showing collected logs
 





Added filter of authentication failed
 
Logon event logs
 
Logoff event logs
 
SIEM Setup
For this lab, the open-source SIEM platform Wazuh was installed in a virtual machine using VMware. Wazuh provides log collection, threat detection, and security monitoring capabilities through a centralized dashboard. After installation, the Wazuh web interface was accessed through a browser using the server’s IP address.
Example access URL:
https://192.168.0.109
The Wazuh platform includes several important components:
•	Wazuh Manager – analyzes and processes security logs
•	Wazuh Dashboard – provides a graphical interface for monitoring events
•	Indexer – stores and organizes collected log data
These components work together to provide centralized visibility of security events across systems.
Log Collection Configuration
To collect logs from a Windows system, the Wazuh agent was installed on a Windows machine. The agent was configured to communicate with the Wazuh server using the server IP address. Once installed, the agent began collecting Windows Event Logs and forwarding them to the SIEM.
The logs collected from the Windows system included:
•	Application logs
•	Security logs
•	System logs
The Windows system appeared in the Wazuh dashboard under the Agents section with the status Active, confirming successful communication between the agent and the SIEM server.
Generating and Monitoring Logs
To generate sample security events, several activities were performed on the Windows machine such as user login, failed login attempts, and running command-line commands. These activities generated Windows Event Logs that were automatically sent to the Wazuh server.
The collected logs were viewed through the Threat Hunting → Events section of the Wazuh dashboard. This section displayed detailed information about each event including the timestamp, agent name, rule description, and severity level. The presence of these logs confirmed that the SIEM system was successfully collecting and analyzing security events.
Conclusion
This lab demonstrated the basic setup and functionality of a SIEM system in a SOC environment. By installing Wazuh and configuring a Windows agent, security logs were successfully collected and monitored in a centralized dashboard. SIEM platforms are essential tools for SOC analysts because they help detect suspicious activity, investigate incidents, and improve overall security monitoring within an organization.
