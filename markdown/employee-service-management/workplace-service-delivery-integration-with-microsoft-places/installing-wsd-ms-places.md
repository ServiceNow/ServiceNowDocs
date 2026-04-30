---
title: Register WSD for Microsoft places
description: Register the WSD for Microsoft places application in the Microsoft Azure portal.
locale: en-US
release: xanadu
product: Workplace Service Delivery Integration with Microsoft Places
classification: workplace-service-delivery-integration-with-microsoft-places
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure WSD for Microsoft places, WSD for Microsoft places, Workplace Service Delivery, Employee Service Management]
---

# Register WSD for Microsoft places

Register the WSD for Microsoft places application in the Microsoft Azure portal.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your Microsoft Azure portal.

2.  Click **App registrations**.

3.  Click **+ New registration**.

4.  In the **Display name** field, provide the name for the application.

    The values for the **Application \(client\) ID**, **Directory \(tenant\) ID**, **Object ID**, and **Application ID URL** fields are auto-generated.

5.  Set the application permissions.

    1.  Go to **API permissions**.

    2.  Under **Configured permissions**, add the following permissions and provide **Grand admin consent for ServiceNow**.

        -   Calendars\_ReadWrite
        -   email
        -   offline\_access
        -   openid
        -   profile
        -   User\_Read
6.  Go to **Expose an API**.

7.  In the **Application ID URI** field, replace the application ID with the value in the **Application \(client\) ID** field.

    For example: `api://msplacesdemo.service-now.com/<Application (client) ID>`.

8.  Add a scope.

    1.  Click **+ Add a scope**.

    2.  Enter the **Scope name** field value as `access_as_user`.

    3.  Enter the **Admin consent display name**, **Admin consent description** details and select **Add scope**.

    **Scopes** record is created.

9.  Under **Authorized client applications**, add clients you like to authorize by selecting **+Add a client application**.

    1.  In the **Client ID** field, enter the following Client Ids and select the Authorized scopes check box.

        -   5e3ce6c0-2b1f-4285-8d4b-75ee78787346
        -   1fec8e78-bce4-4aaf-ab1b-5451cc387264
        -   bc59ab01-8403-45c6-8796-ac3ef710b3e3
        -   89bee1f7-5e6e-4d8a-9f3d-ecd601259da7
        -   4765445b-32c6-49b0-83e6-1d93765276ca
        -   0ec893e0-5785-4de6-99da-4ed124e5296c
        -   27922004-5251-4030-b22d-91ecd9a37ea4
    2.  Select **Add application**.

10. Go to **Authentication**.

11. Under **Web Redirect URLs** add the URI.

    For example: `https://msplacesdemo.service-now/sn_now_teams_ms_login.do`

12. Under **Implicit grant and hybrid flows**, select the **Access tokens** and **ID tokens** check box.

13. Under **Supported account types**, select the required account type.

14. Select **Save**.


## What to do next

Follow up with downloading the manifest files.

**Related topics**  


[Download manifest files](download-manifest-files.md)

