---
title: Enable security incidents for vulnerabilities
description: Access threat intelligence context for security incidents directly within the Security Incident Response Workspace. TISC context helps you understand related threats and make informed decisions during incident response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/tisc-view-security-context.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-27"
reading_time_minutes: 1
keywords: [TISC context,security incident,vulnerability,threat intelligence]
breadcrumb: [TISC integration within SIR Workspace, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Enable security incidents for vulnerabilities

Access threat intelligence context for security incidents directly within the Security Incident Response Workspace. TISC context helps you understand related threats and make informed decisions during incident response.

## Before you begin

Roles required:

-   sn\_sec\_tisc.analyst
-   sn\_si.analyst

## About this task

Security incidents enable tracking and management of remediation efforts for vulnerabilities in TISC, supporting prioritized response and maintaining auditability. For more information, see [Create Security Incident from a Vulnerability Record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-create-security-incident.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Workspace**.

2.  Select the **Security Incidents** icon on the workspace.

3.  Navigate to **Lists** &gt; **All**.

4.  Open a security incident record.

5.  Navigate to the **TISC Context** section.

    The **Vulnerabilities** entry point provides access to information about threat objects related to the selected vulnerability.

6.  Select **View Related Info** to explore associated vulnerability data.

    This displays a list of related threat objects associated with the vulnerability, including threat actors, attack patterns, campaigns, cases, vulnerability entries, and vulnerability assessments.

7.  Select any object to view the corresponding record in the TISC workspace.


**Parent Topic:**[TISC integration within SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/tisc-sir-workspace.md)

**Related topics**  


[Define Vulnerability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/define-vulnerability.md)

[Create Remediations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-create-remediation-record.md)

[Create Vulnerability Assessment from a Vulnerability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-vul-assess.md)

