---
title: Configure alert remediation actions
description: Run commands to perform alert remediation on remote Linux and Windows CIs.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Alert management rules for resolving alerts, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure alert remediation actions

Run commands to perform alert remediation on remote Linux and Windows CIs.

## Before you begin

Install the following plugins:

-   IntegrationHub Enterprise spokes plugin
-   ServiceNow IntegrationHub Action Step - PowerShell
-   ServiceNow IntegrationHub Action Step - SSH

For Linux: Ensure that the remote Linux host is reachable using the MID Server IP address that runs action scripts.

For Windows:

-   Ensure that Powershell v3.0 - 5.0 are supported and installed on the Windows target server.
-   Enable Powershell remoting on the remote Windows target server.
-   Ensure that the remote Windows target server is reachable using the FQDN from the MID Server that runs action scripts.

Add credentials to the credential aliases that come with the base system:

-   linuxAdmin
-   windowsAdmin

Role required: evt\_mgmt\_admin or flow\_designer

## Procedure

1.  Access remediation actions in one of the following ways:

    -   Quick actions in an alert, as described in [Apply a quick response in an alert](apply-quick-response-in-alert.md).
    -   The Playbook tab in Service Operations Workspace, as described in [Run actions to resolve alert issues](../../service-operations-workspace-itom/task/run-alert-remediation.md) .
2.  Configure additional input in the alert's **Additional Information** field, using this format:

    `{"remediation_action_resource":"<mandatory input>"}`

    The mandatory input per action is described in the following table.

    |Action name|Mandatory input in Additional information field|
    |-----------|-----------------------------------------------|
    |Stop Windows Process|Process ID|
    |Restart Linux Service|Service Name|
    |Kill Linux Process|Process ID|
    |Get Windows Processes|N/A|
    |Stop Windows Service|Service Display Name|
    |Restart Windows Service|Service Display Name|
    |Get Windows Services|N/A|
    |Stop Linux Service|Service Name|
    |Start Windows Service|Service Display Name|
    |Suspend Windows Service|Service Display Name|
    |Get Linux Services|N/A|
    |Run Linux Top for Memory|N/A|
    |Show Disk Space Used|N/A|
    |Run Linux Top|N/A|
    |Start Linux Service|Service Name|
    |Show Disk Space Used|N/A|


## Result

After executing an alert action, the results are noted in the **Work Notes** field of the alert.

**Parent Topic:**[Alert management rules for resolving alerts](../concept/alert-management-rule.md)

**Related topics**  


[Troubleshooting WMI/Powershell issues on the remote machine](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0549830)

[WMI, PowerShell, and Windows Firewalls](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0549828)

[MID Server: troubleshooting WMI/Powershell issues - Credentials](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0549834)

[How to Enable/Test PowerShell Remoting on Windows Host](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0813330)

