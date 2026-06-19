---
title: Set up the Google Sheet spoke
description: Set up an outbound integration between your ServiceNow instance and the Google Sheets by setting up a connection and credential record.Set up an OAuth application on the Google Sheets API to enable authentication of requests from your ServiceNow instance.Create a connection and credential record that contains the details required to connect to the Google Sheets Application Programming Interfaces \(API\) on the Google Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-gsheets.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Google Sheets Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Sheet spoke

Set up an outbound integration between your ServiceNow instance and the Google Sheets by setting up a connection and credential record.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Sheets spoke plugin.
-   Role required: admin.

## About this task

The Google Sheets API authenticates the requests from your ServiceNow instance through an OAuth application. You must [Set up OAuth app on Google Sheets API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-gsheets.md) by visiting the [https://console.developers.google.com/](https://console.developers.google.com/). The connection and credentials record contains the information the Google Sheets API must authenticate the requests from your ServiceNow instance.

## Set up OAuth app on Google Sheets API

Set up an OAuth application on the Google Sheets API to enable authentication of requests from your ServiceNow instance.

### Before you begin

-   Create a business account on [https://console.developers.google.com/](https://console.developers.google.com/)
-   Create a domain and an email address associated with the domain. For example, www.mydomain.com and jane-admin@mydomain.com.

    **Note:** You can only register one email address per domain in Google Workspace.

-   Role required: admin

### Procedure

1.  Set up a project on the Google Workspace.

    The project includes the details of the OAuth application and the Application Programming Interface \(API\) permissions, if applicable.

    1.  Log in to [https://console.developers.google.com/](https://console.developers.google.com/) with the same domain email ID and password as mentioned in the prerequisites.

    2.  Select the button.

        \[Omitted image "google-calendar-spokes-click-create-project.png"\] Alt text: Project creation button on Google Workspace.

    3.  Select **NEW PROJECT**.

        \[Omitted image "google-calendar-spoke-create-project.png"\] Alt text: Click New Project button on Google Workspace.

    4.  In the Project name\* field, enter a unique name for the project.

    5.  In the Location\* field, select **BROWSE** to select an organization.

    6.  Select **CREATE**.

        The project is created.

    7.  Select the button.

        \[Omitted image "google-calendar-spokes-click-create-project.png"\] Alt text: Select the project.

2.  Select the project that you created.

    \[Omitted image "gsheets-select-project.png"\] Alt text: Project selection on Google Sheets API.

3.  Enable the Google Sheets API.

    1.  Click **+ENABLE APIS AND SERVICES**.

        \[Omitted image "gsheets-enable-apis.png"\] Alt text: Google Sheets API Enable APIs and Services button.

    2.  On the Welcome to the API Library page, enter `Google Sheets` in the search box.

    3.  Press **Enter**.

    4.  Select the Google Sheets API button.

    5.  Select **ENABLE**.

        The Google Sheets APIs are enabled on your project.

4.  Create the OAuth app and credentials.

    1.  Select **CREATE CREDENTIALS**.

        \[Omitted image "google-sheets-create-creds.png"\] Alt text: Click Credentials button for Google Sheets API.

    2.  Fill the form.

<table id="table_rxt_zgw_5wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select an API\*

</td><td>

Name of the API for which you're creating the credentials.**Note:** Ensure that you select Google Sheets API.

</td></tr><tr><td>

What data will you be accessing? \*

</td><td>

Type of data your ServiceNow will access through the APIs.**Tip:** Select User data.

</td></tr></tbody>
</table>    3.  Click **NEXT**.

    4.  Fill the form.

        |Field|Description|Mandatory?|
        |-----|-----------|----------|
        |App name|Name of the OAuth app.|Yes|
        |User support email|Email at which users can send queries to you about their consent.|Yes|
        |Logo file to upload|Logo representing the OAuth app.|No|
        |Developer contact information|Google will contact the developer of the OAuth app if there are any changes to the project.|Yes|

    5.  Click **SAVE AND CONTINUE**.

5.  Define the API scopes.

    API scopes enable you to select specific APIs. For example, /auth/spreadsheets scope enables you to create, edit, or remove spreadsheets.

    1.  Click **ADD OR REMOVE SCOPES**.

    2.  Enter `Google sheets API`, as shown in the image.

        \[Omitted image "google-sheets-search-scopes.png"\] Alt text: Search Google Sheets in the scopes.

    3.  Select one or more scopes.

    4.  Click **UPDATE**.

    5.  Click **SAVE AND CONTINUE**.

6.  Generate OAuth client ID.

    1.  From the Application type\* list, select `Web application`.

    2.  In the Name\* field, enter a unique name of the OAuth client.

7.  Under the Authorised redirect URIs heading, click **+ ADD URI**.

8.  In the URI field, enter the redirect URI in the following format: `https://instance.service-now.com/oauth_redirect.do`.

9.  Click **CREATE**.

    The OAuth details are generated in a JSON file.

    **Tip:** Click DOWNLOAD to download the JSON file for later reference.

    \[Omitted image "google-sheets-download-json.png"\] Alt text: Download button to download OAuth credentials file.

10. Click **DONE**.

    You've created the OAuth application on Google Workspace.


## Create Connection and Credential record for Google Sheets spoke

Create a connection and credential record that contains the details required to connect to the Google Sheets Application Programming Interfaces \(API\) on the Google Workspace.

### Before you begin

-   Create an OAuth application for the Google Sheets APIs in the Google Workspace. To learn how to create an OAuth application, see [Set up OAuth app on Google Sheets API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-gsheets.md).
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click Connections.

3.  In the Search all connections field, enter `Google sheets`.\[Omitted image "google-sheets-search-conn.png"\] Alt text: Search Google Sheets alias on Flow Designer alias.

4.  On the GoogleSheets card, click **View Details**.

5.  Click **Configure**, as shown in the image.\[Omitted image "google-sheets-click-configure.png"\] Alt text: Configure button on Google Sheets alias.

6.  Fill the form.

<table id="table_vyw_bk4_3mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.**Note:** The field is read-only.

</td></tr><tr><td>

Connection URL

</td><td>

The URL used for connecting to Google Sheets APIs. This field is automatically set to `https://sheets.googleapis.com/v4/spreadsheets`

</td></tr><tr><td>

Credential Name

</td><td>

Name of the credential. This field is automatically set to `Google Sheets Spoke Credential`.

</td></tr><tr><td>

OAuth Entity Name

</td><td>

Name of the OAuth entity profile. This field is automatically set to `Google Sheets Spoke OAuth`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID of the Google Sheets application you registered in G Suite.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret generated when you registered the application in Google API Console.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The redirect URL. The format of the URL is `https://<your-instance>.service-now.com/oauth_redirect.do`

</td></tr></tbody>
</table>7.  Click **Create and Get OAuth Token**.


