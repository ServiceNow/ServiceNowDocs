---
title: Set up the OAuth application on the Google Sheets API
description: Set up the OAuth application on the Google Sheets API so that you can authenticate requests from your ServiceNow instance to access Google Sheets.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exporting your table records to Google Sheets, Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up the OAuth application on the Google Sheets API

Set up the OAuth application on the Google Sheets API so that you can authenticate requests from your ServiceNow instance to access Google Sheets.

## Before you begin

-   Create a business account on [https://console.developers.google.com/](https://console.developers.google.com/).
-   Create a domain and an email address that is associated with the domain. For example, www.mydomain.com and jane-admin@mydomain.com.

    **Note:** You can register only one email address per domain in Google Workspace.

-   Role required: admin

## About this task

Setting up the OAuth application on the Google Sheets API enables you to access and update spreadsheets securely from your instance. For example, if you're exporting incident records from the ServiceNow instance to a Google Sheet, OAuth ensures that the system has permission to create or update the sheet on your behalf, without needing you to log in manually each time.

## Procedure

1.  Navigate to Google Workspace and set up a project.

    The project includes the details of the OAuth application and the API permissions, if applicable.

    1.  Log in to [https://console.developers.google.com/](https://console.developers.google.com/) with the same domain email ID and password as mentioned in the prerequisites.

    2.  In the Google Cloud Console, select **Select a project**.

        ![Creating a project on Google Workspace.](../image/google-calendar-spokes-click-create-project.png)

    3.  In the **Search projects and folders** field, select **New project**.

        ![Creating a new project on Google Workspace.](../image/gsheets-select-project.png)

    4.  In the **Project name\*** field, enter a unique name for the project.

    5.  In the **Location\*** field, select **Browse** and then select an organization.

    6.  Select **Create**.

        The project is created and appears in the Notifications box.

2.  Enable the Google Sheets API.

    ![Project selection on Google Sheets API.](../image/gsheets-select-project.png)

    1.  Open the project that you created in step 1.

        The API and services dashboard page opens for the selected project.

    2.  In the search box, enter `Google Drive`.

    3.  From the search results list, select **Google Drive API**.

        ![Searching for Google Drive API.](../image/search-gdrive-api.png)

    4.  Select **Enable**.

        The Google Drive APIs are enabled on your project.

3.  Create the OAuth app and credentials.

    1.  In the Enabled APIs &amp; services dashboard, select **Create credentials**.

        The Create credentials page is displayed.

        ![Create credentials button in the Google workspace.](../image/create-credentials-gsheets.png)

    2.  In the Credential Type section, select **User data** and then select **Next**.

        ![Create credentials form displays in the APIs & Services dashboard in Google Workspace.](../image/credential-type-gsheets.png)

    3.  On the form in the OAuth Consent, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |App name|Name of the OAuth app.|
        |User support email|Email at which users can send queries to you about their consent.|
        |Logo file to upload|Logo representing the OAuth app.|
        |Developer contact information|Developer to contact for changes to the project.|

    4.  Select **Save and continue**.

4.  In the Scopes section, define the API scopes.

    API scopes enable you to select specific APIs. For example, the /auth/spreadsheets scope enables you to create, edit, or remove spreadsheets.

    1.  Select **Add or remove scopes**.

        ![Adding or removing scopes in the Scopes section of the Create credentials form.](../image/scopes-gsheets.png)

    2.  In the Update selected scopes list, search for Google Drive API, and then select the `.../auth/drive.file` scope.

        ![Selecting a file for the Google Drive API scope.](../image/select-gdapi-scope.png)

    3.  Select **Update** and then select **Save and continue**.

    The API scope is selected.

5.  In the OAuth Client ID section, create the OAuth client ID.

    1.  From the Application type\* list, select **Web application**.

    2.  In the **Name\*** field, enter a unique name for the OAuth client.

6.  On the Authorized redirect URIs heading, select **+ ADD URI**.

7.  In the **URI** field, enter the redirect URI in the following format: `https://instance.service-now.com/oauth_redirect.do`.

8.  Select **Create**.

    The OAuth details are generated in a JSON file.

    **Tip:** Select **DOWNLOAD** to download the JSON file for later reference.

    ![Downloading the OAuth credentials file.](../image/download-gsheets-credentials.png)

9.  Select **Done**.

    The OAuth application on Google Workspace is created.

10. Configure the audience allowed to access Google Sheets API.

    For example, your audience is the ServiceNow instance.

    1.  In the APIs &amp; Services dashboard menu, select **OAuth consent screen** and then select **Audience**.

    2.  In the User type section, select **External** and add the user that you want to give access to the instance.


## Result

The OAuth application is enabled to authenticate the access of Google Sheets from your instance.

## What to do next

To enable OAuth authorization for exporting table records to Google Sheets, register the Google Drive application in your instance. For more information, see [Create an application registry for Google Sheets on a ServiceNow instance](configure-app-registry-gsheets.md).

**Parent Topic:**[Exporting your table records to Google Sheets](../concept/setup-gsheet-export.md)

