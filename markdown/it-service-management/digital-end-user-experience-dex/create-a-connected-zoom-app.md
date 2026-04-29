---
title: Create a connected Zoom application
description: Create a connected application in your Zoom account to establish an OAuth 2.0 level of authentication between the Zoom APIs and the DEX for Zoom on the ServiceNow AI Platform. After creating the connected app, you can add scopes that enable you to perform different actions from the DEX for Zoom.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring DEX for Zoom, Configure, Digital End-User Experience, IT Service Management]
---

# Create a connected Zoom application

Create a connected application in your Zoom account to establish an OAuth 2.0 level of authentication between the Zoom APIs and the DEX for Zoom on the ServiceNow AI Platform. After creating the connected app, you can add scopes that enable you to perform different actions from the DEX for Zoom.

## Before you begin

1.  Create a Zoom account
2.  Role required: Zoom admin

## About this task

Creating the connected app is a one-time activity.

## Procedure

1.  Log in to [Zoom marketplace](https://marketplace.zoom.us/).

2.  Navigate to **Develop** &gt; **Build App**.

3.  Select **General App**.

4.  Select **Create**.

5.  Double-click the default name of the app and update the name.

    ![Update general app name.](zoom-spk-app-name.png)

6.  Select **Admin-managed**.

7.  Select **Save**.

8.  Under the **App Credentials** section, copy the Client ID and Client secret and store them at a secure place.

    ![Client ID and client secret.](zoom-spk-client-id-secret.png)

9.  Under the **OAuth Information** section, complete the following steps.

    1.  In the **OAuth Redirect URL** field, enter the redirect URL in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

    2.  Under **OAuth Allow List**, add a ServiceNow instance redirect URL in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

        A token is generated. This token is used by the OAuth app to give the Zoom spokes access to the Zoom APIs.

    3.  To add another URL to the allow list, select **Add New List**.

        The following example shows the screen that you use to generate credentials for the OAuth app.

        ![OAuth credentials configuration for Zoom spokes.](zoom-app-conf.png)

        **Note:** To learn more about the difference between the Redirect URL for OAuth and the URL that is mentioned in the OAuth allow list, see [Zoom Developer Forum](https://devforum.zoom.us/t/difference-between-redirect-url-and-allow-list-in-app-settings/58709).

10. Select **Access**.

11. Under the **Access** section, copy the Secret Token.

12. Select **Scopes**.

13. Select **+ Add Scopes** and add the following scopes:

    -   report:read:user:admin
    -   dashboard:read:list\_meeting\_participants\_qos:admin
    -   dashboard:read:meeting\_participant\_qos:admin
    -   dashboard:read:list\_zoomrooms:admin
    -   dashboard:read:issues\_zoomroom:admin
    -   user:read:user:admin
14. In the **Search** scope field, enter the granular scope.

    An example of a granular scope is `meeting:delete:meeting:admin`.

    The granular scope appears.

    ![Scope search and find.](zoom-spk-find-scope.png)

15. Select the scope and then select **Done**.

    The granular scope is added.

    ![Granular scope added](Zoom_scope_added.png)

16. Repeat the steps to add more granular scopes.


