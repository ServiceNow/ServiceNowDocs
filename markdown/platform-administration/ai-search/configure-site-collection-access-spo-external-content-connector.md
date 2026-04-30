---
title: Configure site and site collection access for the Microsoft SharePoint Online external content connector
description: Allow the Microsoft SharePoint Online connector to crawl your sites and site collections by granting site-specific SharePoint API FullControl permissions to the OAuth 2.0 app registered in Microsoft Entra for the connector.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-01-28"
reading_time_minutes: 8
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure site and site collection access for the Microsoft SharePoint Online external content connector

Allow the Microsoft SharePoint Online connector to crawl your sites and site collections by granting site-specific SharePoint API FullControl permissions to the OAuth 2.0 app registered in Microsoft Entra for the connector.

## Before you begin

You must have PowerShell 7.0 or a later compatible version installed.

You need appropriate privileges or permissions to alter permissions for the target app, which is the Microsoft Entra OAuth 2.0 app that allows the Microsoft SharePoint Online external content connector to authenticate and access your source system content. These privileges and permissions depend on which authentication model you want to use when configuring site access for the target app:

-   To use interactive browser-based login, your Microsoft Entra account needs administration privileges.
-   To use service principal authentication, you need a service principal for a Microsoft Entra app that has the Sites.FullControl.All Microsoft Graph API application permission granted by a Microsoft Entra admin. This service principal app is distinct from the target app. You also need one of the following items:

    -   For certificate-based service principal authentication, you need the certificate and private key for your service principal app in PFX format.

        **Note:**

        If you only have your service principal app's certificate and private key in a Java KeyStore \(JKS\) file, you can convert that file to PFX format using this Java keytool command:

        ```
        keytool -importkeystore -srckeystore <your-keystore>.jks -destkeystore certificate.pfx -deststoretype PKCS12 
        -srcalias <your-alias> -deststorepass <your-pfx-password> -destkeypass <your-pfx-password>
        ```

        In this command, replace `<your-keystore>` and `<your-alias>` with the name and alias of the existing JKS file. Replace `your-pfx-password` with the password you want to specify for the PFX output file.

        For details on the Java keytool utility, see [https://docs.oracle.com/en/java/javase/21/docs/specs/man/keytool.html](https://docs.oracle.com/en/java/javase/21/docs/specs/man/keytool.html).

    -   For client secret-based service principal authentication, you need the client secret for your service principal app. If you don't have the client secret, ask your Microsoft Entra administrator for it.

Role required: none

## About this task

This task is only required if you specify the Sites.Selected SharePoint API permission instead of the Sites.FullControl.All permission when configuring the registered Microsoft Entra OAuth 2.0 app for the Microsoft SharePoint Online connector.

**Note:** For details on how these permissions are specified in the OAuth 2.0 app configuration process, see step [3.f](cfg-azure-spo-ext-cont-connector.md#add-sharepoint-api-permissions-substep) in [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md).

By default, source system administrators grant the Sites.FullControl.All SharePoint API permission to the registered Microsoft Entra OAuth 2.0 app for the Microsoft SharePoint Online connector. This permission allows the connector to read content, metadata, and security information for all types of content in all source system sites and site collections.

If your organization's security practices don't allow granting of Sites.FullControl.All permission, you can instead grant the Sites.Selected SharePoint API permission to the OAuth 2.0 application. With this permission granted, the Microsoft SharePoint Online connector can only read content, metadata, and security information for sites and site collections that the OAuth 2.0 app has FullControl permission for.

A source system administrator must grant FullControl permission for each site or site collection that you want the Microsoft SharePoint Online connector to be able to crawl. If you want to prevent the connector from crawling a site or site collection, you can revoke a previously granted FullControl permission for that site or site collection.

## Procedure

1.  Import the SelectedSiteAppPermissionManager PowerShell module on your local system.

    1.  Download the SelectedSiteAppPermissionManager PowerShell module archive from the [KB2741707](https://support.servicenow.com/kb_view.do?sysparm_article=KB2741707) article in the Now Support Knowledge Base.

    2.  Extract the downloaded archive's contents to a directory.

    3.  Start a PowerShell session and navigate to the directory where you extracted the archive's contents.

    4.  Verify that you have the latest version of the Microsoft Graph PowerShell SDK installed by running these PowerShell commands:

        ```powershell
        Install-Module -Name Microsoft.Graph -Scope CurrentUser
        ```

        ```powershell
        Update-Module -Name Microsoft.Graph -Force -Scope CurrentUser
        ```

    5.  View your PowerShell module paths by running this PowerShell command:

        ```powershell
        $env:PSModulePath -split [System.IO.Path]::PathSeparator
        ```

    6.  Copy the SelectedSiteAppPermissionManager module folder from the downloaded archive into one of your PowerShell module paths by running this PowerShell command, replacing `<PowerShell-module-path>` with one of the paths reported in step [1.e](configure-site-collection-access-spo-external-content-connector.md#view-powershell-module-paths).

        ```powershell
        Copy-Item -Path "SelectedSiteAppPermissionManager" -Destination "<PowerShell-module-path>" -Recurse
        ```

        As an example, to copy the module folder into your personal modules folder, you might run this command:

        ```powershell
        Copy-Item -Path "SelectedSiteAppPermissionManager" -Destination "$HOME\Documents\PowerShell\Modules" -Recurse
        ```

    7.  Import the SelectedSiteAppPermissionManager module by running this PowerShell command:

        ```powershell
        Import-Module SelectedSiteAppPermissionManager
        ```

    8.  Verify that the SelectedSiteAppPermissionManager module is correctly imported by running this PowerShell command:

        ```powershell
        Get-Module SelectedSiteAppPermissionManager
        ```

        The command should display information about the SelectedSiteAppPermissionManager module, including its version and supported commands.

2.  Copy one of the JSON-format example configuration files found in the `SelectedSiteAppPermissionManager\Config` directory to a new `my-config.json` file, depending on which authentication method you want to use when configuring site access:

    -   To use interactive authentication in the browser, copy `app-config-interactive.example.json` to `my-config.json`.
    -   To use service principal authentication with a client secret, copy `app-config.client-secret.example.json` to `my-config.json`.
    -   To use service principal authentication with a PFX-format certificate, copy `app-config.certificate.example.json` to `my-config.json`.
3.  In a text editor, modify the JSON object literal key-value pairs in your `my-config.json` file to match your Microsoft Entra app configuration.

<table id="table_e1w_yrk_tgc"><thead><tr><th>

JSON object literal key

</th><th>

Value

</th></tr></thead><tbody><tr><td>

ServicePrincipal.Authentication.Certificate.Password

</td><td>

Password for the PFX-format certificate used for service principal authentication. You only need this key-value pair if you're using service principal authentication with a certificate that has a password. If your certificate has no password, omit this key-value pair.

 Type: String

</td></tr><tr><td>

ServicePrincipal.Authentication.Certificate.Path

</td><td>

Relative path to a PFX-format certificate file that contains the certificate and private key for your service principal app in Microsoft Entra. You only need this key-value pair if you're using service principal authentication with a certificate.

 Type: String

</td></tr><tr><td>

ServicePrincipal.Authentication.Secret

</td><td>

Client secret for your service principal app in Microsoft Entra. You only need this key-value pair if you're using service principal authentication with a client secret.

 Type: String

</td></tr><tr><td>

ServicePrincipal.Authentication.Type

</td><td>

Type of authentication to use for your service principal. You only need this key-value pair if you're using service principal authentication with a certificate or a client secret.

 Type: Choice

 Supported values:

-   **Certificate**: Authenticate using a PFX-format certificate.
-   **Secret**: Authenticate using a client secret.


</td></tr><tr><td>

ServicePrincipal.ClientId

</td><td>

Application \(client\) ID for your service principal app in Microsoft Entra. You only need this key-value pair if you're using service principal authentication with a certificate or a client secret.

 Type: String

</td></tr><tr><td>

ServicePrincipal.TenantId

</td><td>

Directory \(tenant\) ID for your service principal app in Microsoft Entra. You only need this key-value pair if you're using service principal authentication with a certificate or a client secret.

 Type: String

</td></tr><tr><td>

TargetApp.DisplayName

</td><td>

Display name for the OAuth 2.0 app that's registered in Microsoft Entra for the Microsoft SharePoint Online connector. For details on this app, see [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md).

 Type: String

</td></tr><tr><td>

TargetApp.Id

</td><td>

Application \(client\) ID for the OAuth 2.0 app that's registered in Microsoft Entra for the Microsoft SharePoint Online connector. For details on this app, see [Configure Microsoft SharePoint Online for external content indexing](cfg-azure-spo-ext-cont-connector.md).

 Type: String

</td></tr></tbody>
</table>    Example configuration for interactive authentication:

    ```json
    {
        "TargetApp": {
            "Id": "your-application-id",
            "DisplayName": "Your Application Name"
        }
    }
    ```

    Example configuration for service principal authentication with PFX-format certificate:

    ```json
    {
        "TargetApp": {
            "Id": "your-application-id",
            "DisplayName": "Your Application Name"
        },
        "ServicePrincipal": {
            "ClientId": "your-service-principal-id",
            "TenantId": "your-tenant-id",
            "Authentication": {
                "Type": "Certificate",
                "Certificate": {
                  "Path": "path/to/certificate.pfx",
                  "Password": "pfx-password" // Optional if certificate has no password
                }
            }
        }
    }
    ```

    Example configuration for service principal authentication with client secret:

    ```json
    {
        "TargetApp": {
            "Id": "your-application-id",
            "DisplayName": "Your Application Name"
        },
        "ServicePrincipal": {
            "ClientId": "your-service-principal-id",
            "TenantId": "your-tenant-id",
            "Authentication": {
                "Type": "Secret",
                "Secret": "your-client-secret"
            }
        }
    }
    ```

4.  Create a site list file with all the Microsoft SharePoint Online site and site collection URLs you want to operate on for bulk operations.

    1.  In a text editor, create a new file called `sitelist.txt`.

    2.  Populate the new `sitelist.txt` file with the URLs for all the Microsoft SharePoint Online sites and site collections you want to view or modify permissions for, one per line.

        As an example, if you wanted to view or modify permissions for two sites at once, your file might look like this:

        ```
        https://example.sharepoint.com/sites/site1
        https://example.sharepoint.com/sites/site2
        ```

5.  To view existing app permissions for specified Microsoft SharePoint Online sites and site collections, run this PowerShell command:

    ```powershell
    
    Get-SharePointAppPermission -SiteUrls "https://example.sharepoint.com/sites/site1","https://example.sharepoint.com/sites/site2" -ConfigFile "./my-config.json"
    ```

    If you have a site list file, you can specify it with the `-SiteListFile` argument \(replacing the `-SiteURLs` argument\):

    ```powershell
    
    Get-SharePointAppPermission -SiteListFile "./sitelist.txt" -ConfigFile "./my-config.json"
    ```

    **Important:** If you're using service principal authentication, add the `-UseServicePrincipal` argument to your command line.

6.  To add FullControl permissions to specified Microsoft SharePoint Online sites and site collections, run this PowerShell command:

    ```powershell
    
    Add-SharePointAppPermission -SiteUrls "https://example.sharepoint.com/sites/site1","https://example.sharepoint.com/sites/site2" -ConfigFile "./my-config.json"
    ```

    If you have a site list file, you can specify it with the `-SiteListFile` argument \(replacing the `-SiteURLs` argument\):

    ```powershell
    
    Add-SharePointAppPermission -SiteListFile "./sitelist.txt" -ConfigFile "./my-config.json"
    ```

    **Important:** If you're using service principal authentication, add the `-UseServicePrincipal` argument to your command line.

7.  To remove FullControl permissions from specified Microsoft SharePoint Online sites and site collections, run this PowerShell command:

    ```powershell
    
    Remove-SharePointAppPermission -SiteUrls "https://example.sharepoint.com/sites/site1","https://example.sharepoint.com/sites/site2" -ConfigFile "./my-config.json"
    ```

    If you have a site list file, you can specify it with the `-SiteListFile` argument \(replacing the `-SiteURLs` argument\):

    ```powershell
    
    Remove-SharePointAppPermission -SiteListFile "./sitelist.txt" -ConfigFile "./my-config.json"
    ```

    **Important:** If you're using service principal authentication, add the `-UseServicePrincipal` argument to your command line.


## What to do next

If you remove FullControl permissions from sites or site collections that are still crawled by the Microsoft SharePoint Online external content connector, the connector will log permissions alerts when it tries to crawl content from those sites or site collections. To eliminate these alerts, ask your connector admin to remove or exclude the affected sites and site collections from the set of sites crawled by the connector.

**Parent Topic:**[Microsoft SharePoint Online external content connector](../concept/microsoft-sharepoint-online-external-content-connector.md)

