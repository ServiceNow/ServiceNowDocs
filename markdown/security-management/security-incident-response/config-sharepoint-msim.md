---
title: Configure Microsoft SharePoint with Major Security Incident Management
description: Establish a connection between Major Security Incident Management and Microsoft SharePoint to enable document collaboration and management of security incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/config-sharepoint-msim.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [sharepoint, integration, document-collaboration, incident-management]
breadcrumb: [Integrate Major Security Incident Management with Microsoft SharePoint, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Microsoft SharePoint with Major Security Incident Management

Establish a connection between Major Security Incident Management and Microsoft SharePoint to enable document collaboration and management of security incidents.

## Before you begin

Role required: admin, sn\_msi.workspace\_admin

**Note:** The Azure App Registration credentials \(Client ID, Tenant ID, Certificate or Client Secret\) are the same values entered in each instance. The SharePoint Site URL differs if separate sites were provisioned per environment.

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Administration**.

2.  Select **Document Collaboration**, and then **Microsoft SharePoint Setup**.

3.  Select **Grant Azure App Access to SharePoint Site** from the context menu.

4.  Grant access to your registered application using one of the following methods: Curl Commands, Azure CLI or PowerShell.

    **Note:**

    -   The Azure administrator must provide the access configuration.
    -   Grant the Sites.FullControl.All permission to the registered application.
    -   Remove the Sites.FullControl.All permission when the access is successfully granted.
    **Note:** This is a two-phase process: **Phase 1 \(Azure portal\)** — temporarily grant Sites.FullControl.All at the API Permissions level on the App Registration to enable the site-level grant commands below. **Phase 2 \(commands\)** — execute one of the three methods to grant *write* access to the registered application at the SharePoint site level via the Microsoft Graph API. Once the ServiceNow connection is confirmed, return to the Azure portal and remove Sites.FullControl.All from API Permissions; the site-level write permission granted by the commands remains in place for ongoing MSIM operations. For the command reference for all three methods, see [Commands to grant Azure application access to the Microsoft SharePoint site](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/grant-azure-app-access-sharepoint-site-commands.md).

5.  Select **Set Up SharePoint Configuration** from the context menu.

6.  Select a configuration type in **Select Configurations Types**, and configure the following.

    -   Certificate \(Applications Permissions\)

        \[Omitted image "sharepoint-setup-msim.png"\] Alt text: SharePoint setup for certificate

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

        \[Omitted image "sharepoint-setup-clientsecret.png"\] Alt text: SharePoint setup for client secret

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


**Parent Topic:**[Integrate Major Security Incident Management with Microsoft SharePoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/integrate-msim-sharepoint.md)

