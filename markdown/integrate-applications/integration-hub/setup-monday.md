---
title: Set up the monday.com spoke
description: Integrate the ServiceNow instance and monday.com by creating a custom OAuth application in monday.com to authenticate ServiceNow requests.Create a monday OAuth2 application to authorize access to the monday.com API.Create a connection between your monday applications and your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [monday.com Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the monday.com spoke

Integrate the ServiceNow instance and monday.com by creating a custom OAuth application in monday.com to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the monday.com spoke.
-   monday.com role required: admin.
-   Role required: admin.

## Create a monday OAuth2 application

Create a monday OAuth2 application to authorize access to the monday.com API.

### Before you begin

Role required: monday.com admin.

### About this task

A monday application enables you to build workflows, user experiences, and products on top of the existing monday.com work operating system \(Work OS\). When you configure a monday application to use OAuth2, it is granted access to the monday.com API so that it can read and modify user data.

### Procedure

1.  From a web browser, go to [monday.com](https://monday.com/).

2.  Log in using your admin credentials.

3.  At the bottom of the left navigation menu, click your profile icon and then select **Developers**.

    The My Apps page opens.

4.  Click **Create App**.

    The Basic Information page for the new application opens.

5.  In the Display Information section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the monday application.|
    |Short Description|Description of the application.|

6.  In the same section, add your own application icon by clicking the auto-generated icon and then selecting an icon image.

    You can also change the icon color by clicking **App Color** and then selecting either a preset or custom color. If you do not add your own application icon or select an icon color, the application uses the auto-generated icon and default icon color.

7.  In the App Credentials section, copy the values in the **Client ID** and **Client Secret** fields.

    Save them in a secure location for later use.

8.  Click **Save App**.

9.  From the left navigation menu of the new application, navigate to **General** &gt; **OAuth**.

    The **Scopes** tab of the OAuth &amp; Permissions page opens.

10. In the Scopes section, specify how the application can access or use different types of user data by selecting the checkboxes for the following OAuth scopes according to your requirement:

    -   **me:read**
    -   **boards:read**
    -   **boards:write**
    -   **workspaces:read**
    -   **workspaces:write**
    -   **users:read**
    -   **users:write**
    -   **account:read**
    -   **notifications:write**
    -   **updates:read**
    -   **updates:write**
    -   **assets:read**
    -   **tags:read**
    -   **teams:read**
    -   **webhooks:write**
    For more information about permission scopes, see [Set Up Permission Scopes](https://developer.monday.com/apps/docs/oauth#set-up-permission-scopes).

11. Click **Save Feature**.

12. Select the **Redirect URLs** tab of the OAuth &amp; Permissions page.

13. In the Redirect URLs section, enter the URL of the OAuth provider that users are redirected to after authentication.

    Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

14. Click **Save Feature**.

15. Navigate to **Manage** &gt; **App Versions**.

16. Click the three dot menu under **Actions** and select **Promote to live**.

    For more information, see [Promoting a draft version to live](https://developer.monday.com/apps/docs/versioning#promoting-a-draft-version-to-live).

17. From the **Promote selected version** pop-up, click **Promote**.


## Create a monday connection

Create a connection between your monday applications and your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Locate your monday connection and then click **Add Connection**.

    The Create Connection and Credential dialog box opens.

4.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection.|
    |Connection URL|Base URL for the monday.com API. This field is automatically set to `https://api.monday.com/v2`.|
    |OAuth Client ID|Client ID that is assigned to your monday application.|
    |OAuth Client Secret|Client secret that is assigned to your monday application.|
    |OAuth Redirect URL|URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the redirect URL that you specified in [Create a monday OAuth2 application](setup-monday.md#).|

5.  Click **Create and Get OAuth Token**.

    The Authorize App dialog box opens.

6.  In the dialog box, sign in using the same monday.com credentials that you used to create your monday application.

7.  Click **Allow**.

    The OAuth access token becomes available for authorizing your monday connection.


