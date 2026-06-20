---
title: Set up the Google Meet spoke
description: Integrate the ServiceNow instance and Google Meet by creating a custom OAuth application in the Google Cloud console to authenticate ServiceNow requests.Create OAuth credentials that your ServiceNow instance uses to have its requests for connection authenticated by Google Cloud console.Set up the connection between your ServiceNow instance and the Google Meet APIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/set-up-the-google-meet-spoke.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Google Meet Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Meet spoke

Integrate the ServiceNow instance and Google Meet by creating a custom OAuth application in the Google Cloud console to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Meet spoke.
-   Role required: admin.

## Create OAuth credentials for Google Meet API

Create OAuth credentials that your ServiceNow instance uses to have its requests for connection authenticated by Google Cloud console.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the [Google Cloud console](https://console.cloud.google.com/).

2.  Select the project button.

    \[Omitted image "gmeet-spk-gconsole-new-proj.png"\] Alt text: Project button on Google Cloud console landing page.

3.  On the Select a project window, select **NEW PROJECT**.

4.  Set up the new project.

    1.  In the Project name field, enter the project name.

    2.  In the Location field, select **BROWSE** to select an organization.

    3.  Select **CREATE**.

        Notifications show that the project is created.

        \[Omitted image "gmeet-spk-oauth-proj.png"\] Alt text: Notification that the project is created.

5.  Select **SELECT PROJECT**.

6.  Navigate to **Navigation Menu** &gt; **APIs &amp; Services** &gt; **Enabled APIs &amp; Services**.

7.  Select **+ENABLE APIS AND SERVICES**.

8.  In the Search for APIs and services field, enter `Google Meet REST API` and press **Enter**.

9.  Select **Google Meet REST API**.

10. Select **ENABLE**.

11. Select the **CREDENTIALS** tab.

    \[Omitted image "gmeet-spk-creds-tab.png"\] Alt text: CREDENTIALS tab.

12. Select **+ CREATE CREDENTIALS** and then select **OAuth client ID.**

    \[Omitted image "gmeet-spk-create-creds.png"\] Alt text: OAuth Client ID option in the CREDENTIALS tab.

13. Select **CONFIGURE CONSENT SCREEN**.

    **Note:** Refresh token expires in 7 days when a Google Cloud Platform project with an OAuth consent screen is configured for an external user type and its publishing status is **Testing**. To get new OAuth, click **Edit and Get OAuth Token** by navigating to the associated connection.

    \[Omitted image "gmeet-oauth.jpg"\] Alt text: Refresh token after it expires.

14. Select **Internal**.

15. Select **CREATE**.

16. Fill the form.

    |Field|Description|
    |-----|-----------|
    |App name|Option to provide a name of the OAuth application that you're creating.|
    |User support email|Option to provide the email ID that the users of the OAuth application can use to request support.|
    |Developer contact information|Option to provide the email ID of the developer of the OAuth application.|

    \[Omitted image "gmeet-spk-consent-form.png"\] Alt text: OAuth consent screen.

17. Select **SAVE AND CONTINUE**.

18. Select **ADD OR REMOVE SCOPES**.

19. In the Filter field, enter the scope `meetings.space.created`, `openid`, and `meetings.space.readonly`, and then select the scope value.

    \[Omitted image "gmeet-spk-scopes.png"\] Alt text: OAuth scopes.

20. Select **UPDATE**.

    The scopes appear under the Your non-sensitive scopes and Your sensitive scopes sections.

    \[Omitted image "gmeet-spk-oauth-scopes.png"\] Alt text: OAuth scopes appear.

21. Select **SAVE AND CONTINUE**.

22. On the left panel, select **Credentials**.

23. Navigate to **+CREATE CREDENTIALS** **OAuth client ID**.

24. In the Application type field, select **Web application**.

25. In the Name field, enter a name of the application.

26. Under the Authorized redirect URIs, select **+ADD URI**.

27. In the URI1 field, enter the redirect URL in the format `https://<your-instance-name>.service-now.com/oauth_redirect.do`.

28. Select **CREATE**.

29. Copy the client ID and client secret and store at secure place.

    \[Omitted image "gmeet-spk-client-details.png"\] Alt text: Client details.

30. Select **OK**.


## Configure connection for Google Meet spoke

Set up the connection between your ServiceNow instance and the Google Meet APIs.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Confirm that the **Outbound** tab is selected.

4.  In the Search all connections field, enter `Google Meet`.

5.  On the Google Meet tile, select **View Details**.

    \[Omitted image "gmeet-spk-alias-card.png"\] Alt text:

6.  Select **Configure**.

7.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Name that uniquely identifies the connection record.|
    |Connection URL|URL to Google Meet APIs. Enter `https://meet.googleapis.com`.|
    |Client ID|OAuth client ID of the Google Meet OAuth app that you had created in the Google Cloud console.|
    |Client Secret|OAuth client secret of the Google Meet OAuth app that you had created in the Google Cloud console.|
    |Redirect URL|OAuth redirect URL of your ServiceNow instance. Enter in this format `https://<your-instance-name>.service.now.com/oauth_redirect.do`.|

    \[Omitted image "gmeet-spk-conn-form.png"\] Alt text: Create Connection form.

8.  Select **Create and Get OAuth Token**.

    You must log in to the Google Cloud console to fetch the OAuth token.


