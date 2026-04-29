---
title: Set up the Google Calendar spoke
description: Set up an outbound integration between your ServiceNow instance and the Google Calendar Application Programming Interfaces \(API\) by setting up a connection and credential record.Create an OAuth application on the Google Calendar that authenticates requests to access the Google Calendar APIs from your ServiceNow instance. After successful authentication, you can generate an OAuth token that your ServiceNow can use to access the Google Calendar APIs.Create a connection and credential record that enables your ServiceNow instance to integrate with the Google Calendar Application Programming Interface \(API\).
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 6
breadcrumb: [Google Calendar Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Calendar spoke

Set up an outbound integration between your ServiceNow instance and the Google Calendar Application Programming Interfaces \(API\) by setting up a connection and credential record.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Calendar spoke.
-   Ensure that you have a Google Workspace account.
-   Ensure that you have a domain and an email address related with the domain. For example, www.mydomain.com and jane-admin@mydomain.com.

    **Note:** you can only register one email address per domain in Google Workspace.

-   Role required: admin.

## Create OAuth application on Google Calendar

Create an OAuth application on the Google Calendar that authenticates requests to access the Google Calendar APIs from your ServiceNow instance. After successful authentication, you can generate an OAuth token that your ServiceNow can use to access the Google Calendar APIs.

### Before you begin

Google Calendar spoke integration requirements:

-   A domain and an email address associated with the domain. For example, www.mydomain.com and jane-admin@mydomain.com. Note that you can only register one email address per domain in Google Workspace.
-   Google Workspace login credentials created with the same domain.

Role required: admin.

### Procedure

1.  Log in to [https://console.developers.google.com](https://console.developers.google.com) with your Google Workspace credentials.

2.  Create a project on Google Workspace.

    The project provides the OAuth application and the permissions to access the Google Calendar APIs from your ServiceNow instance.

    1.  Select the button.

        ![Create project button for Google Calendar on Google Workspace.](../image/google-calendar-spokes-click-create-project.png)

    2.  On the Select a Project window, select **NEW PROJECT**.

    3.  In the Project name field, enter a unique name for the project.

    4.  In the Location field, select BROWSE to select an organization.

    5.  Select **CREATE**.

        The Notifications window confirms that the project is created.

        ![Project creation confirmation.](../image/gcalendar-spoke-proj-created.png)

    6.  Select SELECT PROJECT.

3.  Enable the Google Calendar API permissions.

    1.  Select **+ ENABLE APIS AND SERVICES**.

        ![Enable API and Services button.](../image/gcalendar-spoke-enable-api.png)

    2.  On the Welcome to the API Library page, navigate to the Google calendar API card under the Google Workspace heading.

        ![Google Calendar API button.](../image/gcalendar-spoke-api-button.png)

    3.  Select **Google Calendar API**.

    4.  Select **ENABLE**.

        The Google calendar API is enabled on your project.

        ![Google Calendar API is enabled.](../image/google-calendar-api-enabled.png)

4.  Create the credentials that the connection and credential form will store.

    1.  Select **CREATE CREDENTIALS**.

        ![Create credentials button to access Google Calendar API.](../image/google-calendar-create-creds.png)

    2.  Fill the form.

<table id="table_fx2_vlh_5wb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Select an API

</td><td>

Name of the API that your ServiceNow instance accesses. **Note:** Ensure that the Google Calendar API option is chosen.

</td></tr><tr><td>

What data will you be accessing? \*

</td><td>

Type of data that your ServiceNow instance accesses from the Google Calendar application.**Tip:** To create an OAuth application, select User data.

</td></tr></tbody>
</table>    3.  Select **NEXT**.

    4.  In the OAuth Consent Screen section, fill the form.

        |Field|Description|Mandatory?|
        |-----|-----------|----------|
        |App name|Custom name of the OAuth app.|Yes|
        |User support email|Users of the OAuth app can send their queries on consent to this email.|Yes|
        |App logo|Logo of the OAuth app,|No|
        |Developer contact information|Google uses this email ID to inform you about any changes to the project.|Yes|

    5.  Select **SAVE AND CONTINUE**.

5.  Specify the permissions to access specific Google Calendar API.

    1.  Under the SCOPES heading, select **ADD OR REMOVE SCOPES**.

    2.  In the Update selected scopes window, enter `Google Calendar` in the Enter property name or value field.

        ![Enter Google Calendar in the field.](../image/gcalendar-spoke-scope.png)

    3.  From the list, select Google Calendar API.

    4.  Select the required APIs from the list.

        ![Select required Google Calendar APIs.](../image/gcalendar-spoke-api-selection.png)

    5.  Select **UPDATE**.

6.  Generate the OAuth Client ID and related details.

    You must enter the OAuth Client ID and related details in the connection and credential form.

    1.  In the Application type field, select `Web application`.

    2.  In the Name field, enter a custom name for the application.

    3.  To add a redirect URL, under the Authorised redirect URIs heading, select **+ ADD URI**.

    4.  Enter the URL of your ServiceNow instance.

    5.  Select **CREATE**.

        The credentials for the OAuth application are created, as shown in the image.![Copy or download the OAuth credentials.](../image/google-calendar-copy-creds.png)

7.  Select **DONE**.


## Create Connection and Credential record for the Google Calendar spoke

Create a connection and credential record that enables your ServiceNow instance to integrate with the Google Calendar Application Programming Interface \(API\).

### Before you begin

Role required: admin.

### About this task

The connection and credential record includes the details that you had set up when you created the OAuth app. See [Create OAuth application on Google Calendar](setup-gcal.md#).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select Connections.

3.  In the Search all connections field, enter `Google Calendar`.![Search the Google Calendar connection card.](../image/google-calendar-search-conn-card.png)

4.  On the Google\_Calendar card, click **View Details**.

5.  Click **Configure**.![Google Calendar connection and credential record configure button.](../image/google-calendar-configure-button.png)

6.  Fill the details in the form.

<table id="table_nck_bl4_5wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection with the Google Calendar API.**Note:** The first and default connection name is Google\_Calendar which is read-only. To provide a custom name to the connection, create a connection by selecting **Add Connection**.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to the Google Calendar APIs.Enter `https://googleapis.com`.

</td></tr><tr><td>

API Version

</td><td>

Version of the Google Calendar APIs that your ServiceNow instance accesses.Enter `V3`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

The ID of the client that accesses the OAuth app you had created.**Tip:** You can find the OAuth Client ID in the JSON file you had downloaded while creating the OAuth app. See [Create OAuth application on Google Calendar](setup-gcal.md#).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

The secret that your ServiceNow instance uses to prove its identity to the OAuth app.**Tip:** You can find the OAuth Client secret in the JSON file you had downloaded while creating the OAuth app. See [Create OAuth application on Google Calendar](setup-gcal.md#).

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The redirect URL to the application after the OAuth app authenticates the request from your ServiceNow instance.**Tip:** You can find the OAuth Redirect URL in the JSON file you had downloaded while creating the OAuth app. See [Create OAuth application on Google Calendar](setup-gcal.md#).

</td></tr><tr><td>

OAuth Authorization URL

</td><td>

The URL provided by the OAuth service provider that your ServiceNow instance can use to initiate the OAuth authorization process.**Tip:** You can find the OAuth Authorization URL in the JSON file you had downloaded while creating the OAuth app.

</td></tr><tr><td>

OAuth Token URL

</td><td>

The URL provided by an OAuth service provider that your ServiceNow instance can use to exchange an authorization code for an access token.**Tip:** You can find the OAuth Authorization URL in the JSON file you had downloaded while creating the OAuth app.

</td></tr></tbody>
</table>7.  Select **Configure and Get OAuth Token**.

8.  Log in to Google Workspace and get the OAuth Token.

    The connection and credential record is created.


