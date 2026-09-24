---
title: View and update Security Incident Response system properties
description: View and update the Security Incident Response system properties from the Security Incident Response Workspace administration panel to access and update the required properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/view-update-sirw-system-properties.html
release: brazil
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [system properties, view system properties, update system properties, enable workspace v2, switch workspace, workspace 2.0]
breadcrumb: [Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View and update Security Incident Response system properties

View and update the Security Incident Response system properties from the Security Incident Response Workspace administration panel to access and update the required properties.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Expand **System Properties**.

3.  Locate **Enable Workspace V2**.

4.  Set **Enable Workspace V2** to **true** and select **Save**.

5.  Reload the page to load SIR Workspace 2.0.


## Result

SIR Workspace 2.0 loads for your instance. **Enable Workspace V2** is an instance-wide property, not a per-user setting. Set it back to **false**, save, and reload to switch back to the current classic workspace.

-   **[Configure default landing tab for security analysts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/configure-default-landing-tab.md)**  
Configure the default landing tab \(Overview or Details\) for security analysts when they select a security incident so they directly land on the page where they need to work on.
-   **[Configure auto refresh interval for security incident lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/configure-auto-refresh-for-security-incident-lists.md)**  
Configure the refresh interval for security incident lists for automatic update of the security incident list ensuring an updated list for the security analysts.
-   **[Configure default view for contextual menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/configure-default-view-for-contextual-menu.md)**  
Configure whether the contextual menu panel for a security incident is expanded or collapsed by default.
-   **[Configure the preview modal for attachment upload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/configure-attachment-upload-preview-modal.md)**  
Configure whether the preview modal appears when security analysts attach files to a security incident record.

**Parent Topic:**[Configuring SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/configuring-security-incident-response-workspace.md)

**Related topics**  


[Configuring ServiceNow Otto for Security Incident Response \(SIR\)]()

[Set up view of SIR Records]()

[Configure SI design time investigation]()

[SIR Workspace Related Records]()

[Define the new Risk Score Calculator Rules]()

[Configure Shift Handover]()

[Security Incident Response conference call integration]()

[Configure report templates in Security Incident Response]()

[On-Call scheduling in Security Incident Response]()

[Category management in Security Incident Response]()

[Create quick filters for Security Incidents and Response Tasks lists]()

[Timeline in Security Incident Response Workspace]()

