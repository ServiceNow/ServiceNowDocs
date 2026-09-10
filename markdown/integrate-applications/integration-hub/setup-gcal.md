---
title: Set up the Google Calendar spoke
description: Set up an outbound integration between your ServiceNow instance and the Google Calendar Application Programming Interfaces \(API\) by setting up a connection and credential record.Create an OAuth application on the Google Calendar that authenticates requests to access the Google Calendar APIs from your ServiceNow instance. After successful authentication, you can generate an OAuth token that your ServiceNow can use to access the Google Calendar APIs.Create a connection and credential record that enables your ServiceNow instance to integrate with the Google Calendar Application Programming Interface \(API\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-gcal.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 5
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

        \[Omitted image "google-calendar-spokes-click-create-project.png"\] Alt text: Create project button for Google Calendar on Google Workspace.

    2.  On the Select a Project window, select **NEW PROJECT**.

    3.  In the Project name field, enter a unique name for the project.

    4.  In the Location field, select BROWSE to select an organization.

    5.  Select **CREATE**.

        The Notifications window confirms that the project is created.

        \[Omitted image "gcalendar-spoke-proj-created.png"\] Alt text: Project creation confirmation.

    6.  Select SELECT PROJECT.

3.  Enable the Google Calendar API permissions.

    1.  Select **+ ENABLE APIS AND SERVICES**.

        \[Omitted image "gcalendar-spoke-enable-api.png"\] Alt text: Enable API and Services button.

    2.  On the Welcome to the API Library page, navigate to the Google calendar API card under the Google Workspace heading.

        \[Omitted image "gcalendar-spoke-api-button.png"\] Alt text: Google Calendar API button.

    3.  Select **Google Calendar API**.

    4.  Select **ENABLE**.

        The Google calendar API is enabled on your project.

        \[Omitted image "google-calendar-api-enabled.png"\] Alt text: Google Calendar API is enabled.

4.  Create the credentials that the connection and credential form will store.

    1.  Select **CREATE CREDENTIALS**.

        \[Omitted image "google-calendar-create-creds.png"\] Alt text: Create credentials button to access Google Calendar API.

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

        \[Omitted image "gcalendar-spoke-scope.png"\] Alt text: Enter Google Calendar in the field.

    3.  From the list, select Google Calendar API.

    4.  Select the required APIs from the list.

        \[Omitted image "gcalendar-spoke-api-selection.png"\] Alt text: Select required Google Calendar APIs.

    5.  Select **UPDATE**.

6.  Generate the OAuth Client ID and related details.

    You must enter the OAuth Client ID and related details in the connection and credential form.

    1.  In the Application type field, select `Web application`.

    2.  In the Name field, enter a custom name for the application.

    3.  To add a redirect URL, under the Authorised redirect URIs heading, select **+ ADD URI**.

    4.  Enter the URL of your ServiceNow instance.

    5.  Select **CREATE**.

        The credentials for the OAuth application are created, as shown in the image.\[Omitted image "google-calendar-copy-creds.png"\] Alt text: Copy or download the OAuth credentials.

7.  Select **DONE**.


## Create Connection and Credential record for the Google Calendar spoke

Create a connection and credential record that enables your ServiceNow instance to integrate with the Google Calendar Application Programming Interface \(API\).

### Before you begin

Role required: admin.

### About this task

The connection and credential record includes the details that you had set up when you created the OAuth app. See [Create OAuth application on Google Calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-gcal.md).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Google Calendar** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Google Calendar spoke, click **View Details**.

        \[Omitted image "image.gcalendar-connection"\] Alt text: Connection for the Google Calendar spoke

    -   To manage more than one Google Calendar spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "image.gcalendar-connect-config"\] Alt text: Initial connection configuration

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Name|Auto-generated name to identify the connection record.|
    |URL|Auto-generated URL for the Google APIs website.|
    |API Version|Auto-generated input of the current API version.|
    |Credential Information|
    |OAuth Client ID|Client ID you created during the Google Calendar application registration.|
    |OAuth Client Secret|Key value you created during the Google Calendar application registration.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.|
    |Auth URL|Authorization URL for your Google Calendar configuration.|
    |Token URL|Token URL for your Google Calendar configuration.|

    \[Omitted image "image.gcalendar-config-temp"\] Alt text: Configure a connection for the Google Calendar spoke.

6.  Click **Save and Get OAuth Token**.


