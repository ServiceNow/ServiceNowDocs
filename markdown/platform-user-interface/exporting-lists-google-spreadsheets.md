---
title: Exporting lists to Google Sheets
description: Configure lists in Configurable Workspace to export directly to Google Sheets.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Lists, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Exporting lists to Google Sheets

Configure lists in Configurable Workspace to export directly to Google Sheets.

You can export data from lists in your Configurable Workspace directly to Google Sheets if your instance is integrated with Google Sheets via OAuth.

To configure and use this functionality, follow these steps:

1.  [Set up the OAuth application on the Google Sheets API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/set-up-oauth-app-gsheets-api.md)

    Set up the OAuth application on the Google Sheets API so that you can authenticate requests from your ServiceNow instance to access Google Sheets.

2.  [Create an application registry for Google Sheets on a ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/configure-app-registry-gsheets.md)

    Register the Google Drive application in your ServiceNow instance to enable OAuth authorization for exporting table records directly to Google Sheets.

3.  [Configure ServiceNow connection and credential aliases for Google sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/config-connect-credentials-aliases-for-gsheets.md)

    Configure connection and credential aliases to authenticate an integration between your ServiceNow instance and Google Drive.


Once configured, exporting a list to Google Sheets displays as an option in Configurable Workspace list export as **Export** &gt; **Google Sheets**.

