---
title: Customize SI to MSI flows \(optional\)
description: Copy and customize the SI to MSI promotion flows to control how File Explorer and chat channels are configured when a Security incident is promoted to a Major Security Incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/customize-si-to-msi-flows-for-msim.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-08-03"
reading_time_minutes: 2
breadcrumb: [Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Customize SI to MSI flows \(optional\)

Copy and customize the SI to MSI promotion flows to control how File Explorer and chat channels are configured when a Security incident is promoted to a Major Security Incident.

## Before you begin

Role required: sn\_msi.workspace\_admin

**Note:** You can't edit delivered flows directly. Copy the flow and edit the copy to preserve the original delivered flow.

## About this task

Two Flow Designer flows control component setup when a security incident is promoted to a major security incident:

-   **SI to MSI Promotion \(SharePoint\)** sets up the File Explorer component by calling the **Create Folder Structure** subflow, which builds the folder hierarchy per the [Create Folder Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/file-explorer-folder-templates.md) configuration.
-   **SI to MSI Promotion \(Teams\)** sets up the Chat component by calling the **Chat Team and Channels Creation** subflow, which builds the team and channels per the [Create a chat channel template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/create-chat-channel-template-for-msim.md) configuration.

Both flows are active by default. Use this procedure only if you need to customize how these components are configured during promotion.

## Procedure

1.  In the [ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-platform/now-platform-landing.md), navigate to **Flow Designer**.

2.  Search for the **SI to MSI Promotion \(SharePoint\)** flow.

3.  Open the flow and select **Copy** from the flow actions.

4.  In the Name field, enter a name for the copied flow.

5.  Select **Save**.

6.  Make your customizations to the flow.

    For example, modify the folder structure or add additional actions.

7.  Select **Activate**.

8.  Verify that the flow status shows **Active** and the flow trigger is set to **Major security incident Created or Updated where MSI candidate state is Accepted**.

9.  Repeat steps 2 through 8 for the **SI to MSI Promotion \(Teams\)** flow.


## Result

Confirm your customized flow is in the **Active** state before configuring notification preferences.

**Parent Topic:**[Configuring Major Security Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/configuring-major-security-incident-management.md)

**Related topics**  


[Configure File Explorer Component]()

[Configure Microsoft Teams]()

[Configure Slack chat connector for major security incidents]()

