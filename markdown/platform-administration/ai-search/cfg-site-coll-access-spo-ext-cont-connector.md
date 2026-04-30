---
title: Configure site collection access for the Microsoft SharePoint Online external content connector
description: Allow the Microsoft SharePoint Online connector to crawl your site collections by granting SharePoint API FullControl permissions to your registered Microsoft Entra OAuth 2.0 app for the connector.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-06-22"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure Microsoft SharePoint Online for external content indexing, Configuring source systems for external content indexing, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure site collection access for the Microsoft SharePoint Online external content connector

Allow the Microsoft SharePoint Online connector to crawl your site collections by granting SharePoint API FullControl permissions to your registered Microsoft Entra OAuth 2.0 app for the connector.

## Before you begin

You must have permissions to open an elevated PowerShell session on a Windows system by running PowerShell as an administrator.

Your Windows system must have the PnP PowerShell module installed. For details on this module, see the [PnP PowerShell overview article](https://learn.microsoft.com/en-us/powershell/sharepoint/sharepoint-pnp/sharepoint-pnp-cmdlets) on the Microsoft Learn site and the [PnP PowerShell](https://pnp.github.io/powershell/) site.

**Note:** You can check whether the PnP PowerShell module is installed by running `Get-Command -Module PnP.PowerShell` in a PowerShell session. This cmdlet returns a list of installed PnP PowerShell aliases and cmdlets if the module is installed. If the cmdlet returns no results, the module isn't installed.

You must have an Entra ID application registered to use with PnP PowerShell. For details on registering this application, see the [Register an Entra ID Application to use with PnP PowerShell article](https://pnp.github.io/powershell/articles/registerapplication.html) on the PnP PowerShell site.

**Note:** The Entra ID application allows you to connect to your Microsoft SharePoint Online site collections using PnP PowerShell. It's distinct from the OAuth 2.0 app configured in Microsoft Entra for the Microsoft SharePoint Online external content connector.

Role required: none

## About this task

This task is only required if you specify the Sites.Selected SharePoint API permission instead of the Sites.FullControl.All permission when configuring the registered Microsoft Entra OAuth 2.0 app for the Microsoft SharePoint Online connector.

**Note:** For details on the OAuth 2.0 app configuration process, see [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md).

By default, source system administrators grant the Sites.FullControl.All SharePoint API permission to the registered Microsoft Entra OAuth 2.0 app for the Microsoft SharePoint Online connector. This permission allows the connector to read content, metadata, and security information for all types of content in all source system site collections.

If your organization's security practices don't allow granting of Sites.FullControl.All permission, you can instead grant the Sites.Selected SharePoint API permission to the OAuth 2.0 application. With this permission granted, the Microsoft SharePoint Online connector can only read content, metadata, and security information for site collections that the OAuth 2.0 app has FullControl permission for.

A source system administrator must grant FullControl permission for each site collection that you want the Microsoft SharePoint Online connector to be able to crawl. If you want to prevent the connector from crawling a site collection, you can revoke a previously granted FullControl permission for that site collection.

## Procedure

1.  On your Windows system, start an elevated PowerShell session by running PowerShell as an administrator.

2.  Establish a PnP PowerShell connection to the site collection.

    1.  Run this cmdlet in your elevated PowerShell session, replacing `<siteURL>` with the URL for the site collection whose access permissions you want to change and `<clientId>` with the app ID for your Entra ID application registered for use with the PnP PowerShell module:

        ```powershell
        Connect-PnPOnline -Url <siteUrl> -Interactive -ClientId <clientId>
        ```

    2.  When prompted, enter your Microsoft account credentials.

3.  Grant Write permission to the Microsoft Entra OAuth 2.0 app for the Microsoft SharePoint Online external content connector:

    1.  Run this cmdlet in your elevated PowerShell session, replacing `<appId>` and `<name>` with the application ID and display name of your registered Microsoft Entra OAuth 2.0 app for the Microsoft SharePoint Online external content connector:

        ```powershell
        Grant-PnPAzureADAppSitePermission -AppId appId -DisplayName <name> -Permissions Write
        ```

    2.  Record the permission ID from the cmdlet's response.

        **Important:** You need this permission ID to grant FullControl permissions for your site collections using PnP.

4.  Modify or verify permissions for the site collection in your Microsoft Entra OAuth 2.0 app for the Microsoft SharePoint Online external content connector:

    -   To grant the app FullControl permission for the site collection and allow crawling by the Microsoft SharePoint Online external content connector, run this cmdlet in your elevated PowerShell session, replacing `<permissionId>` with the permission ID you recorded in step [3.b](cfg-site-coll-access-spo-ext-cont-connector.md#record-permission-id-substep) and `<siteURL>` with the site collection's URL:

        ```powershell
        Set-PnPAzureADAppSitePermission -PermissionId <permissionId> -Permissions FullControl -Site <siteUrl>
        ```

    -   To revoke the app's FullControl permission for the site collection and prevent crawling by the Microsoft SharePoint Online external content connector, run this cmdlet in your elevated PowerShell session, replacing `<permissionId>` with the permission ID you recorded in step [3.b](cfg-site-coll-access-spo-ext-cont-connector.md#record-permission-id-substep) and `<siteURL>` with the site collection's URL:

        ```powershell
        Revoke-PnPAzureADAppSitePermission -PermissionId <permissionId> -Site <siteUrl>
        ```

    -   To view the app's existing permissions for the site collection, run this cmdlet in your elevated PowerShell session, replacing `<permissionId>` with the permission ID you recorded in step [3.b](cfg-site-coll-access-spo-ext-cont-connector.md#record-permission-id-substep) and `<siteURL>` with the site collection's URL:

        ```
        Get-PnPAzureADAppSitePermission -PermissionId <permissionId> -Site <siteUrl>
        ```

5.  Disconnect from the site collection by running this cmdlet in your elevated PowerShell session:

    ```powershell
    Disconnect-PnPOnline
    ```

6.  Repeat steps [2](cfg-site-coll-access-spo-ext-cont-connector.md#first-per-site-step) through [5](cfg-site-coll-access-spo-ext-cont-connector.md#last-per-site-step) for each additional site collection you want to modify permissions for.


## What to do next

Provide the list of site collections that have FullControl permissions granted for the Microsoft SharePoint Online external content connector to your ServiceNow AI Platform admin. They need this list to configure a Microsoft SharePoint Online external content connector to crawl only the selected sites.

For details on creating and configuring a Microsoft SharePoint Online external content connector, see [Create a Microsoft SharePoint Online external content connector](create-ext-cont-connector-mspo.md).

**Parent Topic:**[Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md)

