---
title: Authenticate Google for calendar synchronization
description: Set up Google to start with reservation synchronization with the Workplace Reservation Management application. Create scopes, credentials and more.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Authenticate Google for calendar synchronization

Set up Google to start with reservation synchronization with the Workplace Reservation Management application. Create scopes, credentials and more.

## Before you begin

Ensure the following:

1.  Install [Google Calendar Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/gcal-spoke.md).
2.  [Set up Google Calendar spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-gcal.md)

Role required: Google Admin

## Procedure

1.  Log in to [https://admin.google.com/](https://admin.google.com/).

2.  If you want to manage users for the Google account, do the following:

    1.  Select **Manage** in the **Users** card on the homepage.

    2.  Add, delete, or update user details.

3.  Log in to [https://console.cloud.google.com/](https://console.cloud.google.com/) with your google workspace credentials.

4.  Create a project to get the OAuth authentication and the permission to use the Google Calendar from ServiceNow.

    1.  Select **Select a project** on the top panel.

    2.  On the select a project window, select **NEW PROJECT**.

    3.  Enter project details.

        1.  Specify the **Project name**.
        2.  Select your **Organization**.
        3.  In the **Location** field, select **Browse** and select your organization.
    4.  Select **CREATE**.

        A notification is displayed that the project is created.

    5.  In the notification window, select **SELECT PROJECT**.

5.  Set Google Calendar API permissions.

    1.  On the homepage, select **APIs &amp; Services**.

    2.  On the top panel, select **+ ENABLE APIS AND SERVICES**.

    3.  On the Welcome to the API Library page, under the Google Workspace, select **Google Calendar API**.

    4.  On the Google Calendar API details page, select **ENABLE**.

        The Google calendar API is enabled on your project.

6.  Create credentials to use when creating a connection and credential for Google

    1.  On the Google Calendar API details page, select **CREATE CREDENTIALS**.

    2.  On the Google Calendar API credentials form, fill in the fields:

        1.  In the **Select an API** field, select **Google Calendar API**.
        2.  Under the **What data will you be accessing?** section, select **User data** to create an OAuth application.
    3.  Select **NEXT**.

    4.  In the OAuth Consent Screen section, fill the fields:

        1.  In the **App name** field, specify a name for the OAuth app.
        2.  In the **User support email** field, specify the user email to which consent-related questions can be sent.
        3.  In the App logo section, select **BROWSE** to upload a logo for the OAuth app.
        4.  In the Developer contact information section, specify the email address to which any project-related changes and updates must be sent.
    5.  Select **SAVE AND CONTINUE**.

7.  Add or remove scopes.

    Specify permissions to access the Google Calendar API.

    1.  Under Scopes section, select **ADD OR REMOVE SCOPES**.

    2.  Select the following scopes:

        -   [https://www.googleapis.com/auth/calendar](https://www.googleapis.com/auth/calendar)
        -   [https://www.googleapis.com/auth/calendar.events](https://www.googleapis.com/auth/calendar.events)
    3.  Select **UPDATE**.

    4.  Select **SAVE AND CONTINUE**.

8.  Generate the OAuth Client ID and related details.

    1.  Under the OAuth Client ID section, in the **Application type** field, select **Web application**.

    2.  In the **Name** field, enter a name for the application.

    3.  Under the Authorized JavaScript origins, select **+ADD URL** to add the JavaScript URL.

    4.  Under the Authorized redirect URIs section, select **+ADD URL** to add a redirect URL.

        Enter the URL of your ServiceNow instance.

    5.  Select **CREATE**.

        The credentials for the OAuth application are created.

    6.  Select **DOWNLOAD** to download the JSON file that contains the credential details.

    7.  Copy and save the Client ID.

9.  Select **DONE**.


