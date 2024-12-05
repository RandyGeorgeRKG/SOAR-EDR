# SOAR(Tines)-EDR(LimaCharlie) Project 
![image](https://github.com/user-attachments/assets/9db49eff-99fa-4f10-84e4-a0c4d14c9218) ![image](https://github.com/user-attachments/assets/344dc903-8cca-4533-a2aa-f5346888e1d2)






## Introduction
Howdy Thank you for taking the time to explore my SOAR-EDR project, which integrates LimaCharlie and Tines. The goal of this project is to demonstrate the critical role of automation in responding to cybersecurity threats in real time.

SOAR stands for Security Orchestration, Automation, and Response, while EDR refers to Endpoint Detection and Response. SOAR is an automation platform used by SOC analysts and security professionals to streamline the detection, investigation, and response to incidents within their environment.

The key distinction between SOAR and a traditional SIEM (Security Information and Event Management) system, such as Splunk, is that SOAR automates response actions. In a SIEM, analysts typically have to manually take actions, such as quarantining compromised systems or investigating alerts. In contrast, SOAR systems automate many of these tasks, enabling SOC analysts to focus on higher-level activities while improving response time and reducing human error.

Integrating a SOAR system into your security operations enhances overall efficiency, reduces risks, and strengthens the ability to mitigate threats effectively.

## Project Overview

![image](https://github.com/user-attachments/assets/008ed71c-37f2-4582-93e3-c8c9c64cfab4)


In this project, I have developed a workbook that demonstrates the integration of LimaCharlie (our Endpoint Detection and Response, or EDR) with Tines, a security orchestration, automation, and response (SOAR) platform. The objective is to show how LimaCharlie detects malicious software or commands on an endpoint, and how Tines is used to automate the response process.

Upon detection of a threat by LimaCharlie, a notification is triggered to alert relevant stakeholders via Slack and Email. At this point, a user prompt is presented, asking whether the affected machine should be isolated from the network. If the user selects "No," they will receive a message informing them that the machine was not isolated. If "Yes" is selected, the affected machine will be quarantined from the network, effectively containing the threat and reducing potential damage to the environment.
