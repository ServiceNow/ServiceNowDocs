---
title: Activate MS Teams chat connector for MS Teams Graph Spoke user
description: If you are an existing user, then follow the procedure in this section to activate Microsoft Teams chat connector for MS Teams Graph Spoke user.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Client Secret value, Establish MS Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate MS Teams chat connector for MS Teams Graph Spoke user

If you are an existing user, then follow the procedure in this section to activate Microsoft Teams chat connector for MS Teams Graph Spoke user.

## Before you begin

Role required: admin

## Procedure

1.  **If you are an existing Microsoft Teams Graph Spoke user, follow the below steps:**

    -   Navigate to your registered application on Azure portal which is used by Microsoft Teams Graph Spoke.
    -   Navigate to **API Permissions** section to configure the required API permissions.
    -   Click **Add a permission**.
    -   Select **Microsoft Graph**.
    -   To use the Microsoft Teams Connector application, you need to add two more delegated permissions to your application from the Azure portal: "ChannelMember.ReadWrite.All" and "TeamMember.ReadWrite.All".
    -   After adding the above required permissions, click on **Grant admin consent**.
    **Configure MS Teams on ServiceNow AI Platform Instance for an existing user:**

    -   Navigate to **Connection &amp; Credential Aliases**.
    -   Select **Microsoft Teams Spoke** record.
    -   Select the Credential record associated with Microsoft Teams Spoke.
    -   Click **Get OAuth Token**. A confirmation message displays that the OAuth Refresh token is available.
    As an existing user, you have now completed integrating Microsoft Teams chat connector application with Microsoft Teams Graph API.


**Parent Topic:**[Using Client Secret value](../../security-incident-response/task/using-client-secret-value.md)

