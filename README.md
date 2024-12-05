# SOAR(Tines)-EDR(LimaCharlie) Project 
![image](https://github.com/user-attachments/assets/9db49eff-99fa-4f10-84e4-a0c4d14c9218) ![image](https://github.com/user-attachments/assets/344dc903-8cca-4533-a2aa-f5346888e1d2)






## Introduction
Howdy Thank you for taking the time to explore my SOAR-EDR project, which integrates LimaCharlie and Tines. The goal of this project is to demonstrate the critical role of automation in responding to cybersecurity threats in real time.

SOAR stands for Security Orchestration, Automation, and Response, while EDR refers to Endpoint Detection and Response. SOAR is an automation platform used by SOC analysts and security professionals to streamline the detection, investigation, and response to incidents within their environment.

The key distinction between SOAR and a traditional SIEM (Security Information and Event Management) system, such as Splunk, is that SOAR automates response actions. In a SIEM, analysts typically have to manually take actions, such as quarantining compromised systems or investigating alerts. In contrast, SOAR systems automate many of these tasks, enabling SOC analysts to focus on higher-level activities while improving response time and reducing human error.

Integrating a SOAR system into your security operations enhances overall efficiency, reduces risks, and strengthens the ability to mitigate threats effectively.

## Project Overview

In this project, I have developed a workbook that demonstrates the integration of LimaCharlie (our Endpoint Detection and Response, or EDR) with Tines, a security orchestration, automation, and response (SOAR) platform. The objective is to show how LimaCharlie detects malicious software or commands on an endpoint, and how Tines is used to automate the response process.

Upon detection of a threat by LimaCharlie, a notification is triggered to alert relevant stakeholders via Slack and Email. At this point, a user prompt is presented, asking whether the affected machine should be isolated from the network. If the user selects "No," they will receive a message informing them that the machine was not isolated. If "Yes" is selected, the affected machine will be quarantined from the network, effectively containing the threat and reducing potential damage to the environment.


![image](https://github.com/user-attachments/assets/008ed71c-37f2-4582-93e3-c8c9c64cfab4)

## Installation and Persistence Detection with LimaCharlie


In this section, I successfully created my LimaCharlie account and navigated to the Sensor section to copy the sensor installation command for my Windows 11 machine. Using the PowerShell tool, I was able to deploy the sensor on the system. Additionally, I demonstrated how LimaCharlie’s Autoruns feature can be leveraged to detect persistence mechanisms commonly used by adversaries, particularly Advanced Persistent Threats (APTs).

APTs pose a significant risk to organizations, often involving long-term, covert access to systems. Having a tool like LimaCharlie to monitor and identify persistent threats is essential for enhancing an organization’s defense against these advanced attack techniques.
![Screenshot 2024-12-02 221154](https://github.com/user-attachments/assets/a4b108da-1d95-4cce-bd70-9bc9f0973cc3)
![Screenshot 2024-12-02 222704](https://github.com/user-attachments/assets/6e7ee725-b636-47c0-861d-d85362686505)![Screenshot 2024-12-02 222743](https://github.com/user-attachments/assets/61d0f43c-d0a1-4eb0-88b0-b8b47542ec36)
![Use Autoruns for persistence ](https://github.com/user-attachments/assets/7f4ff45d-0bcb-43f5-bd4d-4a87f259817e)

## Comprehensive Endpoint Monitoring: Filesystem Integrity, User Activity, and Threat Detection


In the Filesystem tab of the LimaCharlie EDR, analysts can efficiently test the hash of software on a system through VirusTotal, helping to quickly assess potential threats. This functionality is crucial in identifying malicious files based on their hashes, aiding in the detection of known and unknown threats. Additionally, the Integrity Monitoring feature is vital for ensuring the security of files by flagging any unauthorized modifications. Integrity monitoring aligns with one of the most critical components of the CIA triad integrity by detecting changes to files that may indicate malicious activity or unauthorized access. Moreover, the Users tab allows analysts to monitor user accounts on the system, including Administrator, Cyber, Default, and Guest accounts. This capability is essential for detecting any unauthorized creation of user accounts, which could be indicative of a cyber attack. Finally, the Timeline section provides a comprehensive view of the system's events, offering valuable insights into ongoing activities within the environment. By tracking these events, analysts can identify potential threats and Indicators of Compromise (IOCs), ensuring a proactive approach to monitoring and defending against cybersecurity risks.
![Screenshot 2024-12-02 223004](https://github.com/user-attachments/assets/830ef4fb-5293-46a3-bbe5-2271606d4d1b)
![Any changes to any files on the computer ](https://github.com/user-attachments/assets/1c23d551-67b4-4e44-aea7-37f4fc6fcb6d)
![Screenshot 2024-12-02 223237](https://github.com/user-attachments/assets/071dc8e9-f50d-4610-8b5d-619c4d4c4834)
![Screenshot 2024-12-02 223255](https://github.com/user-attachments/assets/aaae7abb-d96a-4042-b19c-1ecac2763764)

## Custom Detection and Response Rule Implementation and Testing in LimaCharlie EDR


In this section, I demonstrate the process of creating a custom Detection and Response (D&R) rule within LimaCharlie EDR. I walk through the configuration and programming involved in setting up both the detection and response components, highlighting the flexibility and effectiveness of LimaCharlie in automating threat identification and response. After establishing the rule, I test its functionality by checking if it successfully detects and responds to the hash of malware present on the system. To further validate the system’s capabilities, I clear the detection section and generate new attacks on the virtual machine. This allows me to showcase how LimaCharlie effectively identifies and responds to various malware threats and malicious commands in real-time. By continuously monitoring and reacting to these attacks, LimaCharlie ensures robust protection, proving its reliability in detecting and mitigating security risks within the environment.
![Creating a New rule ](https://github.com/user-attachments/assets/f6043bcb-9fd5-44b5-9bf8-ff922b95320d)
![Creating our Detect and Respond ](https://github.com/user-attachments/assets/67df2d7b-f227-414a-81df-4b8874362724)
![Testing to see if the rule will work compare to the event](https://github.com/user-attachments/assets/f4ab443d-9655-4241-ba56-e5b70bad4a58)
![The detection worked ](https://github.com/user-attachments/assets/233f9924-20cf-4f60-8f90-8b5881642a6a)

