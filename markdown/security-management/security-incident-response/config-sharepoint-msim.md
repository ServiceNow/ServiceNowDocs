---
title: Configure Microsoft SharePoint with Major Security Incident Management
description: Set up Major Security Incident Management with Microsoft SharePoint connection.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate Major Security Incident Management with Microsoft SharePoint, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Microsoft SharePoint with Major Security Incident Management

Set up Major Security Incident Management with Microsoft SharePoint connection.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Administration**.

2.  Select **Document Collaboration**, and then **Microsoft SharePoint Setup**.

3.  Select **Grant Azure App Access to SharePoint Site** from the context menu.

4.  Grant access to your registered application using one of the following methods: Curl Commands, Azure CLI or PowerShell.

    **Note:**

    -   The Azure administrator must provide the access configuration.
    -   Grant the Sites.FullControl.All permission to the registered application.
    -   Remove the Sites.FullControl.All permission when the access is successfully granted.
5.  Select **Set Up SharePoint Configuration** from the context menu.

6.  Select a configuration type in **Select Configurations Types**, and configure the following.

    -   Certificate \(Applications Permissions\)

        ![SharePoint setup for certificate](../image/sharepoint-setup-msim.png)

        |Field|Description|
        |-----|-----------|
        |SharePoint Site URL|The Microsoft SharePoint Site URL.|
        |SharePoint Document Library Name|Name of the Microsoft SharePoint document library.|
        |Directory \(tenant\) ID|The unique identifier of your Azure Active Directory instance.|
        |Application \(client\) ID|The unique identifier of your registered application in Azure.|
        |Upload Certificate|The certificate file for the authentication.|
        |Thumbprint|The thumbprint for the certificate.|
        |Keystore password|The keystore password to access the certificate's thumbprint.|

    -   Client Secret \(Applications Permissions\)

        ![SharePoint setup for client secret](../image/sharepoint-setup-clientsecret.png)

        |Field|Description|
        |-----|-----------|
        |SharePoint Site URL|The Microsoft SharePoint Site URL.|
        |SharePoint Document Library Name|Name of the Microsoft SharePoint document library.|
        |Directory \(tenant\) ID|The unique identifier of your Azure Active Directory instance.|
        |Application \(client\) ID|The unique identifier of your registered application in Azure.|
        |Client Secret|The secret string of the application used for requesting a token.|

7.  Select **Configure &amp; Get OAuth Token**.

    A login prompt appears to provide your Microsoft account details.

8.  Provide your Microsoft account details and login.

    A successful message appears and the connection is established.


**Parent Topic:**[Integrate Major Security Incident Management with Microsoft SharePoint](../concept/integrate-msim-sharepoint.md)

