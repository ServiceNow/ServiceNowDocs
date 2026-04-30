---
title: Exporting your table records to Google Sheets
description: Integrate your ServiceNow instance and Google Cloud Console so that you can export table records directly to the cloud-based Google Sheets in Google Drive. With this integration, you can view, share, and work on data outside the platform by using spreadsheets.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exporting data, Tables and data, Configure core features, Administer]
---

# Exporting your table records to Google Sheets

Integrate your ServiceNow instance and Google Cloud Console so that you can export table records directly to the cloud-based Google Sheets in Google Drive. With this integration, you can view, share, and work on data outside the platform by using spreadsheets.

In the Google Cloud Console, enable the Google Sheets API to authenticate the requests from your ServiceNow instance through an OAuth application.

**Note:** OAuth enables you to grant access to your data and files to third parties without sharing usernames or passwords.

Before you can do the integration, you must set up the OAuth application so that you can authenticate the requests from your ServiceNow instance. For more information on how to do the setup, see [Set up the OAuth application on the Google Sheets API](../task/set-up-oauth-app-gsheets-api.md) at [https://console.developers.google.com/](https://console.developers.google.com/).

Next, you register the Google Drive application in your ServiceNow instance to enable OAuth authorization for exporting your table records directly to Google Sheets.

Then, you configure the connection and credential aliases to authenticate the integration between your ServiceNow instance and Google Drive.

**Note:** Aliases help keep credentials separate from the integration logic, making it easier and safer to manage sensitive information.

The connection and credentials record contains the information that the Google Sheets API needs to authenticate the requests from your ServiceNow instance. It includes the user credentials and connection type, which are required for your instance to communicate with Google Cloud.

-   **[Set up the OAuth application on the Google Sheets API](../task/set-up-oauth-app-gsheets-api.md)**  
Set up the OAuth application on the Google Sheets API so that you can authenticate requests from your ServiceNow instance to access Google Sheets.
-   **[Create an application registry for Google Sheets on a ServiceNow instance](../task/configure-app-registry-gsheets.md)**  
Register the Google Drive application in your ServiceNow instance to enable OAuth authorization for exporting table records directly to Google Sheets.
-   **[Configure ServiceNow connection and credential aliases for Google sheets](../task/config-connect-credentials-aliases-for-gsheets.md)**  
Configure connection and credential aliases to authenticate an integration between your ServiceNow instance and Google Drive.

**Parent Topic:**[Exporting data](c_ExportData.md)

**Related topics**  


[Export data from a record](../task/export-form-data.md)

[Export data from a list](../task/export-list-data.md)

[Export directly from a URL](../task/t_ExportDirectlyFromTheURL.md)

[Exporting and importing data via XML](../../development-best-practices/concept/c_ExportAndImportXMLFiles.md)

[Exporting currency fields to Excel](c_ExportingCurrencyFields.md)

[Enable export debug logging](c_EnableExportDebugLogging.md)

[Data export reference](../reference/data-export-reference.md)

