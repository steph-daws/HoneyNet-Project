
# Azure Honeynet: Simulating Real-World Cyber Attacks
![Cloud Honeynet / SOC](https://github.com/user-attachments/assets/b416df9d-ac56-4a07-99f4-d4e256594236)


## Introduction

 I am thrilled to present my latest project, which focuses on building a honeynet in Azure to simulate real-world cyber attacks. 
This project showcases my skills in Azure security, incident response, and environment hardening

## Objective
The main objective of this project was to [set up virtual machines that were intentionally vulnerable](https://github.com/steph-daws/Azure_VM_Prep) in the Azure infrastructure to attract and analyze cyber attacks. This helped me to better understand the tactics and techniques used by attackers, while also showcasing my ability to respond quickly and effectively to any identified issues.

## Technologies, Regulations, and Azure Components Employed:

- Azure Virtual Network (VNet)
- Azure Network Security Group (NSG)
- Virtual Machines (2x Windows, 1x Linux)
- Log Analytics Workspace with Kusto Query Language (KQL) Queries
- Azure Key Vault for Secure Secrets Management
- Azure Storage Account for Data Storage
- Microsoft Sentinel for Security Information and Event Management (SIEM)
- Microsoft Defender for Cloud to Protect Cloud Resources
- Windows Remote Desktop for Remote Access
- Command Line Interface (CLI) for System Management
- PowerShell for Automation and Configuration Management
- [NIST SP 800-53 Revision 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) for Security Controls
- [NIST SP 800-61 Revision 2](https://www.nist.gov/privacy-framework/nist-sp-800-61) for Incident Handling Guidance

## Methodology

- <b>*Creating the honeynet*</b>: I began by [deploying multiple vulnerable virtual machines](https://github.com/steph-daws/Azure-VM-Prep/blob/main/README.md) in Azure, simulating an insecure environment.

- <b>*Monitoring and analysis*</b>: Azure was configured to ingest log sources from various resources into a log analytics workspace. Microsoft Sentinel was then used to build attack maps, trigger alerts, and create incidents based on the collected data.

- <b>*Security metrics measurement*</b>: I observed the environment for 24 hours, recording key security metrics while it was insecure. This provided a baseline to compare against after implementing remediation measures.

- <b>*Incident response and remediation*</b>: After addressing the incidents and identifying vulnerabilities, I began the process of hardening the environment by applying security best practices and Azure-specific recommendations.

- <b>*Post-remediation analysis*</b>: I re-observed the environment for another 24 hours to measure security metrics again, comparing the results with the initial baseline.

<b>Before Hardening Measures and Security Controls:</b>

- In the "BEFORE" stage of the project, all resources were initially deployed with public exposure to the internet. This setup was intentionally insecure to attract potential cyber attackers and observe their tactics. The Virtual Machines had both their Network Security Groups (NSGs) and built-in firewalls wide open, allowing unrestricted access from any source. Additionally, all other resources, such as storage accounts and databases, were deployed with public endpoints visible to the internet, without utilizing any Private Endpoints for added security.

  


## Architecture Prior to Implementing Hardening Measures and Security Controls
![Architecture Diagram](https://i.imgur.com/1tLjWY9.png)

