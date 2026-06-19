---
title: Configure Microsoft Teams connection with Major Security Incident Management
description: Set up Major Security Incident Management with Microsoft Teams connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/configure-teams-msim.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate Major Security Incident Management with Microsoft Teams, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Microsoft Teams connection with Major Security Incident Management

Set up Major Security Incident Management with Microsoft Teams connection.

## Before you begin

Prerequisite: Make sure that you have registered an application in Azure Active Directory with required delegate permissions.

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Administration**.

2.  Select **Chat Collaboration**, and then **Microsoft Teams Setup**.

3.  Select a configuration type in the **Select Configurations Types** field, and configure the following.

    -   Certificate \(Delegated Permissions\)

        \[Omitted image "teams-setup-certificate.png"\] Alt text: Teams setup using certificate

        |Field|Description|
        |-----|-----------|
        |Directory \(tenant\) ID|The unique identifier of your Azure Active Directory instance.|
        |Application \(client\) ID|The unique identifier of your registered application in Azure.|
        |Upload Certificate|The certificate file for the authentication.|
        |Thumbprint|The thumbprint for the certificate.|
        |Keystore password|The keystore password to access the certificate's thumbprint.|

    -   Client Secret \(Delegated Permissions\)

        \[Omitted image "teams-setup-clientsecret.png"\] Alt text: Teams setup using client secret

        |Field|Description|
        |-----|-----------|
        |Directory \(tenant\) ID|The unique identifier of your Azure Active Directory instance.|
        |Application \(client\) ID|The unique identifier of your registered application in Azure.|
        |Client Secret|The secret string of the application used for requesting a token.|

4.  Select **Configure &amp; Get OAuth Token**.

    A login prompt appears to provide your Microsoft account details.

5.  Provide your Microsoft account details and login.

    A successful message appears and the connection is established.

6.  Select **Activate Chat Provider** to enable Microsoft Teams connection.

7.  Select **Show Advanced Details** to view the configuration details.


**Parent Topic:**[Integrate Major Security Incident Management with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/integrate-teams-msim.md)

