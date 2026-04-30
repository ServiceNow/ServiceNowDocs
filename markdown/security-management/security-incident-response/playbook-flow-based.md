---
title: Flow-based Playbooks
description: Using the Flow Designer, security administrators and flow design authors can more easily transition from manual or undocumented playbooks to automated and repeatable playbooks. The drag-and-drop feature provides flexibility in moving objects, condition checks, parallel branching, decision tables, and more.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Flow-based Playbooks

Using the Flow Designer, security administrators and flow design authors can more easily transition from manual or undocumented playbooks to automated and repeatable playbooks. The drag-and-drop feature provides flexibility in moving objects, condition checks, parallel branching, decision tables, and more.

Security Incident Response provides the following playbooks with the base system.

In addition to the listed playbooks, there are also subflows in Security Operations Spoke that can be called from the flows playbook. Ransomware is one of that subflows.

Activate these flows before you use them. For more information, see [Activate a Security Incident Response flow](../task/getting-started-phishing-playbook.md).

-   **[Playbook for Automated Phishing](flow-designer-and-phishing-response.md)**  
The Automated Phishing playbook helps you resolve certain types of security threats in a step-by-step manner. With the flow designer templates, you can automate the steps in the phishing response playbook and resolve incidents quickly and efficiently.
-   **[Playbook for Automated Malware](cj-sir-about-malware-flow.md)**  
The Automated Malware playbook provides a sequence of automated steps that helps you resolve malware alerts quickly and efficiently.
-   **[Playbook for Failed Login Manual](cj-sir-flow-library2.md)**  
When a user makes certain unsuccessful login attempts \(according to the SIM configuration\), a security incident is created.
-   **[Playbook for Child Security Incident Automation](cj-sir-flow-library4.md)**  
Duplicate security incidents are categorized as child security incidents and are rolled up to the parent security incidents.
-   **[Playbook for Office 365 - Malicious File Detected](playbook-office-malicious-file-detected-.md)**  
This playbook provides systematic remediation steps for investigating malicious files detected in Office 365.
-   **[Playbook for Repeat Detection](playbook-repeat-detection.md)**  
This playbook helps you determine if the incident response has been provided on an exact or similar phishing report in the past and automatically works on the new report similarly.
-   **[Playbook for Spoofed Emails \(using the same Display name\)](playbook-spoofed-emails-display-name.md)**  
This playbook provides systematic remediation steps to investigate Spoofed Emails, which get triggered when spoofed names for emails are sent to the organization's employees.
-   **[Playbook for Endpoint Detection](playbook-endpoint-detection.md)**  
This playbook provides systematic remediation steps to investigate malware alerts triggered on a host or endpoint \(For example, a malicious file detection\).
-   **[Playbook for Possible Password Spray](playbook-possible-password-spray.md)**  
This playbook provides systematic remediation steps to investigate password spray alerts triggered by multiple failed logins \(too many authentication failures from more than one IP address for the same user\).
-   **[Playbook for T1003 - Detect Credential Dumping Tools](playbook-detect-credential-dumping-tools.md)**  
This playbook provides systematic remediation steps to investigate an incident involving credential dumping activities.
-   **[Playbook for Email Domain Spoofing Detection](playbook-email-spoof-detection.md)**  
This playbook helps with the early stage triage of user-reported phishing submissions by alerting the analyst to the possibility of a look-alike domain in the Phisher's email address.
-   **[Playbook for Typo Squatted Domain](playbook-typo-squatted-domain.md)**  
This playbook provides systematic procedures for investigating misspelled domains and collaborating with the organization’s legal department for take-downs. Typo Squatted domains are intentionally misspelled domain names that closely resemble legitimate ones. Attackers take advantage of spelling errors to lead them to an ill-intended website for financial exploitation or other malicious activities.
-   **[Playbook for Credential Sniffing](playbook-credential-sniffing.md)**  
This playbook provides system remediation steps to investigate an incident involving credential sniffing activities performed through the **sys\_installation\_exit** table in a ServiceNow instance.
-   **[Playbook for T1070 - Windows Events Logs Cleared](playbook-windows-events-log.md)**  
This playbook provides remediation steps to investigate incidents that track event types where the user removes security logs. Whenever the Security log is cleared, the events 517 and 1102 are logged regardless of the Audit System Event policy status.
-   **[Playbook for OSquery of External Address in /etc/hosts file](playbook-osquery-external-address.md)**  
This playbook provides systematic remediation steps to investigate incidents that indicate that an internal hostname or domain has been assigned to an external IP address on the local DNS\(/etc/hosts\) of a Linux server.
-   **[Playbook for User Deleting Bash History - Cloud](playbook-deleting-bash-history.md)**  
This playbook provides systematic remediation steps to investigate incidents that indicate if someone was trying to remove the bash history \(`.bash_history`\) file from a Linux server.
-   **[Playbook for Successful VPN Attempts from the Service Accounts - Corp/Cloud](playbook-successful-vpn-attempts.md)**  
This playbook provides systematic remediation steps to investigate incidents that track successful login attempts from service accounts through VPN. Service accounts aren’t supposed to have login events from a VPN, and such events could be indicators of either brute force or possible exposure of the account's credentials.
-   **[Playbook for Attempted Access to Deactivated Accounts](playbook-attempted-access-deactivated-accounts.md)**  
This playbook triggers when an employee whose account is terminated, disabled, or separated attempts to log in with their credentials. User’s identity state in Sail point generally gets updated to disabled on their termination date.
-   **[Playbook for T1003 - Defense Evasion - Mimikatz DCShadow](playbook-defense-evasion-mimikatz-dcshadow.md)**  
This playbook provides systematic remediation steps to investigate incidents suspected to be caused by Mimikatz DCShadow. DCShadow is a feature in Mimikatz that simulates the behavior of a Domain Controller \(a server controlling Active Directory\) to inject its own data, bypassing most of the standard security controls \(including SIEMs\).
-   **[Playbook for T1003 - Credential Dumping - Mimikatz DCSync](playbook-credential-dumping-mimikatz-dcsync.md)**  
This playbook provides systematic remediation steps to investigate incidents suspected to be caused by Mimikatz DCSync. This playbook triggers when one of the Mimikatz functions `(lsadump::dcsync`\) is used. The function is typically used on attacked Domain Controllers \(DC\).
-   **[Playbook for Okta User Login Failures from Multiple IPs](playbook-okta-user-login-failures-ips.md)**  
This playbook provides systematic remediation steps to investigate incidents for user login failures on Okta.
-   **[Playbook for ModSec Brute force by IP Burst](playbook-modsec-bruteforce-ip.md)**  
This playbook provides systematic remediation steps to investigate incidents of brute force attempts on the login pages from multiple IPs detected by ModSec. The event conditions could be set at the ModSec policy itself and will raise an alert at Splunk when the event is created at ModSec.

**Parent Topic:**[Security Incident Response playbooks](cj-sir-about-flows.md)

**Related topics**  


[Process-based Playbooks](playbooks-process-based.md)

